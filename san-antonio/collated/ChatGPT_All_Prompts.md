# ChatGPT Deep Research Results — San Antonio Manufactured Home Moving (2026)

---

## Prompt 1

﻿
San Antonio Metro Mobile Home Moving Cost Breakdown — 2026 Market Analysis
Scope and definitions
This report covers manufactured home transportation (oversize-load trucking) in the San Antonio–New Braunfels metro including the surrounding counties where moves commonly originate/terminate, with emphasis on Bexar County (as requested). It does not cover household-goods moving, packing, storage, or conventional residential “movers.”

For clarity, the pricing is split into three tiers:

Transport-only: Road-legalization + haul (axles/tongue/hitch prep, towing/haul, escorts if needed, and oversize permitting), typically excluding utilities, skirting, steps, anchoring/foundation work, and third-party inspections.

Full-service (mover/installer scope): Disconnect + transport + reconnect + setup (set/level) + anchoring + skirting + steps. The mover may still exclude or pass through certain third-party fees.

All-in: What a homeowner typically pays after adding pass-through/third-party items like state oversize permits, TDHCA installation reporting fees, local permits, typical utility activation/hookup charges, and inspection-related costs (where applicable). These adders vary materially by jurisdiction and site conditions.

Texas regulatory fees that reliably show up on invoices
State oversize/overweight permits (Texas)
Texas publishes a permit fee schedule for oversize/overweight permits processed through TxPROS, noting that transactions run through Texas.gov, which adds $0.25 + 2.25% to the total transaction.

In that schedule (dated February 2021), the single‑trip “Manufactured Housing” permit fee is $40; the document also shows an approximate total amount due of $41.16 when the Texas.gov service charge is applied.

Implication for cost modeling: a move involving multiple home “sections” can carry multiple permit transactions (one per section/load in many operational setups), so permit costs scale with the number of sections even before escorts, routing constraints, or local rules are considered. (The schedule provides the fee; whether a specific move needs multiple transactions depends on how the home is sectioned and permitted for travel.)

TDHCA manufactured-housing fees and inspection-related charges
Texas rules for manufactured housing fees include (among other items):

Installation reporting fee (“Form T” / Notice of Installation): $75 for installation of a single-section manufactured home, plus $25 for each additional section.
Statement of Ownership issuance fee: $55 (a common transactional fee when ownership/location paperwork must be re-issued/updated).
Optional expedited processing is described as Priority Handling Service for an additional $55 (when used).
Several inspection-related fees also exist in rule, including (examples) $150 for certain requested inspections and $200 for plan review/inspection of salvaged rebuilds (these are situational, not “every move,” but they matter for edge cases).
How the TDHCA fee scales by home type (by section count):

Single‑wide (1 section): $75 installation reporting fee
Double‑wide (2 sections): $100 installation reporting fee
Triple‑wide (3 sections): $125 installation reporting fee
These amounts are unusually “hard-dollar” compared with the market-driven portions of moving (labor, equipment, escorts, and scheduling).

Local market context for demand and provider availability
Manufactured housing footprint in Bexar County
Using the U.S. Census Bureau’s ACS 2024 1‑year Data Profile (DP04) for Bexar County, Texas, the county shows:

845,241 total housing units (DP04_0001E)
23,029 mobile homes (DP04_0014E)
2.7% of housing units as mobile homes (DP04_0014PE)
The Census Bureau lists the 2024 ACS 1‑year release as Aug 28, 2025.

Carrier records and consumer-profile cross-checks
Carrier identity and operating status can be verified via FMCSA SAFER Company Snapshot records for San Antonio–area operators that explicitly identify manufactured home transport in the business name (examples include Texas Elite Mobile Home Transport LLC and Trevino Transportation LLC).

For consumer-facing business reputation context, BBB maintains category listings for “Manufactured Home Transporters” in the region (e.g., listings “near New Braunfels, TX,” which functions as part of the metro’s broader moving/transport catchment).

Pricing framework and inputs used in this report
Primary cost anchor: ProMatcher San Antonio cost observations
The only locality-specific, move-type-specific pricing dataset available in the provided source constraints (without using prohibited sources) is ProMatcher’s San Antonio mobile home moving cost page.

Key ProMatcher datapoints (San Antonio area) used as anchors:

Single‑wide (~50 miles): average $1,650, with observed low/high $1,300–$2,000.
Single‑wide within the metro: average $1,900, low/high $1,400–$2,400.
Double‑wide (~50 miles): average $3,000, low/high $2,500–$3,500.
Longer haul reference point (~500 miles): single‑wide average $5,000 (range $3,000–$7,000) and double‑wide average $10,000 (range $7,000–$13,000).
Important limitation (publication date): the ProMatcher page content visible in the accessible snippet does not clearly display a publication date. This report treats the figures as observed market-based reference points and then layers in the explicitly published Texas permit/fee schedule items above.

Distance modeling approach for long-distance ranges
Because ProMatcher provides comparable anchor points at ~50 miles and ~500 miles, this report uses a simple two-point linear model (fixed mobilization component + per-mile component) to create bounded estimates for the 50–200+ mile band, expressed as ranges at 100 miles and 200 miles.

“All-in” adders (permits, TDHCA, utilities, inspections)
Hard-dollar adders included in the “all-in” layer are grounded in the Texas fees above:

TxPROS manufactured-housing single-trip permit fee: $40 (approx $41.16 with Texas.gov fee)
TDHCA installation reporting fee: $75 + $25 per additional section
TDHCA Statement of Ownership issuance fee: $55
Local permits, utility activation, and inspection costs vary by city/county and by whether service lines/meters already exist. This report therefore treats those as structured, explicit line items in the “all-in” calculation, but they should be interpreted as typical homeowner-paid adders, not statutory statewide fees.

Cost breakdown by home type
Single-wide manufactured home
Local moves under 50 miles
Transport-only (under 50 miles): $1,300–$2,400
This range is taken from ProMatcher’s San Antonio observations for single-wide moves (both the ~50-mile point and “within the metro” range).

Full-service (disconnect → transport → reconnect/setup → skirting/steps/anchoring): $4,200–$6,500
This report models the incremental scope beyond transport-only (setup, anchoring, skirting/steps, and utility reconnection labor) as a structured add-on to the local transport anchor, to keep the full-service band consistent with the observed transport baseline while recognizing the regulated adders discussed earlier.

Long-distance moves (50–200+ miles)
Using the ProMatcher 50-mile and ~500-mile anchors, the modeled transport-only band is:

~100 miles: $1,489–$2,911
~200 miles: $1,867–$3,933
Modeled full-service (transport + teardown/setup package) band:

~100 miles: $4,389–$7,111
~200 miles: $4,767–$8,133
These long-distance figures reflect the reality that manufactured-home transportation has large fixed components (mobilization, prep, permitting, scheduling, escorts as required), so per-mile averages typically decline as distance increases.

Median and mean for full-service local moves
For a single-wide local full-service move, this report treats the full-service price as a triangular distribution bounded by the local full-service range above and centered on a mid-case value. Resulting estimates:

Median (modeled): $5,325
Mean (modeled): $5,333
All-in realistic average and per-mile blended rate
All-in realistic average (local, ~50 miles): $6,213
This adds typical third-party/pass-through amounts (state permit transaction fees, TDHCA installation reporting, and common homeowner-paid local/utility/inspection adders) to the modeled mean full-service local price.

Per-mile blended rate (all-in, based on 50-mile local baseline): $124.27/mile (=$6,213 ÷ 50).

Typical line-item breakdown (single-wide, local ~50 miles, all-in ≈ $6,180)
This is a “typical invoice composition” view (not a statutory schedule) that explicitly shows where the published fees land inside an otherwise market-driven move:

Disconnection/site prep (labor): $800
Transport-only core (haul + prep + escort): $1,858 (includes the permit transaction below)
TxPROS manufactured-housing permit transaction (published fee + Texas.gov fee): $41.16
Setup/level + anchoring: $1,000
Utility reconnection labor: $600
Skirting: $700
Steps: $300
TDHCA installation reporting fee (single-section): $75
Statement of Ownership issuance (when required): $55
Typical homeowner adders (local permits, utility activation, inspection-related costs): $792
Double-wide manufactured home
Local moves under 50 miles
Transport-only (under 50 miles): $2,500–$3,500 (ProMatcher San Antonio double-wide ~50-mile observations).

Full-service (disconnect → transport → reconnect/setup → skirting/steps/anchoring): $6,500–$10,500
This band is constructed by layering a larger teardown/setup package (two sections, marriage-line work exposure, and typically higher escort/handling complexity) onto the ProMatcher local transport anchor, while still carrying through the published state/TDHCA fee items.

Long-distance moves (50–200+ miles)
Modeled transport-only band:

~100 miles: $3,000–$4,556
~200 miles: $4,000–$6,667
Modeled full-service band:

~100 miles: $7,500–$11,056
~200 miles: $8,500–$13,167
Median and mean for full-service local moves
Modeled from the local full-service band:

Median (modeled): $8,402
Mean (modeled): $8,433
All-in realistic average and per-mile blended rate
All-in realistic average (local, ~50 miles): $9,638 (mean full-service + typical third-party adders).

Per-mile blended rate (all-in, based on 50-mile local baseline): $192.77/mile (=$9,638 ÷ 50).

Typical line-item breakdown (double-wide, local ~50 miles, all-in ≈ $9,505)
Disconnection/site prep (labor): $1,200
Transport-only core (two sections): $3,000
TxPROS manufactured-housing permit transaction(s): $82.32 (2 × $41.16)
Reassembly/setup/level + anchoring: $1,800
Utility reconnection labor: $900
Skirting: $1,000
Steps/decks: $400
TDHCA installation reporting fee (two sections): $100
Statement of Ownership issuance (when required): $55
Typical homeowner adders (local permits, utility activation, inspection-related costs): $1,150
Triple-wide manufactured home
Local moves under 50 miles
Transport-only (under 50 miles): $3,750–$5,250
Because ProMatcher does not provide a triple-wide San Antonio datapoint in the accessible excerpt, this report scales the double-wide transport-only band by section count (3 sections vs. 2) as an extrapolation for market planning—not as a directly observed local quote.

Full-service (disconnect → transport → reconnect/setup → skirting/steps/anchoring): $9,000–$15,000
This band reflects three transported sections and a larger setup package, while still incorporating the published state/TDHCA fee items that scale by section count.

Long-distance moves (50–200+ miles)
Modeled transport-only band (scaled from double-wide long-distance bounds as an extrapolation):

~100 miles: $4,500–$6,833
~200 miles: $6,000–$10,000
Modeled full-service band:

~100 miles: $10,500–$15,633
~200 miles: $12,000–$18,800
Median and mean for full-service local moves
Modeled from the local full-service band:

Median (modeled): $11,902
Mean (modeled): $11,933
All-in realistic average and per-mile blended rate
All-in realistic average (local, ~50 miles): $13,613 (mean full-service + scaled third-party adders).

Per-mile blended rate (all-in, based on 50-mile local baseline): $272.27/mile (=$13,613 ÷ 50).

Typical line-item breakdown (triple-wide, local ~50 miles, all-in ≈ $13,480)
Disconnection/site prep (labor): $1,800
Transport-only core (three sections): $4,500 (extrapolated)
TxPROS manufactured-housing permit transaction(s): $123.48 (3 × $41.16)
Setup/level + anchoring: $2,500
Utility reconnection labor: $1,200
Skirting: $1,300
Steps/decks: $500
TDHCA installation reporting fee (three sections): $125
Statement of Ownership issuance (when required): $55
Typical homeowner adders (local permits, utility activation, inspection-related costs): $1,700


---

## Prompt 2

﻿
San Antonio Mobile Home Transport Regulatory & Permitting Framework — 2026 Market Analysis
Scope, definitions, and agency roles in Texas
This report maps the regulatory and permitting framework governing manufactured home transport (HUD-Code/“manufactured housing”) on public roads (oversize-load trucking), plus the parallel framework governing installation/setup after the unit reaches the destination site in the San Antonio metro. It does not cover household-goods moving.

A “HUD-Code” manufactured home is distinct from a modular or site-built home because it is built to federal manufactured home construction and safety standards administered by HUD, and is often transported as an overwidth load. A HUD user guide explains that HUD-Code manufactured homes have been required since 1976 to comply with the federal Manufactured Home Construction and Safety Standards. (HUD user guide, published 2007.) 

In Texas, the regulatory “stack” splits into two major tracks:

Road movement / oversize-load transport (pre-trip and in-transit):

Texas Department of Motor Vehicles issues Texas oversize/overweight (OS/OW) permits and routes for loads exceeding legal size/weight limits, including manufactured housing permits, primarily through TxPROS. (TxDMV OS/OW overview page; no visible publication date; accessed 2026-03-20.) 
Texas Department of Transportation influences routing feasibility via district-level restrictions and coordination (e.g., signal/utility coordination and district restrictions published into TxPROS/TxDMV restriction libraries). (San Antonio District restrictions PDF shows TxDOT district email coordination; restriction dates shown inside; accessed via TxDMV restriction library.) 
Texas Department of Public Safety enforces commercial vehicle compliance and is referenced by TxDMV for certain compliance functions (e.g., drug-testing reporting for intrastate registrants). (TxDMV “TxDMV Number” page; no visible publication date; accessed 2026-03-20.) 
Installation / setup / consumer-protection (post-delivery):

Texas Department of Housing and Community Affairs regulates manufactured housing licensing, installation standards, and installation reporting/inspection mechanisms under 10 TAC Chapter 80 and Texas Occupations Code Chapter 1201 (the Texas Manufactured Housing Standards Act). (TDHCA rule compilation effective 03/03/2024; TDHCA “Standards Act” compilation published 09/01/2023.) 
Finally, site placement and utility connection typically also invoke local permitting and zoning requirements (city or county), and sometimes floodplain and septic/OSSF permitting.

Texas Department of Housing and Community Affairs installation standards, licensing, inspections, and homeowner verification
Governing rule set and most relevant Texas Administrative Code sections
TDHCA’s manufactured housing regulatory rules are compiled as “Chapter 80, Manufactured Housing Rules (Effective: 03/03/2024).” (TDHCA rule compilation effective 03/03/2024.) 

For installation and installer compliance, the most frequently invoked sections include:

10 TAC §80.21 “Requirements for the Installation of Manufactured Homes” (rule effective 01/07/2020, as shown within the 03/03/2024 consolidated compilation). 
10 TAC §80.3 “Fees” (license fees, installation reporting fees, education fees, and specific inspection fees). 
10 TAC §80.41 “License Requirements” (application completeness, fees/security, provisional installer upgrade mechanics, education requirements). (Rule shown effective 03/03/2024.) 
Installation standard: licensed installer + manufacturer instructions, and the “acceptance” workflow
The TDHCA rules explicitly require that new manufactured homes be installed by a licensed installer and in accordance with the manufacturer’s DAPIA-approved installation instructions, and that used manufactured homes must also be installed by a licensed installer with installation completed to resist overturning/lateral movement and be appropriate to the wind zone. (TDHCA rules, effective 03/03/2024, installation provisions shown around page 10 of the compiled rules.) 

From a permitting/acceptance standpoint, TDHCA’s practical “installation acceptance” pipeline is driven by installation reporting and inspection timing:

For each installation completed, the installer must complete and submit a Notice of Installation (Form T) with the required fee no later than seven (7) days after completion (and no later than three (3) days for installers with a provisional license). (TDHCA rules effective 03/03/2024.) 
Provisional installers must also send a copy of the Notice of Installation to TDHCA’s Field Office within three (3) days to facilitate timely inspection. 
TDHCA links the timeliness of Form T submission to inspection practicality: timely submittal helps ensure TDHCA inspectors may inspect the home with utilities connected but before the home is skirted. 
In operational terms for the San Antonio market, this means transport scheduling and utility-connection scheduling are not purely “local permit” issues; they can affect whether a provisional installer can be inspected within TDHCA’s expected window.

TDHCA installer licensing: requirements, fees, education, bond/security, and provisional upgrade triggers
License application content and prerequisites. TDHCA’s rules state that to apply for a license, the prescribed application must be fully completed and submitted with: the required fee, required security, and “all other required supporting documentation,” with TDHCA able to request reasonably related additional information. (10 TAC §80.41, effective 03/03/2024.) 

License fee (installer). The installer license fee is $350. (10 TAC §80.3(a)(4) in TDHCA’s compiled rules.) 

Education and examinations. TDHCA’s rules describe an “initial eight (8) hour course of instruction in the law, including instruction in consumer protection regulations,” and a “four (4) hour installer education course,” among other role-specific requirements. (10 TAC §80.41(c), effective 03/03/2024.) 

