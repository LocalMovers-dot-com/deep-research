---
name: chrome-mcp-deep-research
description: >
  Automate launching Claude.ai Deep Research queries in browser tabs using the Chrome MCP
  and Mac control tools. Use this skill whenever the user wants to run deep research prompts
  in batch, launch multiple Claude.ai research tabs, automate Claude.ai browser interactions,
  paste prompts into Claude.ai via Chrome, or anything involving "deep research" combined with
  "Chrome MCP", "browser automation", "batch research", or "research tabs". Also trigger when
  the user says things like "run these research prompts", "open research tabs for each batch",
  "launch deep research on these topics", "paste my prompts into Claude", or "automate Claude.ai".
  Even if the user just says "run the deep research batches" or "kick off the research tabs",
  use this skill. Do NOT use for general web scraping, Puppeteer scripting, or non-Claude.ai
  browser automation.
---

# Chrome MCP Deep Research Tab Automation

Launch Claude.ai Deep Research queries across multiple browser tabs using the Chrome MCP and
Mac control MCP tools. This skill handles the full sequence: creating tabs, enabling Research
mode, pasting prompts, submitting, and confirming connector dialogs.

## Prerequisites

Before starting, verify:

1. **Chrome MCP tools** are connected (you need `tabs_create_mcp`, `navigate`, `screenshot`,
   `find`, `computer`, and `execute_javascript` from the Chrome MCP)
2. **Mac control tools** are connected (you need `osascript` from the Control your Mac MCP)
3. **Prompt files** exist at the expected path — default is `/tmp/deep-research-prompts/B*.txt`
   (one file per batch, e.g., `B1.txt`, `B2.txt`, ..., `B9.txt`)

If the user hasn't prepared prompt files yet, help them create the directory and save their
prompts before proceeding with the automation.

## Core Concept

Claude.ai uses a ProseMirror contenteditable `<div>` for its text editor, not standard
`<input>` or `<textarea>` elements. This means:

- The `form_input` tool **will not work** — always use the clipboard approach (`osascript` to
  load clipboard, then `cmd+v` to paste)
- The editor's vertical position varies per tab/session, so **never use hardcoded coordinates
  to click the text area** — always focus via JavaScript
- UI element positions shift when content is added, so prefer **JS DOM selectors and ref-based
  clicks** over coordinate clicks wherever possible

## Automation Sequence (Per Tab)

Execute these steps for each prompt batch. The reliable minimum is ~6 tool calls per tab,
achievable in ~10 seconds per tab.

### Step 1: Create Tab + Load Clipboard (parallel)

Run these two calls in the same turn — they're independent and can execute simultaneously:

```
mcp__Claude_in_Chrome__tabs_create_mcp
```

```
mcp__Control_your_Mac__osascript:
  set the clipboard to (read POSIX file "/tmp/deep-research-prompts/B{N}.txt" as «class utf8»)
```

Replace `{N}` with the current batch number.

### Step 2: Navigate to Claude.ai

```
mcp__Claude_in_Chrome__navigate → https://claude.ai/new
```

Wait **2 seconds** after navigation for the page to fully load. The editor and menu elements
must be present in the DOM before proceeding.

### Step 3: Enable Research Mode

This requires two sequential JavaScript executions with a pause between them.

**Open the toggle menu:**

```javascript
document.querySelector('button[aria-label="Toggle menu"]').click()
```

Wait **1 second** for the menu to render.

**Click the Research option via DOM selector:**

```javascript
const items = document.querySelectorAll('[role="menuitemcheckbox"]');
const research = Array.from(items).find(el => el.textContent.includes('Research'));
if (research) research.click();
```

Wait **2 seconds** for Research mode to fully activate. You'll know it's active when the blue
swirl icon appears next to the `+` button in the editor toolbar.

**Why JS selectors instead of coordinate clicks:** The menu item positions shift based on
window size, content state, and which options are available. The `[role="menuitemcheckbox"]`
selector with text matching is resilient to layout changes.

### Step 4: Focus Editor + Paste

**Focus the editor via JavaScript — never click coordinates:**

```javascript
document.querySelector('div.tiptap.ProseMirror').focus()
```

**Then paste from clipboard:**

```
mcp__Claude_in_Chrome__computer → key: cmd+v
```

The pasted content may appear as a collapsed block labeled "PASTED" — this is normal and
contains the full prompt text.

**Do not paste twice.** If the first paste appears to fail, take a screenshot to verify before
retrying. The collapsed block is easily mistaken for an empty editor.

