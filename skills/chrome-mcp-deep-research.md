---
name: chrome-mcp-deep-research
description: >
  Automate launching Deep Research queries across Claude.ai, Gemini, and ChatGPT in browser
  tabs using the Chrome MCP. Use this skill whenever the user wants to run deep research prompts
  in batch, launch multiple research tabs, automate browser interactions for AI platforms,
  paste prompts via Chrome MCP, or anything involving "deep research" combined with
  "Chrome MCP", "browser automation", "batch research", or "research tabs". Also trigger when
  the user says things like "run these research prompts", "open research tabs for each batch",
  "launch deep research on these topics", "paste my prompts into Claude/Gemini/ChatGPT", or
  "automate research". Even if the user just says "run the deep research batches" or "kick off
  the research tabs", use this skill. Do NOT use for general web scraping, Puppeteer scripting,
  or non-research browser automation.
---

# Chrome MCP Deep Research Tab Automation

Launch Deep Research queries across Claude.ai, Gemini, and ChatGPT in multiple browser tabs
using the Chrome MCP tools. This skill handles the full sequence: creating tabs, enabling
research mode, inserting prompts, and submitting.

## Prerequisites

Before starting, verify:

1. **Chrome MCP tools** are connected (you need `tabs_create_mcp`, `tabs_context_mcp`,
   `navigate`, `screenshot`, `find`, `computer`, `javascript_tool`, and `read_page`)
2. **Prompt files** exist at the expected path — default is
   `C:\Users\PaulKaThat\deep-research\<city>\prompts\B*.txt`
   (one file per batch, e.g., `B1.txt`, `B2.txt`, ..., `B7.txt`)

If the user hasn't prepared prompt files yet, help them create the directory and save their
prompts before proceeding with the automation.

## Platform: Windows

This skill was built for **Windows**. Key differences from Mac:
- No `osascript` — use `document.execCommand('insertText')` to inject text into editors
- No `cmd+v` — clipboard paste via `ctrl+v` is unreliable in ProseMirror editors on Windows
- Always use `execCommand('insertText')` for text injection (works on Claude.ai and Gemini)

---

## Platform 1: Claude.ai Deep Research

### Core Concept

Claude.ai uses a ProseMirror/TipTap contenteditable `<div>` for its text editor:
- `form_input` tool **will not work**
- `ctrl+v` clipboard paste is **unreliable** on Windows
- Use `document.execCommand('insertText')` to inject text directly
- UI element positions shift — prefer **JS DOM selectors and ref-based clicks** over coordinates

### Automation Sequence (Per Tab)

#### Step 1: Create Tab
```
mcp__Claude_in_Chrome__tabs_create_mcp
```

#### Step 2: Navigate to Claude.ai
```
mcp__Claude_in_Chrome__navigate → https://claude.ai/new
```
Wait **3 seconds** for page to fully load.

#### Step 3: Enable Research Mode

**IMPORTANT:** Research mode activation via automation is unreliable on Claude.ai. The
recommended approach is to insert text and let the user manually toggle Research mode.

If attempting automation:

**Open the toggle menu:**
```javascript
document.querySelector('button[aria-label="Toggle menu"]').click()
```

Wait **1 second** for the menu to render.

**Click the Research option:**
```javascript
const items = document.querySelectorAll('[role="menuitemcheckbox"]');
const research = Array.from(items).find(el => el.textContent.includes('Research'));
if (research) research.click();
```

**Verification:** Use `find` or `read_page` to check if a button labeled "Research mode"
appears in the accessibility tree. If not, inform the user they need to manually toggle it.

#### Step 4: Insert Prompt Text

**Focus the editor and insert text via execCommand:**
```javascript
const editor = document.querySelector('div.tiptap.ProseMirror');
editor.focus();
document.execCommand('insertText', false, "YOUR PROMPT TEXT HERE");
```

**Do not paste twice.** If the first insert appears to fail, take a screenshot to verify.

#### Step 5: Submit the Prompt

**Preferred approach — find + ref click (most reliable):**
```
mcp__Claude_in_Chrome__find → "send message button"
mcp__Claude_in_Chrome__computer → left_click on ref
```

**Fallback — JavaScript:**
```javascript
const btn = document.querySelector('button[aria-label="Send message"]')
  || document.querySelector('button[data-testid="send-button"]');
if (btn) btn.click();
```