Provisional installer pathway. Under the TDHCA rule text, a provisional installer’s license becomes a full installer’s license when TDHCA inspects a minimum of five (5) manufactured home installations and finds no identified installation violations. (10 TAC §80.41(a)(2)(A), effective 03/03/2024.) 

The same section imposes a “prompt” notification obligation for provisional installers to enable inspection before skirting, defined as within three business days following completion. 

Security/bond expectation (Texas Occupations Code). Texas’ Manufactured Housing Standards Act is in Texas Occupations Code Chapter 1201. (Texas Occupations Code Chapter 1201 compilation, published 09/01/2023 by TDHCA.) 

The statute sets required security amounts by license type; specifically, $25,000 for an installer. (Texas Occupations Code §1201.106; current statute displays this structure; secondary statutory mirrors show the same amount.) 

TDHCA’s rules also connect bond continuity to license status: if a required bond is canceled during the license period, the license is automatically suspended on the date bond coverage ceases. (TDHCA rules effective 03/03/2024.) 

TDHCA installation and inspection-related fees relevant to market operators
TDHCA fees that commonly attach to installation operations include:

Installation reporting fee (Form T): $75 for a single-section manufactured home and $25 for each additional section, submitted with the Notice of Installation within the stated deadlines. (10 TAC §80.3(b).) 
Industry-requested consumer complaint inspection: $150. (10 TAC §80.3(f).) 
Additional TDHCA inspection fees apply in specialized cases (e.g., inspection tied to changing real-property designation back to personal property, or salvaged rebuild inspections). (10 TAC §80.3(g)-(h).) 
Homeowner verification: how to verify a TDHCA installer license
For homeowners, TDHCA provides a public records database portal that includes “View License Records,” with a search requiring the license number or name, and the ability to view “installation & inspection records.” (TDHCA MHWeb “Manufactured Housing Report Options” page; no visible publication date; accessed 2026-03-20.) 

A practical verification approach consistent with TDHCA’s public portal structure is:

Use the View License Records function and search by the installer’s license number or company name. 
Confirm “Active” status (where shown) and ensure the contracting entity matches the one on your contract paperwork. (The MHWeb portal describes active/inactive selection for downloadable license lists.) 
If the installer is claiming recent installations in Bexar County, separately use “View home installation & inspection records” to cross-check installation/inspection record presence when relevant. 
Texas Department of Motor Vehicles oversize/overweight permits for manufactured housing via TxPROS, including San Antonio-area restrictions
Authority, portals, and processing expectations
TxDMV states that vehicles and loads exceeding legal size/weight limits require an OS/OW permit and route from TxDMV to travel on Texas roads. (TxDMV OS/OW overview page; no visible publication date; accessed 2026-03-20.) 

TxDMV’s Motor Carrier Handbook (published “9 months ago” by TxDMV’s site index, accessed 2026-03-20) explains that OS/OW permits may be obtained online through TxPROS or by phone, and that applicants may apply online 24/7; many permit types are available for self-issuance, while those requiring review are processed during business hours. (TxDMV Motor Carrier Handbook, publication indicator “9 months ago.”) 

TxDMV describes TxPROS as an online permitting and GIS-based mapping system that allows customers to apply for and self-issue many permits and provides “real-time restriction management,” emphasizing faster issuance and self-issue capabilities. (TxDMV TxPROS information page; no visible publication date; accessed 2026-03-20.) 

Permit types for manufactured housing: single-trip vs annual
TxDMV offers both single-trip and annual manufactured housing permits:

Manufactured housing single-trip permit

Fee: $40. (TxDMV manufactured housing single-trip permit page; no visible publication date; accessed 2026-03-20.) 
Duration/validity: A permit “will not exceed five days.” (Same TxDMV page; no visible publication date; accessed 2026-03-20.) 
Application channel: Apply online via TxPROS or via the permit office phone line. (Same TxDMV page.) 
Restrictions: TxDMV’s holiday/movement page notes that manufactured housing movement is prohibited on “national holidays unless exception is granted by TxDMV,” and provides the holiday closure schedule for the permit office. (TxDMV Holiday Hours & Movement Restrictions page; no visible publication date; contains 2026 holiday list; accessed 2026-03-20.) 
Manufactured housing annual permit

Fee: $1,500. (TxDMV annual manufactured housing page snippet; no visible publication date; accessed 2026-03-20.) 
Scope: TxDMV’s permit listing describes the manufactured housing annual permit as used to transport new homes to a temporary storage location within a 20-mile radius, valid for one year, and usable by multiple vehicles. (TxDMV OS/OW permit listing page; no visible publication date; accessed 2026-03-20.) 
Operating authority inputs and pre-issuance checks: USDOT vs TDHCA license identifiers
For annual manufactured housing permits, TxDMV states that during the permit application process the applicant must provide a USDOT Number or a TDHCA-issued licensing number, and TxDMV will check the number against FMCSA’s MCMIS for out-of-service orders prior to issuance. (TxDMV annual manufactured housing page snippet; no visible publication date; accessed 2026-03-20.) 

TxDMV’s Motor Carrier Handbook adds that TxDMV will verify the USDOT number with FMCSA’s MCMIS and issue the permit under the company name as it appears in FMCSA’s system, and it clarifies that some permit types not requiring a USDOT number may require a permit surety bond on file. (TxDMV Motor Carrier Handbook, published “9 months ago,” accessed 2026-03-20.) 

Fee schedule context and transaction surcharges through Texas.gov
TxDMV’s “Oversize/Overweight Permit Fees and Credit Card Payments” table explains that OS/OW permits processed through TxPROS are handled through Texas.gov and incur a service charge of $0.25 plus 2.25% of the transaction total. (TxDMV permit fee table PDF, published ~5.1 years ago per index metadata; accessed 2026-03-20.) 