### Step 5: Submit the Prompt

**Preferred approach — find + ref click (most reliable):**

```
mcp__Claude_in_Chrome__find → "send message button"
mcp__Claude_in_Chrome__computer → left_click on ref
```

**Fallback — JavaScript submit button click:**

```javascript
const btn = document.querySelector('button[aria-label="Send message"]')
  || document.querySelector('button[data-testid="send-button"]');
if (btn) btn.click();
```

Wait **4 seconds** after submission, then verify the URL has changed from `/new` to
`/chat/...`. If it hasn't, take a screenshot to diagnose.

### Step 6: Confirm Connectors Dialog

After the first research query submits, Claude.ai may show a connectors/tools confirmation
dialog. Dismiss it:

```javascript
const confirmBtn = Array.from(document.querySelectorAll('button'))
  .find(b => b.textContent.trim().startsWith('Confirm'));
if (confirmBtn) confirmBtn.click();
```

This dialog typically only appears on the first tab. Subsequent tabs may skip it, but always
attempt the confirmation — the `if (confirmBtn)` guard makes it safe to run every time.

## Batch Orchestration

When running multiple batches (e.g., B1 through B9):

1. **Process tabs sequentially** — each tab needs ~10 seconds
2. **Don't screenshot after every step** — only screenshot when something fails or the user
   requests verification
3. After all tabs are launched, inform the user how many tabs are running and that Deep
   Research takes 5–15 minutes per query to complete
4. Offer to check on tab progress later via screenshots

### Speed Optimization

The theoretical minimum per tab is 6 tool calls:

| Call | What |
|------|------|
| 1 | `tabs_create` + clipboard load (parallel) |
| 2 | `navigate` to claude.ai/new |
| 3 | JS: open menu + click Research (can combine with wait) |
| 4 | JS: focus editor + `cmd+v` paste |
| 5 | `find` send button + click ref |
| 6 | JS: confirm connectors dialog |

At ~10 seconds per tab, 9 tabs should complete in ~90 seconds.

## Troubleshooting

### Research mode didn't activate
- **Symptom:** No blue swirl icon after Step 3
- **Cause:** Menu item selector changed, or the click fired before the menu rendered
- **Fix:** Screenshot to verify menu state. Try increasing the wait to 2s after opening the
  menu. If the selector fails, screenshot the menu and adapt the selector text.

### Paste didn't land in the editor
- **Symptom:** Editor appears empty after Step 4
- **Cause:** Editor wasn't focused, or focus was lost between the JS call and the paste
- **Fix:** Re-run the focus JS, then immediately paste. Don't insert any other tool calls
  between focus and paste.

### Submit button didn't work
- **Symptom:** URL still shows `/new` after Step 5
- **Cause:** The send button may be disabled if the editor is empty (paste failed), or the
  ref click missed
- **Fix:** Screenshot to check editor state. If empty, re-paste. If content is present, try
  the JS fallback submit.

### Connectors dialog blocks research
- **Symptom:** Research appears stuck immediately after submission
- **Cause:** The confirmation dialog is waiting for user input
- **Fix:** Run the Step 6 JS. If the button text changed, screenshot and adapt.

### Claude.ai DOM selectors break
Claude.ai's frontend evolves. If selectors stop working:

- `div.tiptap.ProseMirror` — the editor container. Look for any `[contenteditable="true"]`
  div as fallback.
- `button[aria-label="Toggle menu"]` — the model/mode selector. May change aria-label; look
  for the button near the editor toolbar.
- `[role="menuitemcheckbox"]` — the toggle options in the menu. This is a standard ARIA
  pattern and less likely to change.

When adapting selectors, take a screenshot first, then use `execute_javascript` to probe the
DOM (e.g., `document.querySelectorAll('button').length` or dump button text content).

## Example: Full 9-Batch Run

User says: "Run deep research on all 9 batches"

```
For each N from 1 to 9:
  → Create tab + load /tmp/deep-research-prompts/B{N}.txt to clipboard
  → Navigate to https://claude.ai/new, wait 2s
  → JS: open toggle menu, wait 1s
  → JS: click Research menuitemcheckbox, wait 2s
  → JS: focus div.tiptap.ProseMirror
  → Key: cmd+v
  → Find "send message button" → click ref, wait 4s
  → JS: click Confirm button (if present)
  → Move to next batch
```

Total time: ~90 seconds for 9 tabs. Research results arrive in 5–15 minutes per tab.