#### Step 6: Confirm Connectors Dialog (if present)
```javascript
const confirmBtn = Array.from(document.querySelectorAll('button'))
  .find(b => b.textContent.trim().startsWith('Confirm'));
if (confirmBtn) confirmBtn.click();
```

---

## Platform 2: Gemini Deep Research

### Core Concept

Gemini uses a **Quill editor** (`ql-editor`) with `[role="textbox"]`:
- Text injection works via `document.execCommand('insertText')` just like Claude.ai
- Deep Research is accessed via **Tools menu**, NOT the mode picker
- The mode picker (Pro/Fast/Thinking) does NOT contain Deep Research

### Automation Sequence (Per Tab)

#### Step 1: Create Tab
```
mcp__Claude_in_Chrome__tabs_create_mcp
```

#### Step 2: Navigate to Gemini
```
mcp__Claude_in_Chrome__navigate → https://gemini.google.com/app
```
Wait **3 seconds** for page to fully load.

#### Step 3: Insert Prompt Text

**Focus the Quill editor and insert text:**
```javascript
const editor = document.querySelector('.ql-editor[role="textbox"]');
editor.focus();
document.execCommand('insertText', false, "YOUR PROMPT TEXT HERE");
```

#### Step 4: Enable Deep Research

**CRITICAL: Deep Research is under the "Tools" button, NOT the mode picker.**

**Click the Tools button:**
```javascript
const toolsBtn = Array.from(document.querySelectorAll('button'))
  .find(b => b.textContent.trim().includes('Tools'));
if (toolsBtn) toolsBtn.click();
```

Wait **0.5 seconds** for the menu to render.

**Click the Deep Research menu item:**
```javascript
const items = document.querySelectorAll('[role="menuitemcheckbox"]');
const dr = Array.from(items).find(el => el.textContent.includes('Deep research'));
if (dr) dr.click();
```

**Verification:** After clicking, a blue "Deep research ×" tag should appear next to the
Tools icon in the input area. Sources and Files buttons also appear below the input.

#### Step 5: Submit the Prompt

**Click Send via JavaScript:**
```javascript
const sendBtn = document.querySelector('button[aria-label="Send message"]');
if (sendBtn) sendBtn.click();
```

**Or via find + ref click:**
```
mcp__Claude_in_Chrome__find → "Send message button"
mcp__Claude_in_Chrome__computer → left_click on ref
```

After submission, Gemini will show "Generating research plan" and present a research plan.

#### Step 6: Click "Start research" to Execute the Plan

**CRITICAL: Gemini Deep Research shows a research plan first and waits for confirmation.
If you don't click "Start research", it will only show the plan and NOT execute it.**

**Click Start research via JavaScript:**
```javascript
const startBtn = Array.from(document.querySelectorAll('button'))
  .find(b => b.textContent.trim() === 'Start research');
if (startBtn) startBtn.click();
```

**Timing:** The research plan takes **2–5 seconds** to generate after submission. You must
wait for the plan to render before clicking "Start research". Use a screenshot or a short
wait to confirm the button is present.

**Verification:** After clicking "Start research", Gemini will show progress indicators
like "Researching..." with a list of websites being searched. The "Start research" and
"Edit plan" buttons will disappear.

**If "Start research" is not found:** The tab may still be generating the plan. Wait 3–5
seconds and retry. If it still doesn't appear, take a screenshot to diagnose.

### Gemini Concurrent Research Limit

**CRITICAL: Gemini allows a maximum of 3 concurrent Deep Research requests.** If you
submit more than 3, Gemini will respond with "You have 3 research requests running right
now, which is the maximum I can do at one time." The excess tabs will NOT generate a
research plan or start research.

**Workaround for 7+ batches:**
1. Submit the first 3 batches (B1–B3) and click "Start research" on each
2. Wait for at least one to complete (~5–15 minutes) before submitting the next batch
3. Monitor tab titles — when a Gemini tab shows a descriptive title instead of
   "Generating research plan", it's likely complete
4. Repeat until all batches are processed

### Gemini Batch Optimization

For batches within the 3-concurrent limit, you can parallelize:
1. Insert text into all tabs first (parallel `javascript_tool` calls)
2. Click Tools → Deep Research on all tabs (parallel JS calls)
3. Click Send on all tabs (parallel JS calls)
4. Wait **5 seconds** for research plans to generate
5. Click "Start research" on all tabs (parallel JS calls)