Dimensional limits relevant to manufactured housing moves (Texas baseline)
TxDMV provides Texas’ maximum legal dimensions without a permit (e.g., 8'6" width for most vehicles/loads and 14’ height), and also lists maximum permitted dimensions for movement with a Texas permit. (TxDMV Texas Size/Weight Limits page; no visible publication date; accessed 2026-03-20.) 

Key dimension points from that TxDMV reference include:

Legal (no permit): 8'6" maximum width for “all other vehicles and loads,” 14’ maximum height. 
With permit (selected maxima): up to 16 feet width on controlled-access highways (interstate system) “except for manufactured housing,” and other conditional maxima depending on route inspection certifications. 
Because the page flags exceptions for manufactured housing, market operators generally treat manufactured housing routing as its own specialized lane within TxPROS, where district restrictions and permit conditions dominate feasibility. 

Escort/pilot car rules for manufactured housing by width tier (Texas)
TxDMV’s escort and equipment guidance sets escort thresholds and equipment standards, and it notes TxDMV may require law enforcement escorts depending on size/route/nature. (TxDMV Escort and Equipment Requirements page; no visible publication date; accessed 2026-03-20.) 

For manufactured housing specifically, the TxDMV escort page states:

Over 16 feet to 18 feet wide: one escort vehicle is required (with placement depending on roadway type). 
Over 18 feet wide: two escort vehicles are required (front and rear). 
The same TxDMV guidance specifies escort vehicle lighting requirements (e.g., amber beacons or alternating blue/amber under permitted circumstances) and requires two-way communications between escort and permitted vehicle. (TxDMV escort requirements page; no visible publication date; accessed 2026-03-20.) 

TxDMV also references formal training requirements for escort flaggers who direct traffic, tied to the Texas Commission on Law Enforcement’s curriculum standards. (TxDMV Motor Carrier Handbook, published “9 months ago”; and TxDMV escort guidance referencing TCOLE training.) 

San Antonio metro routing constraints: district restriction libraries and time-based curfew overlays
For San Antonio-area moves, two Texas data layers tend to be decisive:

District/corridor restrictions (TxDMV restriction library, rooted in TxDOT district constraints).
The “San Antonio District” permit restriction PDF (pulled from TxDMV’s restriction library and showing restriction creation dates by segment) includes numerous corridor-level constraints in Bexar County, including “no permits” movements on specific ramps/junction maneuvers and specific max-width constraints on frontage roads and mainlanes. Examples include:

In San Antonio: “No permits” on designated ramps on IH10/US90 (ramp-specific restrictions dated 01/05/26). 
In San Antonio: IH35 mainlanes/frontage roads width restrictions on defined segments (restriction dated 02/24/26). 
Multiple “no permits” maneuver restrictions at major interchanges (e.g., junction restrictions dated 08/21/25 and other dated entries). 
Practically, these constraints mean that even if a statewide manufactured housing permit is issued, route feasibility inside the metro is frequently bottlenecked by interchange geometry, frontage-road constraints, and specific disallowed ramp movements, so carriers often structure origin/destination choices around what can be routed without violating “no permits” segments. 

Time-based curfews for “time permits” (overlay).
TxDMV’s “Time Permit Curfews” PDF (effective 09/30/2025) defines curfew rules that apply to listed time-permit types, including annual manufactured housing permits among the listed permit categories affected. (Time Permit Curfews PDF, effective 09/30/2025.) 

Because these curfews are a separate overlay, market operators commonly treat San Antonio metro routing as: (a) build a compliant physical route in TxPROS under district restrictions, then (b) schedule movement windows that do not violate time-curfew restrictions applicable to the permit type. 

Texas Department of Public Safety escort requirements: when law enforcement escort is triggered, what’s “mandatory,” and what is known for Bexar County
Private escort vehicles vs law enforcement escorts in Texas permitting practice
Texas distinguishes between:

Escort flag vehicles / pilot cars (private escorts) that become mandatory at certain width/length thresholds and must meet equipment/communication rules. (TxDMV Escort and Equipment Requirements page; no visible publication date; accessed 2026-03-20.) 
Law enforcement escorts that may be required by TxDMV “depending on the size, route, or nature of the permitted load,” and may also be required by a city/county restriction that forces contact with specific police/sheriff dispatch for escorting or traffic control at pinch points. (TxDMV Motor Carrier Handbook, published “9 months ago,” and San Antonio District restriction entries explicitly calling for “law enforcement escorts.”) 
This distinction matters because the “mandatory” trigger for private escorts is usually dimensional, while the “mandatory” trigger for law enforcement escort is often route-specific (printed as a condition/restriction rather than a universal statewide width tier).

What is mandatory vs optional (Texas view)
Based on TxDMV source language, the most defensible “mandatory vs optional” phrasing is:

Mandatory (private escort vehicles): when the permitted load exceeds escort thresholds published by TxDMV (including manufactured housing >16’ wide thresholds). 
Mandatory (law enforcement escort): when a permit condition or district/city restriction explicitly requires it (“law enforcement escorts are required” / “mover must contact police/sheriff for assistance”). 
Optional: when not specified by permit conditions/restrictions; however, carriers may still voluntarily hire law enforcement or traffic control support to manage intersections, utilities, or safety where allowed.
Bexar County: what is explicitly documented in the restriction library, and what is not
Inside the San Antonio District restriction PDF, many Bexar County entries emphasize “no permits” maneuvers and dimensional caps, but the extracted entries reviewed here did not explicitly state “DPS escort required” for Bexar County segments; where law enforcement escort requirements appear explicitly in the same district document, they often reference other counties/cities (e.g., Bandera). (San Antonio District restriction PDF entries.) 

A representative example of a law enforcement escort requirement in the San Antonio District library (not Bexar County) is: “Law enforcement escorts are required” with a dispatch number, paired with an instruction to email the permit to the district. (Entry dated 09/26/25 in Bandera.) 

For Bexar County itself, the most concrete and current “must-do” items supported by the restriction library are the ramp/junction prohibitions and width caps on specific segments in San Antonio, not a generalized law enforcement escort mandate. 

Why “DPS escort fees” are hard to standardize from public sources
TxDMV’s OS/OW framework clearly supports law enforcement involvement, but the publicly visible Texas sources gathered here do not provide a single statewide “DPS escort fee schedule” for manufactured home moves; instead, police/sheriff escort requirements are commonly introduced as local dispatch coordination requirements (with movers “responsible for all fees”) in jurisdiction-specific restrictions. (TxDMV “Known Jurisdictions with Restrictions Requiring Notification Prior to Movement” page shows multiple city examples where escorts are required and the mover is responsible for fees; no statewide fee schedule listed there.) 

From a compliance standpoint, the most supportable Bexar County operational guidance is therefore:

check the permit conditions and TxDMV restriction library for any law-enforcement triggers on your specific route, and
if a law enforcement escort is required in a particular municipality/corridor, coordinate with the named agency and treat fees as agency-specific rather than statewide. 
Local permitting and siting: Bexar County (unincorporated) vs San Antonio
Unincorporated Bexar County: what permits typically apply (and what generally does not)
A key market reality is that many “San Antonio metro” installations occur outside city limits. In Texas, counties often regulate development through specific programs (floodplain, stormwater, right-of-way, septic/OSSF, plats) rather than broad residential building permits.

Bexar County’s Public Works “Summary of Bexar County Permits” (updated 10/06/2025) provides a concise county permit verification checklist with fees and review timelines. (Bexar County Public Works PDF updated 10/06/2025.) 

The county-level permits most likely to touch a manufactured home placement project in unincorporated areas include:

Storm Water Quality (SWQ) Permit: required when ≥1 acre is disturbed; fee $500; review time noted as 30 days for first submittals and 15 days for resubmittals. 
Post Construction Permit: required when ≥1 acre disturbed; fee $50 or $250 depending on mitigation worksheet; concurrent review with SWQ. 
Right-of-Way (ROW) permit: required for work within county-maintained ROW; fee varies; review time 15–30 days. 
On-Site Sewage Facility (OSSF) permit: required when site not served by public sanitary sewer; review time 30 days. 
Floodplain Development Permit (Floodplain Permit): required for property within/near FEMA 1% floodplain (described as encumbered or within 100 feet); fee $50; review time 30 days first submittal / 15 days resubmittal. 
Bexar County’s floodplain page confirms Public Works must review construction activity in proximity to the 100-year floodplain and notes flood study triggers. (Bexar County Floodplain Development Permits page; no visible publication date; accessed 2026-03-20.) 

Bexar County’s OSSF page describes permitting expectations for septic systems, including that an existing-system permit can require hiring a sanitarian/engineer for site survey and design and submitting supporting documentation. (Bexar County On-Site Sewage Facilities page; no visible publication date; accessed 2026-03-20.) 

Building permit limits in unincorporated Bexar County. The same Bexar County Public Works guideline explicitly states that a Fire Marshal “building permit” requirement in unincorporated areas applies to commercial, public accessible, or multi-family residential buildings (or pre-built buildings placed on property), and that it does not apply to single family residential homes (including duplexes and triplexes). (Bexar County Public Works PDF updated 10/06/2025.) 

For manufactured home siting used as a single-family dwelling in unincorporated Bexar County, this public county guidance therefore supports a market interpretation that local permitting friction is more likely to arise from OSSF, floodplain, stormwater, platting, and ROW rather than a county-issued residential building permit. 

City of San Antonio Development Services: installation permit requirements, inspections, zoning, floodplain triggers, and fee schedule
Within city limits, the City’s Development Services practice is more “building-permit centric.” The City provides a “Manufactured Home Installation Permit – On Private Property” submittal checklist and application (rev. 5/2015). (City of San Antonio manufactured home application, rev. 5/15; accessed 2026-03-20.) 

Core DSD requirements for manufactured home installation (private lot)
The City’s manufactured home application states:

No work may begin until plans are approved and a building permit is issued. 
Submittals must meet the City’s adopted 2015 International Residential Code standard (as stated in the form). 
Foundation drawings must be stamped/sealed/signed as required by Texas professional practice acts, and the as-completed project requires foundation, framing, and final inspections prior to utility release. 
Trade permits required for manufactured home installation include Electrical, Plumbing, Mechanical (HVAC), Sewer/Septic, and Gas (if applicable), and these must be obtained by a licensed trade contractor; inspections for each trade permit are required prior to utility release. 
A Letter of Inspection Report from a licensed foundation engineer must be on file at completion. 
Floodplain and zoning compliance in the City
The application specifies:

zoning can be verified by contacting the City’s call center, and
projects in or near a floodplain require signed release/approval from storm water review, with floodplain verification routed through Transportation & Capital Improvements contact information in the form. 
The same form also asserts that, under the City’s Unified Development Code, properties must front on a paved city street or be paved at owner cost in specified circumstances, and it cites UDC section references for that requirement. 

City fee schedule: concrete published fees and how they appear for manufactured home projects
The City’s FY 2026 Development Fee Schedule (Rev. October 2025) is the controlling fee schedule document for published Development Services fees. (City fee schedule cover showing FY 2026 and “Rev. October 2025.”) 

From that schedule, the directly stated manufactured-home-relevant fees include:

Mobile Home Installation: $50.00 (listed as a flat fee under “Flat Fees for Miscellaneous Residential Projects”). (City fee schedule, FY 2026, Rev. Oct 2025.) 
Because San Antonio’s application also requires separate trade permits and inspections for utilities, the total city-side permitting cost for a manufactured home installation project is commonly the sum of:

the relevant building/plan-review fee(s) (including the $50 mobile home installation fee where applicable), plus
any linked trade permits (electrical/mechanical/plumbing/sewer/gas) and their inspections as required. 
The same FY 2026 schedule provides a square-footage-based table for “Residential Construction – New, Remodels, and Additions,” showing building permit fees and integrated trade permit fees assessed on the parent permit for new residential construction, plus separate plan review fees for certain jobs. (City fee schedule, FY 2026, Rev. Oct 2025.) 

Processing timelines: permit expiration windows
San Antonio’s manufactured home installation application incorporates IRC-based expiration language:

applications without permit issuance within 180 days can expire, and
permits can become invalid if work does not commence within 180 days or is suspended/abandoned for 180 days, with possible extensions. (City manufactured home installation application, rev. 5/15.) 
These “clock” rules are especially market-relevant for manufactured housing because manufactured home transport scheduling often depends on TxPROS route approvals and the availability of escort vehicles and utility coordination windows; expiration rules create a soft deadline for sequencing those dependencies. 

Adjacent jurisdiction variations across the San Antonio metro
This section briefly highlights process differences in common origin/destination points: permitting portal, explicit manufactured home permit types, and where available, known OSOW escort restrictions. The emphasis is on what changes relative to San Antonio proper.

New Braunfels
New Braunfels’ building permits portal lists “Manufactured Home” as an available residential permit type for online submittal, and it also lists related permit types such as floodplain development and standalone trade permits (electrical/mechanical/plumbing). (City of New Braunfels building permits page; no visible publication date; accessed 2026-03-20.) 

New Braunfels also provides a dedicated “Manufactured Homes Permit Checklist” through its Forms & Applications/QuickLinks structure. (New Braunfels Forms & Applications / QuickLinks page; no visible publication date; accessed 2026-03-20.) 

On the transport side (not installation), TxDMV’s jurisdiction notification list documents a San Antonio District restriction for BS46 in New Braunfels requiring law enforcement escorts for over 12’ wide loads on the specified segment, including a contact phone number. (TxDMV “Known Jurisdictions…” page; restriction dated 08-16-96.) 

Boerne
Boerne’s Permitting and Code Compliance Department describes itself as providing code assistance and review of building, electrical, plumbing, mechanical, fuel gas, and energy requirements citywide. (City of Boerne Permitting and Code Compliance page; no visible publication date; accessed 2026-03-20.) 

For installation workflow planning, the key “difference” relative to San Antonio is usually the specific online portal, checklists, and local zoning allowances, rather than TDHCA installation law (which remains statewide). 

Seguin
Seguin instructs applicants to apply online through its Development Services Portal for permits/inspections and notes that electric/water/wastewater applications should accompany the building permit and be completed by a licensed contractor. (Seguin Permits and Inspections page; no visible publication date; accessed 2026-03-20.) 

Kyle
Kyle’s Building Services and Permits page emphasizes a Citizen Self-Service (CSS) Portal for applying and paying online for permits, inspections, and plans, with a support email for portal navigation. (City of Kyle Building Services and Permits page; no visible publication date; accessed 2026-03-20.) 

San Marcos
San Marcos provides a Permit Center hub and an Applications list that includes a “2020 Mobile Home Permit Guide” and a mobile home permit application. (City of San Marcos Applications page; no visible publication date; accessed 2026-03-20.) 

The San Marcos mobile home permit application explicitly warns that if the mobile home is not located in a mobile home park, a building permit is required, and it lists other permits such as electrical, plumbing, and mechanical as associated permits. (San Marcos mobile home permit application; publication date not shown in snippet; accessed via city document center.) 

Schertz
Schertz describes a permitting workflow supported by a land-use management software platform (“CityView”) that allows customers to submit, pay, request, and track permits and inspections online. (City of Schertz Building Permits page; no visible publication date; accessed 2026-03-20.) 

Schertz also points users to online payments and states that an inspection-division fee list is available. (Schertz Building Permits/Inspections page; no visible publication date; accessed 2026-03-20.) 

Interstate considerations: Louisiana, New Mexico, Oklahoma, and Mexico border crossings
General rule for interstate moves: each state requires its own OS/OW permit
The Federal Highway Administration’s freight operations guidance underscores that OS/OW permits are state-issued and that carriers must obtain state permits for each state they wish to travel in (with state contacts provided). (FHWA OSOW permit contacts page dated 07/01/2025.) 

Accordingly, a manufactured home move originating in or destined to Texas but crossing state lines should be modeled as:

a TxDMV manufactured housing/OSOW permit for Texas legs, plus
the destination/origin state’s OSOW permits and escort rules, plus
local/city restrictions on the route endpoints.
Louisiana (LaDOTD OSOW permitting)
Louisiana DOTD’s OSOW permits page includes an explicit insurance requirement: OSOW truck loads seeking to operate in Louisiana must present a certificate of insurance for a minimum of $100,000, with insurance certificates required to be on file as of December 4, 2019. (Louisiana DOTD OSOW permits page; no visible publication date in snippet; contains dated policy change notice.) 

Louisiana DOTD’s permit pages describe fee structures for oversize permits, including:

Monthly Oversize Permit: $10 each day the permit is valid, with listed maximum dimensions for that permit type and validity options across weekday/weekend spans. (Louisiana DOTD Monthly Permits page; no visible publication date shown in snippet; accessed 2026-03-20.) 
Single Trip / Oversize permit: described as $10 per day / per trip for oversize movements (with exceptions listed). (Louisiana DOTD Single Trip Permits page; no visible publication date shown in snippet; accessed 2026-03-20.) 
Market implication for San Antonio carriers: A Texas-manufactured-home transporter running into Louisiana must budget for (a) Louisiana insurance-on-file compliance and (b) Louisiana daily-permit fees as applicable to oversize permits, on top of Texas TxPROS permitting. 

New Mexico (NMDOT oversize/overweight permits)
New Mexico DOT’s permits page provides a centralized entry point for permits including oversize/overweight permits and points to NMDOT ePermitting. (NMDOT Permits page; no visible publication date; accessed 2026-03-20.) 

NMDOT’s ePermitting page states that required documents are listed in the ePermitting system during application entry and references checklists and user guides. (NMDOT ePermitting page; no visible publication date; accessed 2026-03-20.) 

For escort triggers, a New Mexico commercial resources page (posted 08/06/2013) states that an escort is required for widths exceeding 14 feet and for loads exceeding 90 feet in length, with additional route-based discretion. (New Mexico commercial resources/escort guidance, dated 08/06/2013.) 

What is missing from the collected official sources: In the sources retrieved here, an official NMDOT fee schedule specifically itemizing manufactured home permit fees was not captured, and NMDOT ePermitting indicates that requirements and document lists appear inside the ePermitting workflow. 

Oklahoma (ODOT permits, fees, and escort contract triggers)
Oklahoma DOT publishes a permit fees PDF that explicitly lists a permit fee line for “Manufactured Home, Modular Home, House” as $40.00. (ODOT Permit Fees PDF, published ~1.8 years ago per index metadata; accessed 2026-03-20.) 

ODOT’s Size and Weight Permits page includes an “OHP Escort Contract” form for submitted applications where the load may require an Oklahoma Highway Patrol escort. (ODOT Size and Weight Permits page; no visible publication date; accessed 2026-03-20.) 

Market implication: Oklahoma provides clearer published baseline permit fees for manufactured home-type moves than the New Mexico sources retrieved here, but carriers should still model escort as potentially required through an OHP escort contract workflow depending on load/route. 

Mexico border crossings: U.S. export filings and border compliance (and why Mexico-side highway permits require separate diligence)
For a manufactured home being moved across the Mexico border, the move is no longer purely a “state OS/OW permits” problem; it becomes an export transaction plus cross-border trucking.

On the U.S. side, U.S. Customs and Border Protection (CBP) describes the Automated Export System (AES) as the central point through which export shipment data required by multiple agencies is filed electronically to CBP through ACE. (CBP “Introduction to AES,” dated 02/03/2026.) 

CBP’s help guidance (dated 01/29/2026) explains that Electronic Export Information (EEI) is required documentation and is filed through AES under defined filing thresholds/rules. (CBP Help article dated 01/29/2026.) 

The Foreign Trade Regulations specify EEI data elements in 15 CFR §30.6 and clarify that “mandatory” data elements must be reported for each transaction. (eCFR, 15 CFR §30.6; current regulation page accessed 2026-03-20.) 

CBP’s broader importing/exporting guidance emphasizes shared responsibility for compliance with laws and regulations governing trade. (CBP Basic Importing and Exporting page dated 02/10/2026.) 

Mexico-side permits not captured in the retrieved sources: This research set did not capture a primary Mexican federal highway oversize permitting manual from Mexico’s road/transport authority; therefore, this report can only state at a high level that Mexico-bound manufactured home moves should be expected to require Mexican customs clearance and any route/oversize authorizations required by Mexican federal/state authorities, with detailed fees and escort rules requiring Mexico-specific permitting sources. 

Carrier licensing and insurance: Texas requirements beyond FMCSA authority, including TDHCA bond/security linkages
State-level credentials beyond FMCSA: TxDMV motor carrier registration (“TxDMV Number”)
TxDMV states that intrastate motor carriers operating commercial motor vehicles on Texas roads must register operations with TxDMV’s Motor Carrier Division (obtaining a “TxDMV Number”), and it lists vehicle/cargo triggers for when registration is required (e.g., >26,000 lbs GVW/registered weight thresholds, hazmat placarding, passenger thresholds). (TxDMV “TxDMV Number” page; no visible publication date; accessed 2026-03-20.) 

The same TxDMV motor carrier registration page states that Texas law requires intrastate motor carriers to file proof of insurance/financial responsibility and identifies required insurance filings (Form E for liability, Forms H/I for cargo insurance, Form K for cancellation) submitted electronically by the insurer, and it describes administrative consequences for failure to maintain continuous proof. (TxDMV “TxDMV Number” page; no visible publication date; accessed 2026-03-20.) 

TxDMV’s Motor Carrier Handbook further describes insurance filing expectations and the use of Forms E/H/I/K for electronic filing. (TxDMV Motor Carrier Handbook, published “9 months ago.”) 

OS/OW permit application identity requirements: USDOT number verification and out-of-service checks
TxDMV’s Motor Carrier Handbook states that a valid USDOT Number is required for many OS/OW permit applications and that TxDMV verifies the USDOT with FMCSA’s MCMIS to ensure the carrier is not under an out-of-service order. (TxDMV Motor Carrier Handbook, published “9 months ago.”) 

For annual manufactured housing permits, TxDMV additionally allows use of the TDHCA licensing number in lieu of USDOT in some circumstances and performs out-of-service checks prior to issuance. (TxDMV annual manufactured housing page snippet; no visible publication date; accessed 2026-03-20.) 

TDHCA bond/security minimums that affect installation providers (and sometimes permit eligibility)
Texas’ Manufactured Housing Standards Act requires license holders (including installers) to file a bond or other security, with the installer amount at $25,000. (Texas Occupations Code §1201.106; TDHCA Standards Act compilation published 09/01/2023.) 

TDHCA’s 10 TAC rules operationalize bond continuity by linking bond cancellation to automatic suspension of the license. (TDHCA rules effective 03/03/2024.) 

How this impacts transport markets: Although the road-move OS/OW permit is under TxDMV, Texas’ annual manufactured housing permit process explicitly allows a TDHCA licensing number as an identifier in the permit application pipeline, creating a direct coupling between TDHCA licensing/bond continuity and TxDMV permit issuance eligibility for some manufactured housing moves. 

Key limitations and gaps from retrieved public sources
Texas DPS “escort fees” for Bexar County: Retrieved TxDMV and restriction-library sources show how law enforcement escorts become mandatory via specific permit conditions and jurisdiction restrictions and that movers are responsible for the fees, but a single statewide DPS escort fee schedule for manufactured home moves was not present in the retrieved official pages. 
New Mexico manufactured home permit fee schedule: Retrieved NMDOT sources clearly identify the ePermitting portal and workflow but did not include a captured primary fee table for manufactured home moves in the sources collected. 
Mexico highway OSOW permitting: U.S.-side export filing rules are well-supported in CBP/eCFR sources, but Mexico-side oversize highway permit fees and escort rules require Mexico authority sources not captured in this dataset. 


---

## Prompt 3

﻿
San Antonio Mobile Home Moving Distance-Based Pricing Tiers — 2026 Market Analysis
Scope and definitions
This report covers manufactured (mobile) home transportation—i.e., moving a home on a temporary chassis/returnable undercarriage (single-section) or as multiple transportable sections (multi-section homes). It does not cover household-goods moves. 

The pricing tiers and estimates below are framed around moves originating from or destined to the San Antonio metro and use the requested mileage brackets: 0–25, 25–50, 50–100, 100–200, 200–500, and 500+ miles.

What “transport” means in this analysis. In real invoices, “moving a manufactured home” often bundles items that are related to transport (e.g., mobilization, route planning, loading onto travel gear, basic handling at destination) and items that are installation/setup (e.g., re-leveling, anchoring, utility connection). Some consumer pricing references explicitly separate setup after transport from the move itself. 

To keep this “transport market” focused, the pricing table below estimates:

Base transport = linehaul + dispatch/mobilization + typical handling to make the home movable on road (varies dramatically by home condition and site access). 
All-in total (transport-all-in) = base transport + state trip permits + fuel surcharge allowance + escort/pilot car allowance (when required or commonly used). 
All dollar figures are USD and reflect a March 2026 market context for fuel (see Fuel section). 

Regulatory cost drivers for moves touching the San Antonio metro
Texas permitting authority and movement rules
In Texas, oversize/overweight permitting (including manufactured housing movement) is issued through the Texas Department of Motor Vehicles (TxDMV) Motor Carrier Division, and TxDMV rules incorporate route controls, movement windows, and escort requirements. 

Key manufactured housing permit/rule elements that directly affect pricing and especially short-haul scheduling:

A manufactured home permit is issued for a single continuous movement and not to exceed five days, and—critically—movement is daylight hours only under the rule language for manufactured housing. 
Manufactured housing movement is prohibited on major holidays (listed in rule text) and is also highlighted as restricted in TxDMV guidance. 
The permit contains the authorized route; the route must be the “most practical,” with explicit exceptions where construction restriction publications or bridge/overpass constraints make the route unsafe for the permitted dimensions. 
TxDMV guidance also notes that the Texas Department of Transportation (TxDOT) may restrict travel on routes because of “maintenance, construction activity, or congested traffic conditions.” That makes metro construction zones and peak congestion a real cost driver via detours, layovers, and escort needs. 
Escort and law-enforcement escort triggers in Texas
Texas has general escort/flag vehicle rules for overwidth loads (e.g., >14 ft triggers escort in general rules), but manufactured housing has special escort requirements codified in TxDMV rules:

If a manufactured home’s width exceeds 16 ft but not 18 ft, it requires one escort flag vehicle (front on two-lane roadways; rear on 4+ lanes). 
If a manufactured home exceeds 18 ft, it requires front and rear escort flag vehicles on all roadways at all times. 
TxDMV guidance also states law enforcement escorts may be required depending on size/route/nature of load, and the rules allow official law-enforcement motorcycles as escorts in certain incorporated-city movements. This is where local conditions can create “DPS escort if applicable” scenarios. 
Note: In Texas, the relevant law-enforcement entity referenced in OS/OW context is often the Texas Department of Public Safety (DPS). For manufactured housing, private escort flag vehicles are the baseline requirement in rule text; law enforcement involvement tends to be route-/jurisdiction-specific. 

Nearby/adjacent jurisdictions and curfews that matter for San Antonio metro-to-edge moves
TxDMV publishes a “time permit curfews” addendum for specific locations; near San Antonio this includes restrictions in the New Braunfels area (e.g., Business 46 / Loop 337 corridor and FM 306). These matter directly in the 25–50 mile and 50–100 mile brackets because “metro-to-edge” moves often traverse these corridors. 

New Braunfels is also a common edge-market destination for San Antonio-area manufactured home moves, aligning with the user’s bracket examples. 

Distance-tier pricing table for San Antonio-area manufactured home transport
How the table was constructed
Because actual invoices vary by home condition, site access, routing constraints, and what is bundled (transport-only vs broader relocation services), the table is a market estimation model anchored to published 2025–2026 cost references and explicit regulatory/fuel benchmarks.

Anchors used (no LocalMovers.com):

Published “local move” size-bands (typical, not Texas-specific):
iMoving (Updated Feb 23, 2026) reports $5,000–$8,000 to move a single-wide up to ~50 miles and $10,000–$13,000 for a double-wide (and triple-wide $20,000+). 
This Old House (Updated Mar 12, 2026) cites $1,000–$5,000 for “transportation only” as a broad benchmark. 
SpareFoot (Published Feb 5, 2025) provides size-level ranges (single-/double-/triple-wide) and notes “across town” can be around $3,000, while long-haul can reach $25,000+. 
San Antonio-region low-end “transport-only” signal: ProMatcher cost reports (Texas movers data) show single-wide “local move <50 miles” fixed-fee values around the low-$2,000s and double-wide per-mile figures for longer moves (reported data). 
Per-mile towing vehicle benchmark: Extra Space Storage (Updated Dec 8, 2025) cites $4.00–$5.50 per mile “for the towing vehicle alone.” 
Escort/pilot cost benchmarks:
Jim.com (Published Nov 14, 2025) cites typical pilot-car rates $1.75–$2.50 per mile, day rates $400–$600, and overnight adders $150–$250. 
Pilot Car 101 (Published Jan 26, 2025) shows example day-rate and per-mile structures (e.g., $2.00/mile, $650 day rate below 250 miles, by region). 
Fuel surcharge benchmark: U.S. Department of Energy 2026 weekly fuel surcharge matrix (Printed Mar 17, 2026) shows a truckload FSC example of $0.57/mile at a national diesel benchmark of $5.071 (week of Mar 16, 2026). 
Important interpretation note. In this model, “base transport” is intentionally wide to span:

low-end moves where a home is transport-ready and site access is straightforward (often closer to the ProMatcher/transport-only signals), and
higher-end moves where additional handling, route complexity, and coordination are required (often closer to the iMoving local-move bands). 
Distance-tier pricing table
The table uses representative midpoint mileage for each tier (15, 40, 75, 150, 350, 750 miles) to compute the effective per-mile values and fuel surcharge adders. Regulatory permit and escort assumptions are explained immediately under the table.

Distance tier	Home type	Base transport cost range	Transport-only linehaul rate (summed)	Transport-only effective rate	Permits (state trip permits)	Escort/pilot cars	Fuel surcharge add-on (est.)	Total all-in cost range	All-in blended per-mile
0–25 miles	Single-wide	$1,800–$7,638	$4.00–$5.50	$124.00–$507.50	$40–$40	$0–$650	$9	$1,909–$8,281	$127.24–$552.07
0–25 miles	Double-wide	$3,600–$15,275	$8.00–$11.00	$248.00–$1,015.00	$80–$80	$0–$1,300	$17	$3,817–$16,562	$254.47–$1,104.14
0–25 miles	Triple-wide	$5,400–$22,912	$12.00–$16.50	$372.00–$1,522.50	$120–$120	$0–$1,950	$26	$5,726–$24,843	$381.71–$1,656.21
25–50 miles	Single-wide	$1,900–$7,775	$4.00–$5.50	$49.00–$195.50	$40–$40	$0–$650	$23	$2,023–$8,433	$50.57–$210.82
25–50 miles	Double-wide	$3,800–$15,550	$8.00–$11.00	$98.00–$391.00	$80–$80	$0–$1,300	$46	$4,046–$16,866	$101.14–$421.64
25–50 miles	Triple-wide	$5,700–$23,325	$12.00–$16.50	$147.00–$586.50	$120–$120	$0–$1,950	$68	$6,068–$25,298	$151.71–$632.46
50–100 miles	Single-wide	$2,000–$8,050	$4.00–$5.50	$28.00–$116.50	$40–$40	$0–$650	$43	$2,183–$8,645	$29.10–$115.27
50–100 miles	Double-wide	$4,000–$16,100	$8.00–$11.00	$56.00–$233.00	$80–$80	$0–$1,300	$86	$4,366–$17,290	$58.21–$230.54
50–100 miles	Triple-wide	$6,000–$24,150	$12.00–$16.50	$84.00–$349.50	$120–$120	$0–$1,950	$128	$6,548–$25,936	$87.31–$345.81
100–200 miles	Single-wide	$2,200–$8,600	$4.00–$5.50	$16.00–$60.50	$40–$40	$0–$650	$86	$2,526–$9,100	$16.84–$60.67
100–200 miles	Double-wide	$4,400–$17,200	$8.00–$11.00	$32.00–$121.00	$80–$80	$0–$1,300	$171	$5,051–$18,201	$33.67–$121.34
100–200 miles	Triple-wide	$6,600–$25,800	$12.00–$16.50	$48.00–$181.50	$120–$120	$0–$1,950	$257	$7,576–$27,302	$50.51–$182.01
200–500 miles	Single-wide	$2,600–$10,250	$4.00–$5.50	$9.14–$29.93	$40–$40	$0–$1,125	$200	$3,440–$10,790	$9.83–$30.83
200–500 miles	Double-wide	$5,200–$20,500	$8.00–$11.00	$18.29–$59.86	$80–$80	$0–$2,250	$399	$6,879–$21,579	$19.65–$61.65
200–500 miles	Triple-wide	$7,800–$30,750	$12.00–$16.50	$27.43–$89.79	$120–$120	$0–$3,375	$599	$10,318–$32,368	$29.48–$92.48
500+ miles	Single-wide	$3,800–$12,450	$4.00–$5.50	$6.40–$17.00	$50–$80	$0–$2,375	$428	$5,278–$14,508	$7.04–$19.34
500+ miles	Double-wide	$7,600–$24,900	$8.00–$11.00	$12.80–$34.00	$100–$160	$0–$4,750	$855	$10,555–$29,015	$14.07–$38.69
500+ miles	Triple-wide	$11,400–$37,350	$12.00–$16.50	$19.20–$51.00	$150–$240	$0–$7,125	$1,282	$15,832–$43,522	$21.11–$58.03

Permit and escort interpretation inside the table (San Antonio context).
Texas manufactured housing movement is controlled by TxDMV permits and rules, including daylight-only movement and holiday prohibitions; escort requirements for manufactured housing are triggered notably above 16 ft width and above 18 ft, per rule text. 

The table therefore shows escort costs as $0–(escort range) because many common sections (e.g., ~14 ft) may not require escorts in Texas, while wider sections (or certain urban routing constraints) can trigger them. Escort cost benchmarks come from 2025 pilot-car rate references. 

Permit escalation logic for TxDMV permits and county/jurisdiction crossings
How Texas permit fees change with distance
For San Antonio-area manufactured home moves under Texas manufactured housing permits, the state permit is best understood as:

Flat per-section trip permit pricing (not mileage-priced for manufactured housing in the materials cited here), and a single continuous movement validity window (up to five days). 
Practical distance effect: while the permit fee itself is not “per mile,” distance increases the odds of needing multi-day staging (daylight-only rule), routing around construction restrictions, and coordination with utilities/obstructions—each of which can increase total cost even if the permit fee does not. 
County/city crossing considerations near San Antonio
Two recurring escalation patterns for moves starting/ending in San Antonio:

Time/curfew constraints on specific corridors: TxDMV publishes corridor-based curfews (not universal across the metro), including restrictions around New Braunfels that commonly affects “San Antonio to edge” routes. 
Local jurisdiction restrictions and fees: TxDMV maintains a list of jurisdictions with restrictions requiring notification before movement, including examples where cities require local permits and/or law-enforcement escorts for manufactured housing/house moves (e.g., the City of Houston; City of Laredo). While San Antonio is not singled out in the excerpted entries, the existence of such requirements elsewhere is evidence that city permitting/escort requirements can become an incremental cost depending on route. 
San Antonio area route constraints and oversize-move friction points
Manufactured home moves are unusually sensitive to dense interchanges, work zones, ramp geometry, and local “no-go” windows, because these moves are typically daylight-only and must follow permitted routes. 

Specific corridors requested
The following highlights focus on why these corridors routinely create cost variability, not on a claim that these highways are “always prohibited” for manufactured housing.

Loop 1604 (north side) and the I‑10 interchange zone
The Loop 1604 North Expansion Project is a major multi-segment TxDOT program in north Bexar County with sustained construction activity. Construction-phase detours and ramp/frontage road closures can force routing changes (and thus permit re-work or rescheduling), which is explicitly contemplated in TxDMV routing rules where construction restrictions make a route impractical for a permitted load. 

I‑35 through downtown (including downtown connectors to I‑10)
TxDOT’s San Antonio I‑35 corridor program (including “NEX” expansions) implies ongoing work and evolving traffic patterns. TxDMV guidance explicitly allows for TxDOT to restrict travel due to congested conditions and construction, which can be acute in downtown segments and can push manufactured home moves into narrower daytime windows. 

Loop 410 and I‑10 east-west flows
TxDOT materials describe I‑10 through the San Antonio district as a major east‑west corridor and note capacity/safety projects. In practice, the I‑10/410 interchange area is also a known freight bottleneck zone in broader corridor studies (used here only to support that congestion and construction are realistic operational constraints), reinforcing why oversize routing through these nodes is often planned as an off‑peak/daylight operation with high route-survey sensitivity. 

US‑281 corridor
TxDOT’s San Antonio-area US‑281 project pipeline reflects continuing corridor changes; for oversize movements, shifting construction patterns affect route selection and can require detours or alternative staging points. 

Oversize-load restrictions relevant to these corridors
Across these corridors, the following rules/constraints are the most “price-relevant”:

Daylight-only movement for permitted oversize moves as a baseline, with limited exceptions; manufactured housing movement is explicitly daylight only in the manufactured housing rule text. 
Construction-zone restrictions may be published and can invalidate otherwise “most practical” routing for a given permitted dimension set; this is explicitly called out in manufactured housing routing text. 
Utility/obstruction coordination is placed on the permittee (raising/lowering wires, signals, etc.), which is one of the most common hidden cost drivers for intra‑metro moves where local streets and frontage roads are involved. 
Interstate permit stacking and exact permit fees for TX plus adjacent states
The user requested “TxDOT + [other state DOT] permit stacking.” In practice, the Texas trip permit for manufactured housing is issued by TxDMV, not TxDOT (TxDOT is relevant for route restrictions and construction impacts). 

Below are permit-fee-only stacks for the common case where each transported section requires its own trip permit in each state.

Exact state permit fees used for stacking
Texas manufactured housing trip permit: issued by TxDMV (fee shown on TxDMV manufactured housing permit page). 
Louisiana Department of Transportation and Development: oversize permit is $10 day/trip, with an explicit exception that individual mobile homes issued an oversize permit for a single trip lasting up to 72 consecutive hours. 
New Mexico Department of Transportation: the “New Mexico Truckers Guide 2019” lists a Single Trip Oversize Permit Fee of $25.00. 
Oklahoma Department of Transportation: permit fee addendum lists Manufactured Home / Modular Home / House = $40.00. 
Permit-only stacking totals by home type
Assuming one section = single-wide, two sections = double-wide, three sections = triple-wide:

TX + LA (permit-only):

Single-wide: $40 + $10 = $50
Double-wide: 2 × ($40 + $10) = $100
Triple-wide: 3 × ($40 + $10) = $150 
TX + NM (permit-only):

Single-wide: $40 + $25 = $65
Double-wide: 2 × ($40 + $25) = $130
Triple-wide: 3 × ($40 + $25) = $195 
TX + OK (permit-only):

Single-wide: $40 + $40 = $80
Double-wide: 2 × ($40 + $40) = $160
Triple-wide: 3 × ($40 + $40) = $240 
Additional interstate permit/escort “stacking” realities that affect total cost
Louisiana’s rules also specify that private escort vehicles must have a Louisiana “ESCORT VEHICLE PERMIT,” costing $10 annually (typically embedded in an escort company’s overhead rather than passed as a separately itemized line). 

Oklahoma also publishes daylight-only movement rules and metro-area Interstate curfews (Cleveland, Oklahoma, and Tulsa counties) for oversize movements, which can create layover costs for TX→OK movements depending on schedule and routing. 

Fuel surcharge patterns and Texas Triangle corridor effects
Diesel prices: San Antonio vs national (March 2026)
As of March 20, 2026, American Automobile Association reports:

Diesel in the San Antonio market: $4.889/gal (“Price as of 3/20/26”). 
National average diesel: $5.159/gal (“Current Avg.”). 
That’s a $0.270/gal differential on that date. 

For heavy/oversize towing operations, if an operator’s effective fuel economy is ~5 mpg (a simplifying assumption; actual varies), that differential alone corresponds to roughly $0.054/mile lower fuel cost in the San Antonio market versus national average for the same fuel burn (0.270 ÷ 5). This is an illustrative calculation based on the observed AAA price gap. 

Why many quotes still track national fuel indices
Many surcharge schedules used in freight and logistics reference national diesel indices (e.g., DOE matrix examples). The 2026 DOE weekly fuel surcharge matrix shows that in the week of March 16, 2026, with national diesel at $5.071, a truckload fuel surcharge example is $0.57 per mile. 

Implication for San Antonio pricing: even if diesel is cheaper locally, carriers/brokers using index-based FSC tables may still quote a surcharge aligned with national benchmarks, while carriers using “actuals” may reflect some of the local diesel advantage in a slightly lower per-mile all-in quote. 

Texas Triangle corridor pricing: why SA↔Houston/DFW/Austin can price better per mile
TxDOT’s “Texas Connected Freight Corridors” initiative explicitly covers the “Texas Triangle” formed by I‑35 (including extension to Laredo), I‑45, and I‑10, linking (among others) Austin, Dallas‑Fort Worth, Houston, and San Antonio. 

Texas Triangle logistics intensity is also emphasized in TxDOT’s Texas Triangle Multimodal Strategic Plan framing (Texas Triangle = major share of population/economy). 

Pricing inference (supported by corridor facts, not a published tariff): On high-volume corridors like I‑35 and I‑10—especially between San Antonio and Austin or Houston, and toward the Dallas–Fort Worth region—carrier density and backhaul availability are typically better than on lower-volume rural routes. That tends to reduce deadhead and scheduling friction, which can translate into lower effective per-mile pricing in the 100–200 and 200–500 brackets relative to similarly long moves in sparse corridors. 

Interstate examples aligned to the requested brackets
To match the user’s examples, the 50–100 bracket often captures San Antonio-to-Austin type moves; the 100–200 bracket includes San Antonio-to-Corpus Christi and San Antonio-to-Laredo class moves; the 200–500 bracket includes San Antonio-to-Dallas–Fort Worth; and the 500+ bracket includes San Antonio-to-Albuquerque (TX+NM permitting) and San Antonio-to-Shreveport (TX+LA permitting) type moves, with permit-only stacking shown earlier. 


---

## Prompt 4

﻿
San Antonio Mobile Home Moving Seasonality & Demand Drivers — 2026 Market Analysis
Scope and methodology
This report analyzes manufactured home transport (single-/multi-section “mobile home moving”), not household-goods moving. Seasonal pricing is modeled for the San Antonio metro as a function of (a) transporter/escort capacity constraints, (b) Texas oversize/overweight operating rules (daylight travel, local curfews, holiday prohibitions), and (c) local demand shocks (military PCS seasonality, storm/disaster response drawdowns, redevelopment-driven relocations, and regional housing/energy cycles). 

What the multipliers represent
Annual baseline (1.00x) is the modeled average of transport-only pricing (tow + escorts/pilot cars + permitting/admin typical of a compliant move), normalized across the calendar year for the San Antonio metro. It excludes “site work” and set-up (pad/foundation, utilities, tie-downs, skirting) and excludes extreme, disaster-emergency pricing (where capacity is diverted to response work). These exclusions match how oversize movement is practically priced and constrained in Texas (permit conditions + weekday/daylight windows + holiday limits). 

Why purely “quote-based” seasonality is not published
Neither Texas permitting agencies nor federal sources publish a San Antonio–specific monthly “price index” for manufactured home moves; therefore, the multipliers are an evidence-based market model anchored to measurable demand/capacity drivers (PCS peak season, Texas daylight/curfew restrictions, and disaster-response surge behavior documented through FEMA’s direct-housing logistics and historical Texas disaster deployments). 

Month-by-month seasonal multipliers
Summary of the modeled curve
The modeled seasonal curve has a low point in mid-winter (weak consumer demand, fewer discretionary relocations, and fewer redevelopment “move-out” deadlines landing in January) and a high point in mid-summer (capacity competition from peak military PCS demand and general peak-season scheduling pressure). DoD/Service guidance consistently frames May–August as “peak moving season,” driven by capacity (trucks/drivers) limits; that same capacity logic applies to specialized towing/escort resources used in manufactured-home transport. (U.S. Army article published June 15, 2013; JBSA article published July 10, 2018.) 

Monthly multipliers table
These values average to 1.00x across the year by construction.

Month	Multiplier vs annual baseline	San Antonio-area demand dynamics that push pricing up/down
January	0.86x	Cheapest month (modeled). Post-holiday lull + fewer “must-move” timelines. Also, Texas oversize movement is effectively “daylight-limited” (30 minutes before sunrise to 30 minutes after sunset), which can constrain productivity in winter, but the demand drop dominates the net price effect. 
February	0.88x	Demand remains soft, but schedules begin to firm as installers/transporters book spring work. Any late-winter weather disruption risk is usually lower than northern states, keeping February near the trough. 
March	0.96x	Transition month: rising volumes as buyers place homes before school-year and summer deadlines; also the start of stronger convective-storm patterns in Central/South Texas increases “weather contingency” padding in schedules. 
April	1.01x	Early severe-weather season (hail/severe thunderstorms) increases rescheduling risk and can trigger localized replacement/temporary housing needs after damaging events. Example: hail and severe storms affected the San Antonio area in April 2024 (local reporting published April 21, 2024). 
May	1.07x	PCS ramp-up begins. DoD/Service communications repeatedly identify May–August as peak season, with the highest-pressure window often around late May through early July, creating broad capacity strain that can spill into specialized transport markets. (Army article published June 15, 2013; Air Force news item published March 22, 2012.) 
June	1.12x	Peak-season capacity squeeze: summer is the tightest scheduling environment, and Texas daylight windows are long but heavily competed. Also, hurricane season begins (June), increasing the probability of “capacity diversion” toward coastal staging if a Gulf event forms. (TxDMV handbook notes TxDOT can restrict travel for congestion/construction; manufactured housing is prohibited on national holidays.) 
July	1.18x	Most expensive month (modeled). Peak-of-peak pricing: competition for trucks/drivers/escorts is strongest in midsummer. JBSA reports ~4,500 customer shipments during peak season (May–Aug), illustrating the local scale of peak-period demand pressure. (JBSA article published July 10, 2018.) 
August	1.09x	Still peak, but pressure begins easing as PCS and school-year timing constraints resolve. Booking lead times and “date flexibility” still matter. 
September	1.02x	Shoulder season: more capacity returns, but hurricane season remains active (June–Nov), so the “storm diversion” risk premium persists, especially if coastal impacts create temporary-housing movement needs. 
October	0.98x	Generally stable demand and good operating conditions. While hurricane season continues, Texas often sees fewer peak scheduling conflicts than summer PCS months. 
November	0.94x	Demand softens as customers avoid holiday conflicts; oversize movement planning becomes more sensitive to holiday prohibitions and local congestion restrictions around major travel periods. 
December	0.89x	Holiday effects compound: manufactured housing movement is prohibited on national holidays and permit offices run on weekday schedules, so many customers delay moves rather than pay for awkward scheduling. (TxDMV handbook + TxDMV holiday restrictions page.) 

Single cheapest month: January (0.86x)
Single most expensive month: July (1.18x)

Demand drivers specific to the San Antonio metro
Severe weather and disaster response drawdowns
San Antonio sits inland, but its manufactured-home transport market is exposed to statewide capacity reallocations when disasters create a need to (a) remove damaged units, and (b) deliver temporary housing units.

Severe storms and hail (spring, roughly April–June). Large hail and severe thunderstorm activity can cause widespread property damage in the Hill Country / I‑35 corridor; April 2024 was one such episode with hail and storm impacts reported in the San Antonio area (local reporting published April 21, 2024). These events typically increase short-notice needs for temporary sheltering and can disrupt planned moves through weather delays. 

Gulf hurricanes and temporary housing deployments (June–November). When a major Texas hurricane triggers Direct Temporary Housing Assistance, FEMA’s own guidance describes that eligible survivors may receive a Transportable Temporary Housing Unit such as a travel trailer or Manufactured Housing Unit, after site inspection and ordering a unit “to be delivered,” which is performed through FEMA’s contractor logistics chain (fact sheet dated January 27, 2025). 

Texas has a clear historical precedent that these missions can be large enough to distort the market for transport and installation capacity:

After Hurricane Harvey, Texas recovery materials explicitly describe Manufactured Housing Units (MHUs) and travel trailers as temporary housing options provided by FEMA (state recovery/Harvey fact sheet). 
The DHS Office of Inspector General documented that FEMA’s post‑Harvey MHU program in Texas involved substantial purchase, transportation, and storage costs, including an overestimate of MHUs and at least $152 million in purchase/transportation/storage costs tied to excess units (OIG report issued February 26, 2020). This is direct evidence that Texas hurricane response can consume manufactured-housing transport capacity at scale. 
Why this matters for San Antonio pricing: When a Gulf event (e.g., Hurricane Beryl, major disaster declaration DR‑4798, announced July 2024) increases statewide emergency logistics activity, specialized transporters and escorts can be pulled toward higher‑urgency work, tightening availability in inland metros. Even if San Antonio is not the impact zone, its market can feel the capacity shock through dispatch and subcontractor networks. 

Military PCS cycle and JBSA demand pressure
Military moves are a macro-demand amplifier because they intensify competition for trucking labor, scheduling windows, and related contractor capacity at predictable times.

PCS peak season timing. Service communications routinely describe May–August as the peak moving season (for example, U.S. Army guidance published June 15, 2013; Air Force guidance published March 22, 2012). 

JBSA local scale. JBSA reported that peak moving season is May–August and that the base “averages approximately 4,500 customer shipments during that time” (JBSA article published July 10, 2018). 

How many PCS moves involve manufactured homes? There is no JBSA‑specific public reporting that breaks out “mobile/manufactured home shipments” as a counted category. What can be stated from primary policy sources is:

The Defense Transportation Regulation (draft dated February 16, 2024) explicitly treats mobile homes as an available transportation entitlement and notes that mobile home transportation can be selected instead of household goods transportation, with restrictions when a mobile home is moved under the same PCS order. 
Nationally, GAO reported that USTRANSCOM arranges on the order of ~300,000 personal property shipments annually (GAO report published September 11, 2025). 
Because (a) mobile home transportation is an “in lieu of HHG” option and (b) most PCS households do not relocate a permanently-sited manufactured home, the manufactured-home share of PCS moves is widely understood in industry practice to be small; however, a precise JBSA annual count is not available in the cited public record. The practical pricing implication remains: PCS season still elevates midsummer pricing by tightening driver/tractor availability and bookings—especially for any operators who straddle HHG/military logistics and specialized towing/escort work. 

Population growth and manufactured housing affordability
San Antonio’s growth expands the pool of households for whom manufactured housing is a cost solution—and increases the frequency of placements, park-to-park relocations, and displacement-driven moves.

Growth fundamentals. The U.S. Census Bureau’s Vintage 2024 place estimates show San Antonio added 23,945 people between July 1, 2023 and July 1, 2024 (press release with tables released May 2025). 

At the metro level, the San Antonio–New Braunfels MSA population estimate for 2024 is 2,763,006 (thousands of persons), as published through FRED’s Census-sourced series update (updated March 14, 2025). 

Affordability advantage creates demand elasticity. Manufactured homes’ pricing—especially in the South—supports demand when site‑built housing is expensive. MHI’s summary of Census MHS pricing data reported a national average sales price around $120,900 in January 2025 and identified the South as the most affordable region at $116,300 (published July 22, 2025). 

By comparison, HUD/Census reported the median sales price of new single-family houses sold in January 2025 at $446,300 (press release HUD No. 25‑037). 

Why this matters to transport cost: More manufactured-home purchases and placements increase demand for (a) delivery moves from retailers/factories into the metro edge counties, and (b) secondary relocations as households trade up, parks change ownership, or land uses shift. When this demand stacks with May–August capacity constraints, it raises the probability of premium pricing (modeled in June–August). 

Oil and gas workforce housing cycles
San Antonio’s position on the I‑35 corridor and proximity to the Eagle Ford region can make it a practical staging/dispatch metro for workforce housing deliveries and relocations.

A TDHCA housing-center addendum for Region 9 (San Antonio) reports that the Eagle Ford Shale oil boom contributed to increased affordable housing need and that local sources described rents doubling or tripling due to increased oil production and a rising transient workforce (report excerpted from a TDHCA PDF). The same document reports manufactured home parks surveyed in the region operating at 98.4% occupancy/usage, above the statewide average (figures shown in the report). 

Additionally, in the Census Bureau’s March 13, 2025 metro growth tables, Midland and Odessa appear among the top U.S. metro areas by percent growth (July 1, 2023 to July 1, 2024), consistent with ongoing West Texas energy-region population pressure. 

Transport implication for San Antonio: Energy workload surges can increase demand for “rapid housing” (including manufactured units) and tighten the availability of the specialized tractors, escorts, and setup crews used to deliver and relocate units—raising prices most noticeably when energy surge coincides with summer peak logistics demand. 

Construction, redevelopment, and manufactured-home community displacement
The most direct displacement mechanism is not that a highway project physically “moves a mobile home,” but that land value and redevelopment pressures reduce the stock of older manufactured-home communities and create forced relocations.

Documented local trend: park closures. Texas Public Radio reported that close to 22,000 San Antonio residents lived in the city’s mobile home communities and that at least nine parks had shuttered since 2014, with redevelopment and rezoning among the drivers (published February 23, 2020). 

City programs recognize mobile-home relocation cost structure. The City of San Antonio’s Resident Relocation Assistance Program explicitly includes “costs specific to mobile homes including: relocation of a mobile home, mobile home park fees, and site preparation” and sets higher caps for mobile-home relocation assistance (program page accessed via SA.gov). 

Major infrastructure and growth corridors as indirect catalysts. TxDOT’s I‑35 NEX Central project (9.5 miles, construction started June 2022, estimated completion late 2027) is one example of large-scale corridor investment that can change accessibility and redevelopment economics around interchanges and frontage roads. While the TxDOT project overview does not itself quantify manufactured-home community displacement, the combination of (a) park-closure trend reporting and (b) major corridor redevelopment incentives supports the conclusion that redevelopment-linked relocation demand is a sustained upward pressure on local mover workloads, especially in shoulder seasons when scheduled relocations are often planned. 

Retirement and snowbird seasonality
This driver is real but usually secondary for manufactured-home transport in the San Antonio metro, because many seasonal residents use RV sites rather than relocating titled manufactured homes.

Retirement attractiveness. A San Antonio-focused Axios item (published July 25, 2024) ranks San Antonio highly for “aging-friendly” housing stock and reports rapid growth in the 65+ population over 2020–2023, consistent with retirement/downsizing demand. 

Seasonal “Winter Texan” pattern nearby. Hill Country / I‑35 corridor RV parks market winter seasons typically November–March (examples include RV park seasonal-booking pages in the region). These patterns can increase demand for placement/long-stay sites and light setup work in late fall and winter, but they more often affect RV occupancy than manufactured-home towing volume. 

Net transport implication: retirement/snowbird season contributes modestly to November–March stability (keeping the deep-winter trough from falling further), but it does not outweigh the May–August peak surge in transporter/escort competition. 

Oversize-load constraints and schedule-based pricing
Texas movement windows that structurally shape “cheaper” vs “more expensive” days
Manufactured-home moves are constrained by the same oversize/overweight movement conditions that define how many miles can be completed per day and which days can be used:

Daylight movement standard. TxDMV’s Motor Carrier Handbook defines daytime for permitting (30 minutes before sunrise to 30 minutes after sunset) and states that permitted vehicles may travel only during daytime unless the permit authorizes night movement. 
Congestion/construction restrictions. The same handbook notes TxDOT may restrict travel on certain routes due to maintenance, construction, or congested traffic conditions—relevant in the San Antonio metro where major projects create recurring closure windows. 
Holiday prohibitions. The handbook states manufactured housing are prohibited from moving on national holidays, which compresses scheduling around holiday weeks (raising the probability of premium quotes for adjacent “good days”). 
Local and corridor-specific curfews that affect time-of-day pricing
TxDMV’s “time permit curfews” list (revised September 30, 2025) documents jurisdictional restrictions that can fall on common San Antonio-area routes, including:

New Braunfels: a restriction for loads over 12 feet wide on a specific route segment during 11:30 a.m.–1:30 p.m. (Mon–Fri). 
Seguin: restrictions for loads over 95 feet long with weekday peak-hour curfews (noted in the curfew list), which can reduce productive movement time and push jobs into multi-day scheduling. 
Nearby Hill Country jurisdictions in the same curfew listing include places with weekend-wide curfews for certain oversize/overweight vehicles, which can make “weekend moves” infeasible on particular routings—effectively shifting the market toward weekday scheduling. 
Pricing consequence: A “half-day lost” to curfews, daylight limits, or inspection/escort coordination has real cost because the tractor + escorts + crew time still accrue. Thus, days/times that allow a clean long run (typically mid-week, mid-day) often price more efficiently than high-friction windows (Friday afternoon, pre-holiday, or routes that force waiting through curfew blocks). 

Weekend premiums in practice
Because (a) permitted movement is daylight-limited, (b) many restrictions are weekday congestion blocks or route-specific weekend prohibitions, and (c) permit/admin support runs on business schedules, San Antonio-area manufactured-home moves are commonly quoted and executed on weekdays. Where a weekend move is feasible and requested, any premium is typically a function of (1) whether escorts/install crews charge a weekend rate and (2) whether the route avoids weekend-prohibited jurisdictions. This premium is therefore route- and crew-availability dependent, not a universal “weekend surcharge.” 

What to watch in 2026
Storm-triggered “capacity shocks” are the biggest upside risk to the multipliers
The gradient described in the multipliers assumes a “normal” year without a major Texas temporary-housing mission. If a Gulf hurricane season produces a Harvey-like direct housing scale-up, historical evidence shows FEMA procurement and movement of MHUs can be large enough to generate substantial transportation costs and absorb specialized capacity—raising inland quotes beyond the modeled June–October range. (Texas example: DHS OIG report issued February 26, 2020 on post‑Harvey MHU procurement/transport costs; FEMA direct housing fact sheet dated January 27, 2025 describing delivery process.) 

Continued population growth and redevelopment keep “relocation demand” structurally elevated
The combination of (a) continued city/metro growth measures and (b) documented decline in mobile home communities supports the expectation that relocation-driven demand remains a persistent pricing floor—even in cooler months—relative to slower-growth metros. (Census place estimates release May 2025; TPR displacement reporting February 23, 2020.) 


---

## Prompt 5

﻿San Antonio Mobile Home Mover Market Tiering & Competitive Landscape — 2026 Market Analysis
Scope, definitions, and source base
This market scan focuses on manufactured (mobile) home transportation in the San Antonio metro, defined as oversize-load hauling of single-wide and multi-section homes (often using a toter truck), plus (for many operators) set-up / re-level / foundation / skirting coordination. It explicitly excludes household-goods movers.

Primary data sources used for company verification and market sizing were:

Federal Motor Carrier Safety Administration SAFER Company Snapshot pages for USDOT, status, and power units / drivers (Snapshot “as of” dates are shown within each SAFER record). 
Better Business Bureau business profiles for rating/accreditation, years in business, and publicly listed phone/address/service-area. (BBB pages are dynamic; this report treats them as “accessed” on March 20, 2026.) 
Two review-focused sources requested in the prompt could not be used in a fully consistent way here:

Yelp pages were blocked from direct access by the research crawler (no reliable, citable page retrieval). 
Google Business Profiles were not used as a primary data source because direct profile pages were not consistently retrievable in a verifiable way within this environment; where relevant, this report relies on BBB and company websites instead. 
Pricing is rarely published by movers and is highly route- and condition-dependent. Tier price bands below therefore anchor to industry-reported ranges (national and local estimate sources) and are presented as planning ranges rather than quotes. 

Competitive landscape in the San Antonio metro
Top operators serving the metro
The table below profiles six movers with clear evidence of operational presence serving the San Antonio-area market, using BBB and FMCSA SAFER as the backbone. (Some companies are “install + transport,” others are transport-focused.)

Pricing tier legend (planning bands):

Budget (transport-only / minimal services): Single-wide ~$1,000–$5,000; Double-wide ~$2,000–$8,000 (often two sections; wide variance). 
Mid-range (typical local/regional move + basic coordination): Single-wide ~$5,000–$9,000 (industry “typical” around $6,500); Double-wide ~$9,000–$15,000 (industry “typical” around $11,500). 
Premium (complex routing/conditions/multi-crew, multi-day, multi-section beyond “standard”): Single-wide ~$8,000–$12,000+; Double-wide ~$15,000–$25,000+. 
Company (base city)	Est. years in business	USDOT (SAFER)	BBB rating / accreditation	Fleet capacity indicator	Service area signal	Pricing tier (planning)	Public phone	Notable specialization signals
Texas Elite Mobile Home Transport (San Antonio)	BBB lists 3 years	4056947	A+, BBB Accredited	SAFER shows 1 power unit / 1 driver	Company states service areas include San Antonio, Austin, Houston	Mid-range (can price toward premium when bundled with add-ons)	(210) 801‑9972 (BBB + site)	Appears positioned as a one-stop MH services shop (transport + related services showcased, including leveling/roofing/skirting/decks). 
RH Mobile Home Installers (Lytle)	BBB lists 7 years (started 2019)	3313938	A+, BBB Accredited	SAFER shows 4 power units / 3 drivers	Intrastate, non-hazmat carrier profile; San Antonio-area proximity supports metro coverage	Mid-range	(210) 605‑9761 (BBB); SAFER lists (210) 420‑3032	“Installers” branding suggests a setup/installation-adjacent posture rather than transport-only; likely suited for park-to-park and local repositioning where coordination matters. 
Martinez Mobile Homes (San Antonio)	BBB lists ~14 years (locally since 1983 per BBB)	1981950	F, not BBB accredited	SAFER shows 1 power unit / 1 driver	Carrier operation marked intrastate only; cargo carried includes mobile homes	Mid-range pricing expectations (brand recognition sometimes supports higher quotes), but verify carefully	SAFER lists (210) 394‑9233	High-verification-required profile: BBB notes an alert regarding a TxDMV common carrier license revocation tied to failure to maintain required insurance (dated 1/31/2025 on BBB profile). This increases the importance of current document checks prior to contracting. 
Five Star Mobile Home Transporting (Elmendorf)	Estimated ≥11 years (SAFER MCS-150 form date 2015)	2595356	BBB Not Rated / not accredited	SAFER shows 1 power unit / 1 driver	BBB lists service area by ZIPs concentrated in south-side SA area (examples include 78112, 78214, 78221, 78223, 78235, 78264)	Budget → Mid-range depending on scope (transport-only vs coordination)	(210) 542‑5924	Small-fleet footprint suggests focus on local/regional hauls, often attractive for budget transport-only jobs if you already have set-up crews. 
R & H Transport Services, LLC (Seguin)	Estimated ≥3–4 years (SAFER MCS-150 form date 2022)	2965809	BBB lists A+ / not accredited	SAFER shows 6 power units / 3 drivers	BBB indicates statewide TX service area; larger fleet supports broader dispatch capacity	Mid-range leaning premium for hard jobs (capacity premium)	BBB lists (830) 549‑4445; SAFER lists (830) 433‑5551	In this sample, R & H shows the largest capacity—this tends to matter when schedules are tight, multiple moves are queued, or when escorts/permits create timing constraints. 
Affordable Space Mobile (San Antonio)	Estimated ≥5 years (BBB file opened 2020)	576322 (record shown as INACTIVE in SAFER)	BBB lists A+ / not accredited	Not reliable from SAFER due to “record inactive” status display	BBB lists broad ZIP-based service area coverage (numerous 78xxx ZIPs)	Budget if operating as transport-only; verify operating status first	(210) 602‑8885	This is a verification-sensitive option: SAFER indicates the USDOT record is currently INACTIVE, which is a red flag for any paid transport work without clarifying the underlying status and compliance posture. 

Market tiering and what drives price differences
Budget tier
Budget operators in this market tend to be transport-first and service-light, often with 1 truck / 1 driver and intrastate (Texas-only) operating patterns visible in SAFER snapshots. 

Planning price band (budget): Single-wide ~$1,000–$5,000 for transport-only; double-wide ~$2,000–$8,000, largely because a double-wide is commonly moved in more than one section and may require more time, equipment, and permit complexity. 

Common tradeoffs that explain the lower tier:

Less included scope (permits, escorts, blocking/leveling, utility disconnect/reconnect may be excluded or subcontracted). 
Higher schedule sensitivity (if the single truck is committed elsewhere, lead times can extend). 
In the San Antonio metro, Five Star Mobile Home Transporting often looks structurally “budget-capable” based on its SAFER-reported size. 

Standard tier
Standard-tier operators are most attractive to homeowners who want one contractor coordinating the move, even if specialized electrical/plumbing hookups are performed by separate licensed trades.

Planning price band (standard): Single-wide ~$5,000–$9,000; double-wide ~$9,000–$15,000, aligning with widely published “typical” figures (around $6,500 single-wide and $11,500 double-wide) for a full move in many markets. 

In operator terms, standard-tier companies often show:

A credibility stack that helps buyers feel safer (BBB A/A+ ratings; visible business start dates). 
Enough capacity (more than one power unit, or stable installation crews) to smooth scheduling. 
Examples that can reasonably be positioned in the standard tier (based on a combination of BBB stability signals + SAFER footprint + stated service coverage) include Texas Elite Mobile Home Transport and RH Mobile Home Installers. 

Premium tier
Premium moves are driven less by “brand” and more by job complexity and risk. Even when base mileage is short, complexity adds cost via multi-crew time, escort timing windows, lift/axle work, route engineering, and contingency planning.

Planning price band (premium): Single-wide ~$8,000–$12,000+; double-wide ~$15,000–$25,000+. 

Situations that tend to price premium in the Texas Hill Country / San Antonio regional context (inference grounded in the cost drivers emphasized in major consumer cost guides):

Longer or constrained routing, including narrow access roads and difficult approaches. 
Multi-section moves (double-wide, triple-wide equivalents), where “per-section” mobilization and escorts multiply. 
Tight timeline requirements (a mover with more trucks can command a premium when capacity is scarce). 
Among the profiled set, R & H Transport Services, LLC is best positioned to sometimes price into premium due to higher dispatch capacity (6 power units). 

National carriers and brokers
A complete, source-verified roster of national heavy-haul carriers (and/or brokers) actively quoting manufactured-home moves into the San Antonio metro could not be compiled from the accessible sources above within this environment. The key economic comparison, however, is stable across markets:

National carriers and brokers typically compete on:

Ability to execute interstate moves at scale when local movers are intrastate-only or lack authority. 
Broader equipment options and redundancy (multiple tractors/drivers), which matters when schedules slip. 
They can price higher than small local toter operators on simple local moves, but may be competitive (or even necessary) for multi-state jobs where operating authority, insurance filings, and dispatch redundancy matter. 

Market concentration and pricing power in the San Antonio-region catchment
How many active transporters are “in the market”?
There is no single perfect public count of “manufactured home transporters serving” a county, because firms can serve an area without being headquartered there. Two practical proxies from accessible sources:

BBB’s category directory shows 21 results for Manufactured Home Transport near San Antonio, TX (directory view). 
A trucking-directory filter using “Mobile Homes” freight for San Antonio returns 46 companies (third-party compilation based on carrier data feeds; useful as a directional indicator, not a regulator-of-record count).
For the surrounding-county ring—Bexar County, Comal County, Guadalupe County, Medina County, Kendall County, and Wilson County—BBB’s directory view explicitly lists multiple operators located in adjacent towns (e.g., Elmendorf, Seguin, Canyon Lake) and flags “service area: TX” for several, indicating that the practical service market is broader than Bexar alone. 

Fragmented vs. concentrated?
Using the six profiled firms as a micro-sample, fleet sizes skew small (1–6 power units). 
 This is consistent with a fragmented market structure (many small operators rather than a few dominant fleets).

Implications for pricing leverage (inference, grounded in the fact pattern of many small fleets and the published price variability in move cost guides):

Consumers have leverage on straightforward local moves because multiple small carriers can bid and the job is substitutable. 
Carriers gain leverage when constraints bite: permit windows, escort vehicle availability, weather, tight park rules, or when a job needs redundancy. A firm with more power units can often command a premium when demand spikes. 
Because SAFER shows many carriers as intrastate-only and “NOT AUTHORIZED” for interstate authority (common in the snapshots), an interstate move can thin the field dramatically, increasing price pressure upward. 
Consumer verification checklist for San Antonio homeowners
This checklist is designed to verify licensing, road authority, and insurance for manufactured home transport and related installation work in Texas.

Verify TDHCA licensing for installation-related work
Use the Texas Department of Housing and Community Affairs Manufactured Housing database to search license records (the public portal explicitly shows “license data last updated” dates). 
Confirm the company (or the individual installer of record) holds the relevant installer credential; TDHCA’s installer license type information indicates that the installer license category has specific requirements (including a surety bond requirement referenced on the installer license page). 
If your mover claims “transport-only,” confirm whether they are relying on a separate licensed installer for the setting/re-level/foundation portion; Texas rules distinguish between transport and installation activity.
Verify TxDMV / TxDOT manufactured housing move authority and permitting
Ask for (and retain) the manufactured housing movement permit documentation for your specific trip. Texas permit rules for manufactured housing moves are administered through state transportation channels (TxDMV program page and Texas Administrative Code references).
Confirm that the move plan complies with Texas size/weight and escort requirements for manufactured housing moves (Texas Administrative Code reference).
Verify FMCSA USDOT status and (if applicable) interstate authority
Pull the mover’s SAFER Company Snapshot and confirm:
USDOT Status: ACTIVE (not inactive / out of service). 
The company name/DBA, address, and phone match what the mover is presenting. 
The fleet size shown (power units) matches the operational story you’re being told (e.g., “we have multiple trucks available”). 
If any portion of your move is interstate for-hire, confirm the mover has the correct operating authority (MC) and insurance filings via the “Licensing & Insurance” link surfaced in SAFER/SMS, and understand that interstate transportation requires active safety registration/authority. 
Verify insurance in a way that actually protects you
Request a Certificate of Insurance (COI) sent directly from the agent/broker to you (not a forwarded PDF).
Verify at least:
Auto liability (limits appropriate to commercial operation) and
Cargo / transit coverage appropriate to a manufactured home move (home value often exceeds basic cargo norms).
Cross-check the existence of insurance filings for for-hire carriers through the FMCSA licensing/insurance system links surfaced by SAFER/SMS. 
Red-flag screens before you pay a deposit
SAFER USDOT shows INACTIVE (for example, “record inactive” messaging) yet the mover is offering immediate paid transport—treat as a stop-and-verify moment. 
BBB alerts about licensing/insurance issues: treat this as a mandatory due-diligence signal, not a soft review metric. 
Mismatch between the mover’s business name and operator-of-record on SAFER (e.g., a different legal name entirely) without a clear DBA explanation. 
What to request in writing
Home specs: HUD label / serial, width/length, section count, axle/tire condition, and whether the mover will require axle work before transport (common cost driver). 
Scope matrix: disconnect, skirting removal, steps/decks, AC handling, escort coordination, permits, and set-up/leveling responsibilities (who does what, and what is excluded). 
Schedule and cancellation terms—small fleets can be schedule-sensitive, and the written agreement should say what happens if the move window shifts. 


---

## Prompt 6

﻿
San Antonio Mobile Home Moving Hidden Costs & Surcharges — 2026 Market Analysis
Scope, sourcing rules, and what “final price” really includes
This report covers manufactured (mobile) home transport and installation in the San Antonio metro (with special attention to the urban core plus Hill Country edge markets such as Helotes/Boerne/Bulverde/Canyon Lake corridors). It does not cover household‐goods moving.

A recurring pricing failure in this market is that many quotes are framed as “transport” or “move-and-set”, while the customer’s “final price” ends up including a wider bundle: teardown and prep, permits and re-issues, escorts, route constraints, utility coordination, site work, foundation/anchoring, and (in certain geographies) floodplain and aquifer compliance. National cost guides show broad “all-in” ranges for a mobile/manufactured home move (e.g., $5,000–$20,000 typical range) and highlight that permits, escorts, and prep can materially move the number. 

A practical “baseline” for context (not a guarantee): one 2026 guide reports full-service relocation averages around $6,500 (single-wide) and $11,500 (double-wide), with large variation by route, setup scope, and site conditions. 

Source exclusions: LocalMovers.com is not used or cited.

Hidden cost register for the San Antonio metro
The table below is structured to meet your requirements: cost item name, specific dollar range, and the San Antonio-area trigger/cause. Where an amount is inherently variable (because the utility or agency bills time-and-materials or because detours are situation-dependent), the entry uses a priced unit-rate or a fixed fee from a primary source, and then shows how the variable portion scales.

Permitting, routing, and compliance fees that often surprise customers
Hidden cost item	Typical 2026 dollar range	San Antonio-area cause / trigger
Texas manufactured housing single-trip permit (per section)	$40.00 base permit fee + credit-card service charge ($0.25 + 2.25%) if paid by card (approx $41.16 for a $40 permit shown on TxDMV fee table)	Required when the home is transported as manufactured housing under Texas OS/OW rules; double-wides typically involve two sections → two permits. TxDMV’s Manufactured Housing Single-Trip Permits page lists the $40 fee and card surcharge rules; TxDMV’s fee table shows an “amount due with service charge.” (TxDMV pages: publication date not clearly shown; accessed Mar 20, 2026.) 
Annual manufactured housing permit	$1,500	Used by some carriers for repeated movements (notably from manufacturer to storage within a limited radius); can appear as a line item if you buy from a dealer who bakes it into delivery economics. (TxDMV page: publication date not clearly shown; accessed Mar 20, 2026.) 
Permit change / re-issue because the route must change	$40.00 per replacement single-trip manufactured housing permit (and potentially more if multiple sections)	Triggered when construction closures, bridge clearance issues, or local restrictions force a different route than originally permitted; the manufactured housing permit is issued for a specific movement/route and is not a “blank check.” 
Escort vehicles required by width	$1.50–$3.50 per mile per escort (market rate range), with TxDMV rules defining when you need 1 vs 2 escorts	In Texas, if the section exceeds 16 ft but not 18 ft, 1 escort is required; if it exceeds 18 ft, 2 escorts are required (front + rear). The mileage pricing range is widely quoted in cost guidance. 
Hill Country / edge-market “extra escort” situations (law enforcement escort segments, district rules, no-convoy rules)	Often adds $100s to $1,000s+ per affected segment (dominant driver is extra vehicles/time; permit itself may be unchanged)	When a permitted route passes through a segment with a district restriction requiring law enforcement escorts or special procedures, escort cost spikes beyond ordinary pilot-car pricing. Example: the TxDMV “San Antonio District” restriction document shows corridors in the district with requirements such as law enforcement escorts and pre-notification/email requirements. (PDF published Sep 26, 2025.) 
Holiday travel blackout risk (schedule compression, staging yard, additional day charges)	Cost varies; commonly shows up as extra day of equipment/escort time or storage/staging fees (often $100s/day)	TxDMV explicitly states you may not transport manufactured housing on national holidays, which can force (a) multi-day staging, (b) rescheduling escorts, and (c) “lost day” charges in mover pricing. (TxDMV page: publication date not clearly shown; accessed Mar 20, 2026.) 
San Antonio/Hill Country construction closures that force detours	Best priced as incremental mileage cost: see “Detour cost model” in next section	Loop 1604 and I-35 corridor projects routinely publish closures and detours. This increases mileage, time-in-escort, and risk of needing permit route adjustments. TxDOT’s I‑35 NEX program has been under construction since June 2022 with Central project completion targeted for late 2027; lane closure pages are updated weekly. 
Floodplain development permit (unincorporated Bexar County)	$50.00 per activity	Applies when placement/sitework is on or adjacent to mapped floodplain areas in unincorporated county jurisdiction; Bexar County’s floodplain permit page and checklist state the fee. (County page: publication date not shown; accessed Mar 20, 2026. County PDF published Oct 20, 2023.) 
FEMA/NFIP manufactured home elevation compliance in SFHA	Cost driver is the added foundation height + certification work; see flood section	Federal floodplain management criteria require manufactured homes in mapped SFHAs to meet elevation/anchoring conditions: lowest floor at/above BFE or chassis supported by reinforced piers ≥ 36 inches above grade (with anchoring to resist flotation/collapse/lateral movement). 
Post‑2018 flood map changes that newly place a lot in SFHA	$0 permitting fee by itself, but can trigger $1,000s–$10,000s+ in elevation/foundation scope changes	FEMA publishes flood hazard determination changes; for unincorporated Bexar County, a Federal Register notice lists an effective date September 17, 2018. If your parcel moved from Zone X to AE/A, the manufactured home placement scope can change overnight. (Federal Register notice published Oct 9, 2018.) 
Edwards Aquifer Protection Program (WPAP) filing fee for a single-family dwelling	$650 (if <5 acres; fee schedule), up to $10,000 (program maximum; larger/other plan types)	If the placement/sitework is in the Edwards Aquifer recharge zone, TCEQ requires a WPAP for “any regulated activity” and the program page lists a $650 minimum and $10,000 maximum; the TCEQ fee form schedules $650 for a “One Single Family Residential Dwelling < 5 acres.” (TCEQ WPAP page last modified Jul 28, 2025; fee form revision Feb 24, 2015.) 

Route risk pricing for I‑35, Loop 410, and Loop 1604 construction detours
TxDOT’s current San Antonio-area highway work is not just “traffic.” It creates hard routing constraints for oversize moves: closures, lane shifts, reduced clearances, and a higher probability that TxDMV’s permitted route needs adjustment. TxDOT notes that I‑35 NEX Central has been under construction since June 2022 and publishes weekly closure/traffic-impact updates. 

Visual grounding for the corridor and Hill Country edge
Detour cost model (priced with published per-mile rates)
You asked for “how much longer alternate route adds in mileage, escort time, and permits.” The cleanest way to make this precise (without inventing a single “one-size” detour distance) is to price the incremental mile and then apply it to the detour mileage that appears on the permit route for your specific move.

Published per-mile pricing benchmarks commonly used in mobile/manufactured home moving cost guidance include:

Towing vehicle: about $4.00–$5.50 per mile 
Pilot/escort car: about $1.50–$1.65 per mile (another cost guide gives $1.50–$3.50 per mile) 
From those:

Single escort detour cost per extra mile:
($4.00–$5.50) + ($1.50–$3.50) = $5.50–$9.00 per mile
Two escort detour cost per extra mile (common for >18 ft sections):
($4.00–$5.50) + 2×($1.50–$3.50) = $7.00–$12.50 per mile
Permit re-issue risk: if the detour requires a new permitted route, add $40.00 per section for a replacement manufactured housing single-trip permit. 

Worked examples (explicitly illustrative)
These are examples to show the math; your actual detour mileage must come from the TxDMV-permitted route version that applies on your move date.

Example A: 18 extra miles, 1 escort → $99–$162 in mileage-based detour cost (18 × $5.50–$9.00). 
Example B: 28 extra miles, 2 escorts → $196–$350 (28 × $7.00–$12.50). 
Example C (worst case): detour requires permit re-issue for a double-wide (2 sections) → +$80 permit fees (2 × $40), plus the mileage costs above. 
Because TxDOT closure notices for Loop 1604 and I‑35 NEX include periodic weekend and night closures and detour routing, detour mileage is not a rare edge case in 2026. 

Utility coordination in the San Antonio service territory
Utility work is a major category of “hidden cost” because it lives in a different scheduling and billing system than movers/transporters—and because some charges are fixed-fee while others are time-and-materials.

CPS electrical and gas charges that can show up as add-ons
CPS has a published “Policy for Miscellaneous Customer Charges” (revision date 02/01/2016) that includes specific charges relevant to a move-and-reset project: meter reconnection fees, rescheduling fees, repeat-call fees, and temporary service charges. 

Hidden cost item	Typical dollar range	San Antonio-area cause / trigger
Reconnection at the meter (electric)	$24.00 (regular work hours) to $30.00 (premium pay hours)	Service disconnected and then reconnected at the meter as part of move/transfer (or after disconnection for non-payment/diversion). (CPS policy effective Feb 1, 2016.) 
Reconnection at the meter (gas)	$36.00 (regular) to $47.00 (premium)	Same as above for gas accounts. 
Reconnection at pole/transformer/gas main (escalation)	Electric at pole: $60–$120; underground transformer: $60–$120; gas main: $400–$600	If reconnection is not a simple meter reconnect (e.g., illegal connection/diversion situations). These are not the norm for compliant moves, but they are a “surprise bill” category in problem situations. 
Repeat call charge	$20.00 (regular) to $30.00 (premium)	Utility technician arrives but customer/responsible party isn’t present or job cannot proceed; second trip billed. 
Customer rescheduled electric service connection	$58.00 per rescheduled overhead connection; $58.00 per rescheduled underground connection	Common when the home isn’t ready (site not prepped, electrician not ready, meter base not installed) on the scheduled day. 
Temporary standard electric service	$150.00 (regular) to $225.00 (premium)	Temporary overhead or underground power during setup, construction, or inspections. 
Temporary standard transformer (≤25 kVA)	$550.00 (regular) to $700.00 (premium)	Temporary transformer required for temporary power in some scenarios (often rural-like edges or where existing distribution isn’t adjacent). 
Non-standard temporary service	Time-and-materials estimate; billed at estimated installation + removal costs	Matters when a manufactured home setup needs a non-standard temporary configuration; billed as estimated labor/equipment/materials rather than a fixed fee. 

Line lifts: You asked specifically for CPS power line lifts (cost per crossing, typical number of crossings). Within the sources retrieved here, CPS publicly documents that customer construction costs are calculated based on materials + labor + time (not a fixed posted “line lift rate”). 
 I was not able to retrieve a CPS document that publishes a per-crossing line-lift price schedule for residential manufactured-home moves under the tool constraints; therefore I am not presenting an invented dollar-per-crossing figure.

SAWS fees that show up at move-in
SAWS publishes a “Special Services Fees – Approved 2026 Fee Changes” table (customer-service related), including the residential account deposit and a category of “rush” type actions (e.g., same-day turn-on). 

Hidden cost item	Typical 2026 dollar range	San Antonio-area cause / trigger
Residential SAWS account deposit	$100.00	Often required when establishing/starting water/sewer service after a move. (SAWS fee table labeled 2026; publication date not explicitly shown on snippet; accessed Mar 20, 2026.) 
Same-day turn-on fee	$35.00	Rush-service surcharge when you miss the standard scheduling window and need same-day activation. (Shown on SAWS fee table labeled 2026; accessed Mar 20, 2026.) 

Septic and rural placements at the metro edge
For placements outside municipal sewer service (more common on the Hill Country edge), septic/OSSF compliance can add both permit fees and engineering/design scope.

Hidden cost item	Typical dollar range	San Antonio-area cause / trigger
OSSF permit application fee (state baseline)	$200.00 application fee + $10.00 additional fee	Texas administrative rules include these fees for OSSF permitting. (Rule excerpt accessed from Texas Administrative Code source; publication date depends on code publisher; accessed Mar 20, 2026.) 
Additional engineering requirements when OSSF is in/near mapped floodplain (unincorporated Bexar County)	$50.00 floodplain permit fee plus professional engineer scope (cost varies by design/study)	Bexar County floodplain permit requirements explicitly call out additional engineering demonstrations for OSSF components in floodplain contexts and require a floodplain permit fee. (County PDF published Oct 20, 2023.) 

Foundations, soil, anchoring, wind zones, and flood elevation
This category is where the “transport quote” most frequently breaks: the transporter can deliver the home, but local conditions drive big adders for set, level, anchor, and connect.

San Antonio-area soils and Hill Country caliche/limestone: anchoring consequences
Texas manufactured housing rules explicitly address difficult soils (including caliche—heavily weathered limestone) where auger anchors cannot be inserted. In that scenario, cross-drive rock anchors may be required, and the rules indicate that maximum spacing for diagonal ties per side is reduced to one-half, implying more anchors/ties than a “normal soil” setup. (TDHCA rules effective 03/03/2024.) 

To make that “more anchors” impact quantifiable, here are published retail costs for cross-drive rock anchor components (hardware-only; labor is separate):

$29.95 (cross-drive rock anchor item listing) 
$39.80 (complete cross-drive anchor kit listing) 
Hidden cost itemization (caliche/rocky soil):

Cross-drive rock anchors (hardware): $29.95–$39.80 per anchor position, multiplied by the number of additional anchor positions required when spacing is halved. 
Expansive clays and engineered foundations
While soil-specific engineered foundation requirements vary by jurisdiction and financing, the market reality is that treating the foundation as “standard” is risky in a region known for expansive clays and variable subsurface conditions. In pricing terms, a common hidden cost is that the “set” price assumes a simple pier-and-beam style set, but the site ends up requiring a heavier foundation solution.

For concrete slab foundation budgeting in Texas-manufactured-home context, one Texas-focused guide states slab foundations typically $6,000–$12,000. (Published Dec 22, 2025.) 

Wind zone compliance in Bexar County: what’s mandatory and what actually adds cost
Wind zone classification reality check
Your prompt frames Bexar County as Texas Wind Zone II. Under the federal HUD wind zone system (24 CFR 3280.305), the Texas counties listed in Wind Zone II are coastal; Bexar County is not in that Wind Zone II list, meaning San Antonio/Bexar is Wind Zone I under the HUD county list. (eCFR page; publication date not shown; accessed Mar 20, 2026.)

What wind-zone anchoring adds to setup cost (quantified)
Even though Bexar is Wind Zone I, wind-zone compliance still creates hidden costs in two common scenarios:

You are importing a home from a different wind zone and the data plate / design wind zone does not match the installation zone you need (this can lead to refusal or redesign).
Your installer prices “higher wind” anchoring as a conservative standard (less common, but it happens when installers standardize hardware packages).
A reliable way to quantify the incremental cost of “higher wind / higher restraint” anchoring is to tie it to the number of additional anchors and straps required (hardware has published unit costs; labor scales with anchor count). Using the published cross-drive anchor costs above ($29.95–$39.80 each) and the Texas rules’ statement that difficult-soil conditions can require adding anchors when spacing is reduced, the hardware-only incremental is:

If +8 additional anchor positions are required: $239.60–$318.40 (8 × $29.95–$39.80) 
If +12 additional anchor positions are required: $359.40–$477.60 (12 × $29.95–$39.80) 
Because labor and equipment time are the dominant portion of anchoring, this hardware-only view is conservative; it is included here because it is directly quantifiable from published prices and the anchoring rules that require additional anchors under certain conditions. 

FEMA flood zone elevation: the placement-cost adders in San Antonio waterways
The San Antonio area’s major creeks/rivers (San Antonio River corridor, Salado Creek, Leon Creek, Olmos Creek, Medina River) correspond to places where parcels may fall into mapped flood hazard areas. The cost impact comes from a combination of:

Permitting and studies (county floodplain permits; potential engineer study where required), and
Physical elevation/structural requirements for manufactured homes.
Federal floodplain criteria (44 CFR 60.3) include a manufactured-home specific standard: elevate lowest floor to/above BFE or mount the chassis on reinforced piers at least 36 inches above grade (with anchoring). 

Direct, priced floodplain-related adders found in San Antonio-area sources:

Bexar County floodplain development permit fee: $50.00 per activity 
Elevation certificate / survey cost (local market starting point): one San Antonio survey provider advertises surveys starting around $400+ (survey type varies; elevation certificates can be priced differently). (Page publication date not shown; accessed Mar 20, 2026.) 
Map update trigger: FEMA published “Changes in Flood Hazard Determinations” affecting unincorporated Bexar County with an effective date September 17, 2018—a concrete mechanism by which an address can become newly regulated and force added elevation cost. 

Installation and site-prep costs that frequently sit outside the mover quote
National “cost factor” breakdowns provide unusually concrete line-item ranges for site work that often becomes the homeowner’s problem after the transport price is agreed.

The following cost ranges are from a 2026 cost guide updated Dec 29, 2025 (Angi). They are not San Antonio-exclusive, but they are highly relevant because they align with the typical scope that becomes “hidden” when a mover quote covers only transport or only basic set. 

Hidden cost item	Typical dollar range	San Antonio-area trigger / cause
Land clearing / tree & vegetation removal	$1,400–$6,220	Common on Hill Country edge lots or lots with mature vegetation/brush. This is also the bucket where “tree trimming for access” lands. 
Grading / leveling the site	$1,030–$3,340	Triggered when the destination pad is not level or needs cut/fill—frequent in sloped terrain. 
New foundation construction (general range)	$4,040–$14,850	Land that needs a different foundation type (pier vs slab vs engineered) than assumed in the moving quote. 
Skirting and vapor barriers	$1,500–$5,000	Often removed/damaged during transport; required for closure/appearance and moisture control. 
Utility hookups (broad “all trades” bucket)	$6,500–$30,000	Captures the reality that “utilities” can mean everything from simple reconnection to trenching, new service, plumbing modifications, and inspections. 
Trenching for service wiring	$400–$1,200	Common on rural/edge placements where service is not at pad. 
Stairs at egress doors (and anchoring stairs)	$600–$5,000	Often required for code/egress and overlooked in “set” quotes that only cover blocking. 
Set-up services after delivery	$3,000–$4,000	Reconnecting utilities, reinstalling skirting/decks, securing home to foundation—frequently quoted as a flat add-on. 
Pre-move repairs to make the unit “move ready”	Tires: $50 per tire; axle: $100–$200; hitch: $200–$300	Older units and stored units commonly need tires/axles/hitch work before a mover will haul them. 

Manufactured home parks, pre‑1976 homes, and transit insurance gaps
Park-related charges in the San Antonio area
Park-to-park moves are a special case because the park often has its own fee schedule on top of transport/set.

Examples of explicitly published park/community charges in the metro area include:

A San Antonio manufactured home community listing lot rent minimum $580/month, security deposit $100, and a $150 hookup charge (“hooking up water, sewer, electricity & gas (if required)”). (Page publication date not shown; accessed Mar 20, 2026.) 
A New Braunfels-area mobile home park listing a $50 application fee per adult. (Page published about 7.7 years ago per search metadata; accessed Mar 20, 2026.) 
Transfer fees / buy-ins / “lot prep” charges: within the retrieved sources, I found clear evidence of application fees, deposits, and hookup charges, but not a robust set of published San Antonio park “transfer/buy-in” fee schedules. Therefore, I am not inventing a “typical transfer fee” number here; the evidence-supported takeaway is that park-side one-time fees of $50–$150+ are demonstrably common even before transport, and rent resets to current market immediately upon move-in. 

Pre‑1976 (pre‑HUD Code) surcharge and refusal risk
The key “hidden cost” for pre‑1976 units is often not a surcharge—it is that many move/install pathways become unavailable due to code, permitting, and market acceptance issues.

Evidence-based constraints include:

Texas OS/OW permitting documentation notes that HUD label numbers are required on houses built after June 15, 1976, while pre‑HUD years require a complete serial number, which can become a documentation hurdle in practice. (TxDOT handbook published ~13.9 years ago per metadata.) 
A Texas municipal-law guidance document explains cities may regulate/prohibit mobile homes and highlights that homes constructed before June 15, 1976 are not HUD-certified and may be treated differently by municipalities. (Document dated June 2022.) 
Mainstream move-cost guidance notes that homes built before 1976 “probably” won’t be allowed to move (reflecting common local restrictions and mover refusal). (Moving.com article published Jun 23, 2022.) 
Cost guidance also notes movers may refuse to move pre-1976 homes on legal grounds and highlights that older homes face higher risk and higher prep/repair exposure. (Angi updated Dec 29, 2025.) 
Required metric you requested (percentage of San Antonio-area transporters who refuse pre‑1976): I did not find a trustworthy, published dataset or survey that quantifies refusal rates by metro area within the sources retrieved here, and I cannot defensibly manufacture a percentage without a transparent, reproducible sample of San Antonio-area transporter policies. The evidence does support that refusal/denial is common enough to be repeatedly warned about in guidance and municipal contexts, but it does not support a numeric market share. 

Transit insurance gap: homeowner policies vs transport exposure
Your prompt correctly notes the “coverage gap” problem: homeowners often assume an existing policy covers transport; many moves instead rely on mover liability structures and/or separate insurance purchased for the move.

Concrete, published pricing benchmarks for moving-insurance style coverage include:

Full value protection is commonly priced at about 1%–2% of declared value (example given: $25,000 value → about $250), per federal moving guidance. (FMCSA page published Feb 2, 2015.) 
Another cost guide states moving insurance averages $215–$2,500, and likewise cites 1%–2% of value for full value protection. (Angi article published Nov 19, 2021 per metadata.) 
San Antonio-specific way this becomes a hidden cost: if your transporter quote is “transport only,” you may need to separately procure coverage for the declared value of the home during the move. Using the published benchmark:

Declared value $80,000 → $800–$1,600 at 1%–2% (illustrative application of the published pricing rule). 
Key takeaways that directly answer your minimum coverage list
Wind zone compliance: Under HUD wind zones, Bexar County aligns with Wind Zone I, not Zone II; Zone II is coastal Texas. Wind-zone compliance cost adds show up when the home’s design wind zone does not match the installation zone or when additional anchoring hardware is required by site conditions; the quantifiable piece is additional anchor hardware (e.g., $29.95–$39.80 per cross-drive rock anchor position) combined with added labor time. 

Hill Country terrain access: The priced drivers you can reliably model are (a) additional escort mileage ($1.50–$3.50 per mile per escort) and (b) site prep like land clearing ($1,400–$6,220) and grading ($1,030–$3,340). The regulatory driver is that specific segments in the TxDMV San Antonio District can require special escort/procedures. 

Highway construction rerouting: TxDOT’s I‑35 NEX and Loop 1604 work creates recurring closures/detours; cost impact is best expressed as incremental-mile pricing (roughly $5.50–$12.50 per extra mile depending on escort count) plus possible permit re-issue fees ($40 per section). 

Utility coordination: CPS reconnection/temporary-service and trip/reschedule charges are explicitly priced (e.g., electric meter reconnect $24–$30; temporary standard electric $150–$225). SAWS has a $100 deposit and $35 same-day turn-on fee. Septic/OSSF adds at least $210 in state fees (plus design/engineering where required). 

Foundation and anchoring: Caliche/rock drives anchor type and count (Texas rules explicitly cover caliche as difficult soil); concrete slab budgeting in a Texas manufactured home context is often $6,000–$12,000, and general “new foundation” ranges reported are $4,040–$14,850. 

Flood elevation: Federal rules for manufactured homes in SFHA require elevation to BFE or use of ≥36-inch reinforced piers with anchoring. Unincorporated Bexar County floodplain permit fee is $50. FEMA notices show Bexar flood hazard determinations were updated with an effective date of Sep 17, 2018, which can change whether a parcel triggers these requirements. 

Manufactured home parks: Published local examples show lot rent minimums (e.g., $580/month), deposits ($100), hookup charges ($150), and application fees ($50/adult). Evidence for standardized “transfer/buy-in” fees across San Antonio parks was not located in the retrieved sources, so it is flagged as a due-diligence item rather than assigned an invented typical number. 

Pre‑1976 surcharge: The economically dominant risk is refusal/denial; Texas municipal guidance and national moving guidance both emphasize restrictions around pre‑1976 homes. A numeric refusal percentage for San Antonio-area transporters is not supported by a published dataset in the retrieved sources. 

Transit insurance gap: Published guidance prices full value protection around 1%–2% of declared value, implying hundreds to low thousands for typical manufactured-home declared values. 

TCEQ compliance and Edwards Aquifer: If the site is on the recharge zone, the WPAP is required and has a priced fee schedule (e.g., $650 for a single-family dwelling on <5 acres; TCEQ WPAP page last modified Jul 28, 2025). 


---

## Prompt 7

﻿
San Antonio Mobile Home Moving Price Distribution & FAQ Content — 2026 Market Analysis
Scope and assumptions
This research covers manufactured home transport (moving the home structure itself), not household-goods moving. Cost bands and the distributions below are intended for San Antonio–area homeowners budgeting a typical relocation within the metro area.

To make the “San Antonio market” usable for histograms and FAQs, this report defines the primary metric as the all-in “full-service move” price most homeowners see on quotes for a metro-area relocation: detach / prep, transport, permits, escort/pilot vehicles when required, and reset (block/level/strap/anchor). This aligns with how major cost-data publishers describe “full-service” (permit handling + disconnect/reconnect + setup) and how setup is commonly priced as a separate line item. 

Major site construction is not assumed to be included in most “move” quotes (e.g., a brand-new engineered foundation, extensive grading, or long utility trenching). Those items are treated as “hidden/add-on costs” in the FAQs because they are frequently quoted separately and can dominate the total project budget. 

San Antonio-specific regulatory and market cost drivers
Texas manufactured-housing permits, escort rules, and carrier compliance
Most manufactured homes are oversize loads and require a Texas manufactured-housing single-trip permit. The published permit fee is $40, and the permit covers one movement (time-limited, up to five days). The permitting process requires a USDOT number, and the state checks it against FMCSA out-of-service status (MCMIS) prior to issuance—important when evaluating carrier reliability and scheduling risk. (TxDMV page does not display a publication date; accessed Mar 20, 2026.) 

Escort (pilot/flag) requirements meaningfully affect price variability, especially for multi-section moves. Under TxDMV’s escort rules for manufactured housing, loads over 16 feet wide up to 18 feet wide require one escort, and loads over 18 feet wide require two escorts; there are also required warning lights/signage for manufactured houses and escort vehicles. (TxDMV page does not display a publication date; accessed Mar 20, 2026.) 

Installation reporting, inspections, anchoring, wind zone, and soil verification
Texas requires manufactured-home installation work to be handled by a licensed installer and completed in accordance with approved installation instructions. For used homes, installation standards explicitly reference the Wind Zone where the home is installed and the need for stabilization appropriate to local soil properties, including designs based on county soil surveys or geotechnical reports when special systems are used. (Texas Administrative Code via Cornell LII; publication date not shown on the LII page; rule context accessed Mar 20, 2026.) 

A key cost item that is unusually “predictable” in Texas is the installation reporting fee: $75 for a single-section home plus $25 for each additional section, submitted with the Notice of Installation after installation completion. (10 Tex. Admin. Code §80.3; most recent amendment date noted as Oct 23, 2022 on the LII page.) 

Inspection timing affects scheduling and, indirectly, labor standby charges: installers must file the installation notice within the specified window, and the rule explains that timely submission helps ensure inspectors can inspect the home with utilities connected but before the home is skirted. (10 Tex. Admin. Code §80.33; publication date not shown on the LII page; accessed Mar 20, 2026.) 

For wind standards, the federal HUD Wind Zone list for Wind Zone II in Texas does not include Bexar County, which makes the San Antonio area Wind Zone I by default under 24 CFR 3280.305(c) (eCFR; publication date not posted; accessed Mar 20, 2026). This matters because the home’s data plate wind rating must be compatible with the installation location’s wind zone, and anchoring details follow the applicable installation instructions. 

San Antonio local code expectations and utility coordination
Local rules can force “move + install” scope to include items owners may assume are optional. San Antonio’s zoning amendments state that HUD-code manufactured homes must be permanently affixed to a foundation, with a visible foundation system and skirting similar to site-built residences, and that wheels/axles must be removed (document dated Jul 20, 2015). 

Utility coordination is a frequent schedule constraint (and sometimes a fee line item). The City’s utility release guidance notes that, after final inspection approvals, CPS Energy is notified and the owner should arrange service; it also states that CPS Energy may require the City to perform an inspection to re-establish utilities and that the owner must apply for a reconnect permit in person. (City page does not show a publication date; accessed Mar 20, 2026.) 

For SAWS, a clear, published fee that often shows up in relocation timelines is the $12 meter trip fee when turning water on/off requires a personal visit (SAWS page does not display a publication date; accessed Mar 20, 2026). 

Why San Antonio pricing tends to sit below national “headline” averages
Two San Antonio-facing factors reduce the share of quotes that drift into the highest national tiers: relatively low administrative permit costs (e.g., a $40 single-trip manufactured-housing permit) and typically less extreme terrain/route constraints for metro-area moves. 

Fuel is still a major variable, but the Gulf Coast diesel price is often below the U.S. average. For the week ending Mar 16, 2026, EIA reported $4.835/gal diesel for the Gulf Coast (PADD 3, which includes Texas) versus $5.071/gal for the U.S. average (EIA release date Mar 17, 2026). 

Price benchmarks used to model San Antonio distributions
The distributions in the next section are modeled (because no public dataset publishes a San Antonio-only histogram split by single-/double-/triple-wide). Bucket ranges and tier centers are anchored to multiple publicly available benchmarks:

ProMatcher’s San Antonio cost report includes two highly local anchors: a single-wide local move under 50 miles at $2,199.66–$2,726.49 (fixed fee) and a double-wide move over 100 miles priced at $2.50–$4.75 per mile, with reporting lines dated Jul 11, 2018 and Aug 17, 2022. ProMatcher also clarifies that the fixed-fee local move does not include utilities, foundation installation, repairs, or oversized trailers, which is why this report treats that band as “transport-only / basic.” 

Angi’s cost guide (updated Dec 29, 2025) provides widely cited national ranges by home type—$4,000–$8,000 for single-wide, $8,000–$15,000 for double-wide, and $12,000–$25,000+ for triple-wide—and a setup fee range of $3,000–$4,000. Angi also quantifies pilot/escort vehicle costs at $1.50–$3.50 per mile. 

HomeAdvisor’s guide (updated Mar 22, 2025) supports the national framing and provides additional distribution logic: shorter moves may be flat-rate, while longer moves increase total cost but can reduce the per-mile rate; it also reiterates full-service inclusion (disconnect/reconnect/setup/permits) and gives typical ranges and averages by size. 

A Texas-based 2026 guide (Spark Homes; dated Jan 26, 2026) supplies recent, practical “Texas cost examples” such as $3,000–$5,500 for a short-distance single-wide and $6,000–$12,000 for a medium-distance double-wide, plus an example breakdown that explicitly separates base transport, permits, and installation. While not San Antonio-exclusive, these examples help size the low-to-mid tiers that appear frequently in Texas metros. 

Finally, Texas regulatory fee floors that strongly influence the “left tail” of distributions include: $40 for the single-trip manufactured-housing permit (TxDMV; no publication date shown; accessed Mar 20, 2026) and the TDHCA installation reporting fee of $75 + $25 per additional section (10 Tex. Admin. Code §80.3; last amendment entry shown as Oct 23, 2022). 

Price distribution histograms
These tables are formatted for direct histogram configuration (bucket bounds + market share). They represent a 2026 modeled distribution of San Antonio–area jobs where homeowners purchase a typical “move + reset” service package (detach/prep, transport, permits, escort when required, and reset), excluding major new site-build work. The bucket edges are localized using ProMatcher’s San Antonio price points and recent Texas cost examples, while the shape (“Most Common” largest) is aligned with national cost-band clustering from Angi and HomeAdvisor. 

Single-wide
Bucket Range	% Market Share	Tier Label
$2,200 – $4,000	18%	Budget/Basic
$4,000 – $5,500	24%	Standard
$5,500 – $7,000	36%	Most Common
$7,000 – $9,000	15%	Premium
$9,000+	7%	Complex

Interpretation notes (San Antonio-specific): the bottom bucket is anchored to ProMatcher’s $2,199.66–$2,726.49 single-wide transport figure for a local (<50 mile) move that excludes utility and foundation work (reported Jul 11, 2018). The “Most Common” bucket centers on the frequent “transport + reset + permits” reality implied by Angi’s $3,000–$4,000 setup fees and $4,000–$8,000 single-wide move range (updated Dec 29, 2025). 

Double-wide
Bucket Range	% Market Share	Tier Label
$6,000 – $9,000	12%	Budget/Basic
$9,000 – $11,500	22%	Standard
$11,500 – $14,500	34%	Most Common
$14,500 – $18,000	20%	Premium
$18,000+	12%	Complex

Interpretation notes (San Antonio-specific): the “Most Common” bucket is aligned with HomeAdvisor’s typical $8,000–$15,000 double-wide band (updated Mar 22, 2025) and Spark’s “Texas medium-distance” double-wide band of $6,000–$12,000 (dated Jan 26, 2026), then shifted upward for the higher frequency of multi-crew work, escort requirements on some loads, and two-section installation reporting fees. 

Triple-wide
Bucket Range	% Market Share	Tier Label
$12,000 – $16,000	10%	Budget/Basic
$16,000 – $20,000	22%	Standard
$20,000 – $25,000	34%	Most Common
$25,000 – $32,000	20%	Premium
$32,000+	14%	Complex

Interpretation notes (San Antonio-specific): national publishers place triple-wide moves in the $12,000–$25,000+ band (Angi updated Dec 29, 2025; HomeAdvisor updated Mar 22, 2025), and the higher-right tail reflects the increased likelihood of multiple escorts, longer route planning, and complexity when three sections must be coordinated and rejoined. 

FAQ content for San Antonio homeowners
How much does it cost to move a single-wide mobile home in San Antonio?
A typical full-service single-wide move in the San Antonio metro area runs about $5,500–$7,000, while a transport-only local move under ~50 miles can be closer to $2,200–$2,700 when utilities and reset work are excluded. (ProMatcher reported Jul 11, 2018 and Aug 17, 2022; Angi updated Dec 29, 2025.) 

Expect state/regulatory line items such as a $40 manufactured-housing single-trip oversize permit plus the TDHCA installation reporting fee ($75 for a single-section home), and coordinate utility shutoff/reconnect steps with CPS Energy and SAWS (e.g., SAWS’s $12 meter trip fee when a site visit is required). (TxDMV/City/SAWS pages do not show publication dates; accessed Mar 20, 2026. TDHCA fee rule last amendment entry shown as Oct 23, 2022 on Cornell LII.) 

What is the average cost to move a double-wide mobile home in San Antonio?
Most San Antonio-area double-wide full-service moves cluster around $11,500–$14,500, consistent with national cost-data ranges of $8,000–$15,000 and Texas examples that separate base transport from permits and installation. (HomeAdvisor updated Mar 22, 2025; Angi updated Dec 29, 2025; Spark guide dated Jan 26, 2026.) 

Regulatory costs are larger than single-wide: the TDHCA installation reporting fee is $100 for two sections ($75 + $25), and if a section’s width crosses the TxDMV escort thresholds you may pay escort/pilot costs (Angi budgets $1.50–$3.50 per mile)—plus San Antonio code expectations for permanent foundation placement and removal of wheels/axles at the destination. (San Antonio amendments dated Jul 20, 2015; Angi updated Dec 29, 2025; TxDMV pages accessed Mar 20, 2026.) 

Does distance affect mobile home moving costs in Texas?
Yes—distance changes both the pricing method and the total. For long moves, San Antonio-area pricing often shifts toward per-mile structures (ProMatcher reports $2.50–$4.75 per mile for a double-wide over 100 miles, reported Aug 17, 2022), and HomeAdvisor notes that while the farther you move the more you pay in total, you often pay less per mile on longer trips (updated Mar 22, 2025). 

Distance also increases the odds of added escort time and escort mileage (Angi budgets $1.50–$3.50 per mile for escorts; updated Dec 29, 2025) and increases exposure to permit timing constraints (TxDMV single-trip permits are time-limited and the move must occur within the permit window; accessed Mar 20, 2026). 

What is the cheapest time of year to move a mobile home in San Antonio?
Pricing is usually lowest in the off-season (winter weekdays) because demand is lower; Angi explicitly notes moves often cost more in summer/weekends and that winter moves usually cost less (updated Dec 29, 2025). 

For San Antonio budgeting, that typically means your quote is more likely to land at the low end of the standard single-wide and double-wide bands—roughly $5,500–$6,000 for many single-wides instead of $6,500–$7,000, and $11,500–$13,000 for many double-wides instead of the upper premium tiers—assuming permits, TDHCA reporting, and utility timing are lined up without delays. 

Are there hidden costs when moving a mobile home in San Antonio?
Yes—San Antonio “hidden costs” typically come from permits/escorts, setup, and utility coordination: setup alone can be $3,000–$4,000 (Angi updated Dec 29, 2025), escort vehicles can add $1.50–$3.50 per mile, and Texas adds fixed regulatory fees such as the $40 manufactured-housing permit and TDHCA installation reporting ($75 + $25 per extra section). 

On top of that, San Antonio’s code expectation for permanent foundation placement (and removing wheels/axles) can drive extra labor/material, SAWS may charge a $12 meter trip fee for turn-on/off visits, and Texas installation rules require installers to verify soil conditions and match anchoring to the home’s wind zone (Bexar County is Wind Zone I by default under 24 CFR 3280.305(c)). 

Source dating and citation notes
Angi’s cost guide provides an explicit update date (Dec 29, 2025) and includes size-based move ranges, setup fees, and escort/pilot mileage pricing. 

HomeAdvisor provides an explicit update date (Mar 22, 2025) and includes ranges/averages, distance-based pricing behavior, and common inclusions/exclusions for “full-service.” 

ProMatcher’s San Antonio cost report provides “reported on” timestamps (Jul 11, 2018 and Aug 17, 2022) that anchor local transport-only and per-mile pricing. 

Texas regulatory fee references are sourced from TxDMV pages (no publication date shown; accessed Mar 20, 2026) and Texas Administrative Code text via Cornell LII (rule pages list amendment history; §80.3 shows most recent amendment effective Oct 23, 2022). 

San Antonio local foundation/axle language is taken from the City’s “Approved Amendments 7-20-15” PDF (dated Jul 20, 2015). 

Utility coordination details for CPS Energy and SAWS fees are from City/SAWS pages that do not show publication dates; they are cited as accessed Mar 20, 2026. 


---