---

## Platform 3: ChatGPT Deep Research

### Core Concept

ChatGPT uses a `[contenteditable="true"]` div with id `prompt-textarea`:
- Text injection works via `document.execCommand('insertText')`
- Deep Research / "Search" mode may be toggled via a search/research button
- The exact UI varies — screenshot first to identify the current layout

### Automation Sequence (Per Tab)

#### Step 1: Create Tab + Navigate
```
mcp__Claude_in_Chrome__tabs_create_mcp
mcp__Claude_in_Chrome__navigate → https://chatgpt.com
```

#### Step 2: Insert Prompt Text
```javascript
const editor = document.querySelector('#prompt-textarea')
  || document.querySelector('[contenteditable="true"]');
editor.focus();
document.execCommand('insertText', false, "YOUR PROMPT TEXT HERE");
```

#### Step 3: Enable Deep Research Mode

**Use find to locate the research/deep research toggle:**
```
mcp__Claude_in_Chrome__find → "Deep Research" or "Search" or "research toggle"
mcp__Claude_in_Chrome__computer → left_click on ref
```

If not found via find, screenshot and inspect the UI to locate the toggle.

#### Step 4: Submit
```javascript
const sendBtn = document.querySelector('button[data-testid="send-button"]')
  || document.querySelector('button[aria-label="Send prompt"]');
if (sendBtn) sendBtn.click();
```

---

## Batch Orchestration

When running multiple batches (e.g., B1 through B7) across platforms:

1. **Process one platform at a time** for reliability
2. **Parallelize within platforms** — insert text into all tabs first, then enable research
   mode on all, then send all
3. After all tabs are launched, inform the user how many are running per platform
4. Deep Research takes **5–15 minutes** per query to complete
5. Offer to check on tab progress later via screenshots

### Tab Reference Guide

Keep track of tab IDs per platform/prompt:

| Platform | B1 Tab | B2 Tab | B3 Tab | B4 Tab | B5 Tab | B6 Tab | B7 Tab |
|----------|--------|--------|--------|--------|--------|--------|--------|
| Claude   | ID     | ID     | ID     | ID     | ID     | ID     | ID     |
| Gemini   | ID     | ID     | ID     | ID     | ID     | ID     | ID     |
| ChatGPT  | ID     | ID     | ID     | ID     | ID     | ID     | ID     |

## Troubleshooting

### Research mode didn't activate (Claude.ai)
- **Symptom:** No blue swirl icon after toggle
- **Fix:** Let user manually toggle. Research mode via automation is unreliable on Windows.

### Deep Research not in Gemini mode picker
- **Symptom:** Only see Fast/Thinking/Pro in mode dropdown
- **Fix:** Deep Research is NOT in the mode picker. It's under **Tools** button → Deep research.
  This is a menuitemcheckbox in the Tools flyout menu.

### Text insertion failed
- **Symptom:** Editor appears empty after execCommand
- **Fix:** Ensure editor is focused first. Use `editor.focus()` immediately before
  `document.execCommand('insertText')` in the same JS call.

### Claude.ai DOM selectors break
Claude.ai's frontend evolves. Key selectors:
- `div.tiptap.ProseMirror` — editor container. Fallback: `[contenteditable="true"]`
- `button[aria-label="Toggle menu"]` — mode selector
- `[role="menuitemcheckbox"]` — toggle options in menu

### Gemini DOM selectors break
- `.ql-editor[role="textbox"]` — Quill editor. Fallback: `[contenteditable="true"]`
- `button[aria-label="Send message"]` — send button
- Tools menu items use `[role="menuitemcheckbox"]`

---

## Result Collection

After all Deep Research queries complete, collect results from each platform.

### Collecting Claude.ai Results

Claude.ai renders results in **artifact panels** (cross-origin iframes). Direct DOM access
is blocked.

**Extraction sequence (per tab):**
1. Scroll down to find the artifact card in the conversation
2. Click the artifact card to open the artifact panel
3. Use `find "Copy button next to Publish"` to locate the Copy button in the panel header
4. Click the Copy button ref
5. **Verify clipboard** via PowerShell:
   ```powershell
   (Get-Clipboard | Measure-Object -Character).Characters
   Get-Clipboard | Select-Object -First 3
   ```
6. Save to file:
   ```powershell
   Get-Clipboard | Out-File -FilePath '<city>/claude/B<N>.md' -Encoding utf8
   ```

**Key gotchas:**
- The artifact panel sometimes doesn't open on first click — click the card again
- Always verify clipboard content changed (compare character count to previous)
- Clear clipboard before each extraction: `Set-Clipboard -Value 'EMPTY'`

### Collecting Gemini Results

Gemini renders results inline in the chat as model response elements.

**Extraction sequence (per tab):**
```javascript
// Focus the page first (required for clipboard access)
document.querySelector('.conversation-container').click();

// Find the last large model response
const responses = document.querySelectorAll('[data-message-author-role="model"], .model-response-text, .markdown');
const report = Array.from(responses).filter(el => el.innerText.length > 500).pop();

// Copy to clipboard
navigator.clipboard.writeText(report.innerText);
```

Then verify and save via PowerShell (same as Claude).

### Collecting ChatGPT Results

ChatGPT Deep Research renders results in a **canvas** (cross-origin sandboxed iframe).
The "Copy response" button does NOT update the system clipboard. Use the select-all approach:

**Extraction sequence (per tab):**
1. Navigate to the conversation URL
2. Wait for page to load (3-5 seconds)
3. Scroll down to find the canvas/report preview
4. **Click directly on the report text** inside the canvas — this expands it to full-screen
5. Click on a text paragraph inside the expanded canvas to place focus
6. Press `Ctrl+A` to select all text (verify blue highlight in screenshot)
7. Press `Ctrl+C` to copy
8. Verify clipboard via PowerShell
9. Save to file

**Key gotchas:**
- The first click on the canvas opens it full-screen; a second click on the text places the cursor
- If `Ctrl+A` returns 0 chars, the cursor wasn't placed inside the editable area — click on text again
- Close the canvas (click X at top-left) before navigating to the next conversation
- **Navigation between ChatGPT conversations:** Use `javascript_tool` with `window.location.assign('URL')` — the `navigate` tool and address bar typing are unreliable due to ChatGPT's SPA routing
- After `location.assign`, wait 6-7 seconds and use F5 to reload if the page appears blank

### Navigation Pattern for ChatGPT Conversations

```javascript
// Reliable navigation between ChatGPT conversations
window.location.assign('https://chatgpt.com/c/<conversation-id>')
```

Wait 6-7 seconds for load. If page is blank, press F5 to force reload.

---

## Result Consolidation

After collecting all results, create consolidated per-platform documents.

### Per-Platform Documents

Create one document per platform containing all prompt results in sequence:

```bash
cd <repo>/<city> && {
echo "# <Platform> Deep Research Results — <City> Manufactured Home Moving (2026)"
echo ""
echo "---"
echo ""
for i in 1 2 3 4 5 6 7; do
  echo "## Prompt $i"
  echo ""
  cat "<platform>/B${i}.md"
  echo ""
  echo ""
  echo "---"
  echo ""
done
} > collated/<Platform>_All_Prompts.md
```

Repeat for each platform (ChatGPT, Claude, Gemini). This produces 3 files:
- `collated/ChatGPT_All_Prompts.md`
- `collated/Claude_All_Prompts.md`
- `collated/Gemini_All_Prompts.md`

### Cross-Platform Collation (Optional)

For each prompt B1-B7, create a comparison document in `collated/B<N>.md` with:
1. **Title & Overview** — what the prompt researched
2. **Comparison Table** — key data points: Gemini | Claude | ChatGPT columns
3. **Platform Summaries** — 4-5 bullets per platform on methodology/strengths
4. **Areas of Agreement** — consensus findings
5. **Areas of Divergence** — where estimates or approaches differ
6. **Recommended Data for LocalMovers.com** — actionable business picks

### Git Commit

After collection and consolidation:
```bash
git add <city>/chatgpt/ <city>/claude/ <city>/gemini/ <city>/collated/
git commit -m "Add <City> deep research results and consolidated documents"
git push
```

**Do NOT commit skill file changes** unless explicitly asked.

---

## User Preferences

- User prefers Chrome MCP tabs in a **new window**, not the current active window
- MCP tools can only create tabs within tab groups — tell user to right-click tab group →
  Move to new window if needed
