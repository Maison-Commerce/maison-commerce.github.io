# Feedwizrd LP — Design Fix Prompt (v2, mapped to the live wireframe)

**Wireframe reviewed:** `Feedwizrd Landing Wireframe.dc.html` (1280px, sections `s1`–`s12`, Inter + IBM Plex Mono, Polaris-styled app mockups)
**Feedback source:** client Loom revision video (11:56), 15 numbered points
**Use:** paste PART 2 into Claude Design. PART 1 is the read-before-you-touch-anything summary. PART 3 is the QA checklist.

Naming corrected from the file: the product is **Feedwizrd** (one word, no space, no "e" in "wizrd"). The chat widget is currently **"Feedwizrd assistant"**, not "AI Bot" — point 11 is a rename *from* "assistant", not from "bot".

---

## PART 1 — WHAT THE FEEDBACK ACTUALLY MEANS FOR THIS FILE

The client's 15 points collapse into **one structural problem plus 11 local fixes**.

**The structural problem:** this wireframe is built end-to-end on *product-level profit after COGS, payment fees, shipping, returns and ad spend*. That is the spine of `s1` (hero headline + Profit column + "Recommended action"), the whole of `s3` (the `waterfall` array), `s4` (sort by profit, "Losing money" filter, "Where the money went" panel), `s5` (all three stage mocks), `s6` (group 1 "See the truth"), `s9` (case quote + `$522` metric), `s11` (FAQ 1, 2, 7) and `s12` (final CTA).

The client says this is the wrong product. Feedwizrd is a **Google Ads product-feed performance tool**. The metric is **ROAS**. COGS is an optional side note most users never fill in, and **payment fees, transaction fees, shipping and fulfilment must be removed from the page entirely**.

So `s3` doesn't get edited — it gets rebuilt — and the profit framing has to be re-angled in eight other sections.

**Watch for this trap:** `s3`'s entire "aha" is *Google says 2.2 ROAS is fine, but you actually lost $522*. Delete profit and that aha vanishes. Don't leave a hole. The replacement aha the client gave is: *Google and Shopify give you account-level numbers; they don't tell you **which feed items** are dragging ROAS down, across which time window, what to change, or whether the change worked.* Build `s3` around that.

**Also note:** the wireframe already does several things the client asked for — the `ASSET:` annotations already flag that real screenshots are needed (point 1), the chart already goes 2.2 → 3.1 (point 13), the FAQ already has 12 written Q&As (point 8). Those need *upgrading*, not building from scratch.

---

## PART 2 — THE PROMPT

```
Revise the existing Feedwizrd landing wireframe (sections s1–s12). Keep the layout
skeleton, the Inter / IBM Plex Mono type system, the warm off-white canvas
(#fdfbf8 / #faf8f5), the 1280px grid, and the Polaris-styled app mockups. Do not
redesign from scratch. Apply the changes below — every one comes from direct
client feedback on this file.

═══════════════════════════════════════════════════════════════
0. GLOBAL REPOSITIONING — DO THIS FIRST, IT TOUCHES 9 SECTIONS
═══════════════════════════════════════════════════════════════
This page is currently about PRODUCT PROFIT. It must be about GOOGLE ADS PRODUCT
FEED PERFORMANCE, measured in ROAS.

Feedwizrd scrapes Google Ads data into a dashboard. From there the merchant
analyses their FEED across 7/14/30/60/90-day windows, gets concrete feed
suggestions from the Feedwizrd Agent, applies them in one click, and the app
monitors whether ROAS actually improved.

REMOVE ENTIRELY from copy, tables, mockups and charts:
  - payment fees, transaction fees
  - shipping & fulfilment costs
  - returns as a cost line
  - "product profit", "profit per product", any P&L waterfall
COGS may survive only as a single optional footnote-level mention ("you can add
cost of goods if you want to — most merchants don't need to"). It is never a
headline, a column, a filter, or a proof point.

LANGUAGE RULE: the object of every sentence is the FEED, not the PRODUCT.
"Analyse your feed", not "analyse your product". Better feed → better Google Ads
performance → higher ROAS → more revenue on the same spend.

AUDIENCE: Shopify dropshippers running Google Shopping. 80–90% sell FASHION.
Every product name in the file is currently home & garden and must be replaced
with apparel/accessories:
    Linen Cushion Cover      → e.g. Oversized Wool Coat
    Ceramic Planter 12cm     → e.g. Ribbed Knit Midi Dress   (appears ~8 times)
    Brass Watering Can       → e.g. Leather Chelsea Boot
    Rattan Basket L          → e.g. Satin Slip Skirt
    Stoneware Mug Set        → e.g. Cropped Denim Jacket
    Terracotta Pot 20cm      → e.g. Linen Blend Shirt
    Jute Doormat             → e.g. Chunky Sole Sneaker
Also update the s5 "Fix" stage: suggested title must be an apparel title and
product type must be "Apparel & Accessories > Clothing > …", not
"Home & Garden > Pots & Planters". Update case-study store descriptors in s9
from "Home & garden store" / "Pet accessories store" to fashion stores.

═══════════════════════════════════════════════════════════════
1. SECTION s3 — REBUILD ("Problem proof — the product ROAS hides")
═══════════════════════════════════════════════════════════════
Current: left column "What Google & Shopify show" (Revenue / Ad spend / ROAS 2.2
/ Conversions) vs right column "What Feedwizrd calculates" — a 6-line cost
waterfall ending in "Product profit − $522". The client says this does not
reflect the real dashboard at all. Rebuild it.

KEEP: the two-column "this vs that" composition, the section rhythm, the
      disclaimer footnote pattern.
KILL: the entire `waterfall` array and the − $522 figure.

New headline direction (write your own, this is the argument):
  "Your account ROAS looks fine. Three products in your feed are dragging it down."

LEFT — "What Google & Shopify show": keep as-is (Revenue, Ad spend, ROAS 2.2,
Conversions) and keep the verdict line, re-angled to "Account level. Looks
acceptable. Tells you nothing about which feed items to fix."

RIGHT — "What Feedwizrd shows" — replace the cost waterfall with the product's
three real capabilities, as three stacked mini-panels:
  a) WINDOWS — the same product's feed performance across 7 / 14 / 30 / 60 / 90
     days, revealing a decline the account-level number hides.
  b) SUGGESTION — a concrete Feedwizrd Agent suggestion with current value →
     suggested value → expected impact. (Real example pattern from the app:
     "Raise bid on [product] by 8%".)
  c) CHANGE MONITOR — the same product after the change, showing ROAS before vs
     ROAS after, so the merchant knows whether it worked.

ROAS COLOUR TREATMENT IN s3 (client point 2):
The "2.2" in the left column currently renders as neutral body text. It must read
as NOT GOOD — but as a warning, not a failure, so use AMBER here (red is reserved
for the s9 case study).
Reuse the existing badge-chip pattern already used for the negative state
(bg #fed3d1 / fg #8e1f0b) but in Polaris warning tokens:
    WARN = { bg: "#ffd79d", fg: "#5e4200" }
Apply as a shaded chip/row behind the 2.2 value, amber value text, plus a small
down-arrow or warning glyph. Do not let green anywhere near this number.

═══════════════════════════════════════════════════════════════
2. SECTION s1 — HERO
═══════════════════════════════════════════════════════════════
- Headline "Know which products make money. Fix the ones that do not." → rewrite
  to feed/ROAS. Direction: "Know which products drag your ROAS down. Fix the feed
  in one click."
- Subhead currently reads "…shows profit for every product after COGS, fees and
  ad spend…" → rewrite around feed performance, agent suggestions, one-click
  apply, and before/after monitoring. Drop "after COGS, fees and ad spend".
- Mockup table columns are `Product | Revenue | Ad spend | ROAS | Profit`.
  Drop the Profit column. Lead with ROAS — make it the widest, boldest column,
  with a trend indicator per row. Suggested set:
  `Product | Ad spend | Clicks | Sales | ROAS ▾`
- The "Recommended action" footer currently reads "Exclude 'Ceramic Planter 12cm'
  from Shopping — losing $12.70 per order after costs." → replace with a feed
  suggestion in the app's real voice, e.g. "Feed title missing colour and
  material terms on [fashion product] — ROAS 1.4 over 30 days."
- Products in `heroRows` must be fashion, with real images present. No empty
  24×24 grey image squares and no "no image synced" placeholder states anywhere.

═══════════════════════════════════════════════════════════════
3. SECTION s4 — "One morning. One decision." (client point 10)
═══════════════════════════════════════════════════════════════
- "Sort: Profit, low to high" → "Sort: ROAS, low to high".
- Drop the Profit column from the demo table; make ROAS the hero column.
- The three filter chips are currently profit-defined. Redefine by feed
  performance:
    "All products"              → keep
    "Losing money"              → "Underperforming ROAS"
    "Spending, barely selling"  → keep the concept, redefine as spend with almost
                                  no clicks/sales; keep the internal "zombie
                                  filter" note.
  Rewrite each filter hint accordingly — remove all references to "cost of goods,
  fees, shipping, returns".
- THE 7 / 14 / 30 / 60 / 90 DAY CHIPS MUST NOT LOOK CLICKABLE. Render them as a
  static dashboard state: no cursor:pointer, no hover, no active/inactive
  contrast that implies a toggle, no button affordance. One window is simply
  shown as selected. (Same for the hero's window chips in s1.)
- The right-hand detail panel's third state is "Where the money went" + the cost
  waterfall. Replace with the suggestion detail: current value → suggested value
  → expected impact → Apply. The wireframe state labels ("All products / Losing
  product selected / Profit calculation expanded") become
  ("Feed overview / Item selected / Suggestion detail").
- Reframe the section promise: this is a dashboard for analysing the WHOLE FEED,
  not for inspecting one product.

═══════════════════════════════════════════════════════════════
4. SECTION s5 — "Find it, fix it, then check what changed."
═══════════════════════════════════════════════════════════════
The three-stage structure is good — keep it. Restate each stage in feed/ROAS terms:
  FIND   — mock lines currently end "Product profit − $522". Replace the line set
           with: Ad spend / Clicks / Sales / ROAS (amber, underperforming).
  FIX    — keep the before/after feed-value preview, switch the example to an
           apparel title and apparel product type. Emphasise that the Agent wrote
           it and the merchant applies it with ONE CLICK. Change the primary CTA
           from "Approve change" to "Apply" or "Apply in one click".
  VERIFY — mock lines currently "Product profit before/after". Replace with
           "ROAS before − 2.2" / "ROAS after − 3.1" / "Window · 30 days" /
           "Change log · feed title, applied by you". This is the Change Monitor.
Note: this section's red shaded treatment (bg #fed3d1 / fg #8e1f0b) is the pattern
the client explicitly pointed to as correct — it is the reference for the amber
treatment in s3 and the red treatment in s9.

═══════════════════════════════════════════════════════════════
5. SECTION s6 — capability groups
═══════════════════════════════════════════════════════════════
Re-label to feed/ROAS language:
  "Product-level profit calculation" → "Product-level feed performance"
  "Full ROI and profit tracking"     → "ROAS tracking across feeds and markets"
  "Performance dashboard"            → keep
  "AI feed improvement drafts"       → "Feedwizrd Agent suggestions"
This is also a natural home for the multi-market worldview motif (see §9).

═══════════════════════════════════════════════════════════════
6. SECTION s7 + s2 + s12 — "NO CUSTOM DEVELOPMENT NEEDED" (points 5 & 6)
═══════════════════════════════════════════════════════════════
The phrase "no tracking code" appears in FOUR places. Replace all of them with
"No custom development needed":
  1. s7 subhead: "…authorize Google Ads. No tracking code goes on your storefront."
  2. s2 reassurance strip, item 3: title "No tracking code" / note "Nothing added
     to your storefront theme."
  3. s7 setupFacts[0]: k "No tracking code" / v "Nothing is installed on your
     storefront theme."
  4. s12 CTA subhead: "No tracking code, no automatic changes."
Keep the "official Shopify and Google flows" proof point in s7 — that stays.

═══════════════════════════════════════════════════════════════
7. SECTION s8 — DELETE THE MERCHANT CENTER ROW (point 7)
═══════════════════════════════════════════════════════════════
In the permissions table, delete this row entirely:
    { scope: "Merchant Center feed", read: "Yes", change: "Attribute values",
      never: "Account settings" }
Nothing in the product happens inside Merchant Center. Remove the row, re-balance
the table so it doesn't read as short, and check no other copy references
Merchant Center.

═══════════════════════════════════════════════════════════════
8. SECTION s9 — CASE STUDY: REWRITE THE ARC (point 13)
═══════════════════════════════════════════════════════════════
The client's words: too clinical, too transactional, skips the emotional journey.
The current quote — "The planter was our best seller on paper. Feedwizrd showed it
cost us $12.70 an order — and the AI wrote the fix for me" — is exactly the
pattern to kill.

Replace the four `caseSteps` with a FIVE-beat narrative, in this order:
  1. PAIN     — "His Google Ads performance was sliding and he couldn't see why."
                Declining, not merely "acceptable". This is the emotional hook.
  2. TRIAL    — "He tried Feedwizrd."
  3. INSIGHT  — "For the first time he could see what was actually dragging his
                product feed down."
  4. ACTION   — "The Feedwizrd Agent wrote the concrete fixes. He applied them
                WITH ONE CLICK." One-click must be explicit — it is the proof point.
  5. RESULT   — "ROAS 2.2 → 3.1 over the next 30 days."
Rewrite the pull quote in the merchant's voice around that arc. Two things must
land above all else: it was HANDS-OFF (the Agent did the thinking, not him) and
it was ONE CLICK.

NUMBERS AND CHART — make the improvement feel dramatic:
- Lead with the ROAS numbers. They are the headline of the section, set large,
  not buried in the metric strip at the bottom.
- MAKE THE BEFORE WORSE. The before series is currently flat at
  [2.2, 2.1, 2.3, 2.2, 2.0, 2.2] and rendered in neutral grey #d9d9d9. It must
  (a) visibly DECLINE, to match the new pain beat — e.g. [2.9, 2.7, 2.6, 2.4,
  2.3, 2.2] — and (b) be RED, not grey: bars in a muted red, "Before · 2.2 ROAS"
  label in the negative token (#8e1f0b).
- The after series stays the improvement and goes GREEN (the refined green from
  §9, not the mint #cdfee1). The client confirmed the after-state green is right.
- The `chartDelta` badge "2.2 → 3.1" is the most important object in the section:
  enlarge it, set the numbers in IBM Plex Mono at display size, red → green.
- Metric cards: "$522 / Monthly loss identified on one product" must go. Replace
  the three with ROAS-led, EcomClaw-style numbers, e.g.:
      "2.2 → 3.1"   Google Ads ROAS, account level
      "+41%"        Revenue on the same ad spend
      "1 click"     Merchant effort to apply the Agent's fixes
  ("1 approval" → "1 click".)
- Apply the same rewrite to all three cases in the carousel, and to the chat
  widget's canned answers.

═══════════════════════════════════════════════════════════════
9. VISUAL LANGUAGE — REFINE THE GREEN, ADD THE WORLDVIEW MOTIF (point 4)
═══════════════════════════════════════════════════════════════
The client: "the green elements look a little bit cheap… even though here you're
using very professional, very premium looking elements. Try to also use this in
here."

Offending greens:
  - #cdfee1 / #0c5132 — the mint positive badge, used on profit badges and the
    ROAS delta chip. Reads as default Polaris, not as brand.
  - #3db85c with a rgba(61,184,92,.15) glow ring — the status dot in s5. This is
    the cheapest element on the page.
Fix: replace with a deeper, more restrained green — a considered brand green in
the same tonal family as the warm neutral palette (#fdfbf8 / #f3f0ea / #2c2420),
not a bright SaaS mint. Use green only as a positive-state signal (improved ROAS,
applied change, agent online); never as decoration, never as a glow, never as a
filled pill floating on its own. The best elements on the page are the quiet
bordered cards and the `#2c2420` dark chips — bring the greens up to that level.

WORLDVIEW MOTIF: add a Shopify-style dotted-globe / point-mapped world graphic
where each dot represents customers in a market (China, Germany, Netherlands…).
Rationale given by the client: many users sell into multiple markets and analyse
their feed per market, and that isn't represented anywhere on the page today.
Place it as a premium background/support element — best homes are the s6 "Scale
the workflow" group and the hero or s7 supporting area. Use it to carry the
multi-feed / multi-market / multi-currency story that currently only exists as
plain bullet text.

═══════════════════════════════════════════════════════════════
10. SECTION s12 — THE CHAT WIDGET → "FEEDWIZRD AGENT" (point 11)
═══════════════════════════════════════════════════════════════
- Rename "Feedwizrd assistant" → "Feedwizrd Agent".
- Replace the status line "Usually replies in a few minutes" with a status dot +
  "Online" (using the refined green, no glow ring).
- Put the Feedwizrd logo mark in the widget header, in place of the generic avatar.
- Visual reference: the EcomClaw "EcomClaw Agents" widget pattern — branded,
  product-like, professional; not a generic support chat bubble.
- The three canned Q&As are profit-based. Replace:
    "How is profit calculated?" → "How does Feedwizrd find what's hurting my ROAS?"
    "Will it change my products?" → keep, re-angle to feed changes + one click
    "What does it cost?" → keep
  Remove "payment fees, shipping, returns" from the answer copy.

═══════════════════════════════════════════════════════════════
11. SECTION s12 — MICRO-COPY (point 9)
═══════════════════════════════════════════════════════════════
"Find the product costing you money before another week of ad spend does."
→ "Find the products costing you money before another week of ad spend does."
The client likes this line; it is a pluralisation, not a rewrite. Keep the rhythm.
Ensure the section's supporting copy underneath is feed/ROAS-framed, not profit.

═══════════════════════════════════════════════════════════════
12. SECTION s11 — FAQ COPY (point 8)
═══════════════════════════════════════════════════════════════
The client can only see one open answer at a time and said "we don't know what
the copy is in there — if you can provide that, we can guide you." Two jobs:
  a) Export all 12 Q&As as a flat, readable copy sheet for client review
     (all-expanded state or a separate copy doc), so they can approve the words.
  b) Rewrite the three that contradict the repositioning:
     - "How is Feedwizrd's profit calculated?" — remove or replace entirely with
       "How does Feedwizrd decide what to change in my feed?"
     - "How is this different from the numbers in Shopify and Google Ads?" —
       re-angle from profit-joining to feed-item-level ROAS visibility.
     - "What does AI feed improvement change?" — rename to the Feedwizrd Agent,
       emphasise one-click apply and the change monitor.
     Strip "payment and transaction fees, shipping cost, returns" from every answer.

═══════════════════════════════════════════════════════════════
13. MOCKUP FIDELITY (points 1 and 12)
═══════════════════════════════════════════════════════════════
Every app mockup in this file is invented, Polaris-styled, and annotated
"ASSET: real screenshot…". The client has now given view access to the live tool
and is loading real data into it.
- Replace the invented tables with the REAL SaaS UI: real column names, real
  table structure, real chart styling, real suggestion and change-monitor screens.
- Zero placeholder artefacts: no "no image synced", no empty grey image squares,
  no lorem rows, no skeleton states.
- Populate with realistic fashion products and realistic numbers.
- Where a screenshot isn't available yet, build to the real UI's structure rather
  than inventing a new visual language, and keep the ASSET annotation on that
  block only.

═══════════════════════════════════════════════════════════════
DELIVERABLE
═══════════════════════════════════════════════════════════════
Return the revised wireframe with all of the above applied, section by section.
Flag any block still waiting on a real screenshot. Deliver the rewritten FAQ and
case-study copy as a separate reviewable copy sheet alongside the design.
```

---

## PART 3 — REVISION CHECKLIST (Loom points 1–15 → this file)

| # | Loom | Client's point | Where it lives in the file | Status |
|---|---|---|---|---|
| 1 | 00:15 | Mockup should not be a prototype | All `ASSET:` blocks in s1, s4, s5, s9; empty 24×24 image squares in `heroRows` / `demoRows` | ☐ |
| 2 | 00:59 | 2.2 ROAS must read as not good — yellow | `googleView` ROAS row in s3; use WARN `#ffd79d`/`#5e4200`, mirroring the NEG `#fed3d1`/`#8e1f0b` pattern from s5 | ☐ |
| 3 | 01:40 | Feed performance, not profit per product | Global; `PRODUCTS` array → fashion; kill Ceramic Planter 12cm (≈8 instances) | ☐ |
| 4 | 03:00 | Green looks cheap; add worldview style | `#cdfee1`/`#0c5132` badges, `#3db85c` glow dot in s5; add dotted-globe motif in s6 / hero | ☐ |
| 5 | 03:55 | "No tracking code" → "no custom development needed" | s7 subhead + `setupFacts[0]`, s2 `reassurance[2]`, s12 CTA subhead — 4 places | ☐ |
| 6 | 04:09 | Setup section wording | s7, keep official Shopify + Google flows | ☐ |
| 7 | 04:23 | Delete Merchant Center | `permissions` row 6 in s8 | ☐ |
| 8 | 04:41 | FAQ texts needed | s11 — export all 12 Q&As for review + rewrite FAQ 1, 2, 7 | ☐ |
| 9 | 04:49 | "product" → "products" | s12 headline | ☐ |
| 10 | 04:55 | "One morning" mockup doesn't match | s4 — ROAS sort, drop Profit column, redefine filters, **7/14/30/60/90 not clickable**, whole-feed framing | ☐ |
| 11 | 05:43 | "Feedwizrd Agent", logo, Online status | s12 chat widget (currently "Feedwizrd assistant / Usually replies in a few minutes") + `CHAT` array | ☐ |
| 12 | 05:50 | Mockups don't match the software | All mockups — coordinate with Ruben; decide whether the SaaS UI also moves toward the LP (Kasper) | ☐ |
| 13 | 06:45 | Case study too clinical | s9 — 5-beat arc, before chart red + declining, after green, "1 approval" → "1 click", kill the `$522` metric | ☐ |
| 14 | 08:35 | Final copy reminder | Global — remove payment/transaction fees, shipping, returns; COGS optional footnote only | ☐ |
| 15 | 09:09 | Google/Shopify comparison doesn't reflect reality | s3 — rebuild right column as windows → suggestions → change monitor; delete the `waterfall` array | ☐ |

### Blocked on the client / team (not design work)
- **Live tool access** — Ruben to hold wider access; design can view the link and take screenshots now.
- **Real data** — Ruben is loading it; re-pull mockups once it lands.
- **UI ↔ LP alignment** — decide whether the SaaS UI moves toward the LP or vice versa (Kasper to coordinate).
- **FAQ + case copy** — design drafts, client approves.
- **Brand reference** — confirm the spelling of the style reference ("EcomClaw" vs "Ecom Cloud").
- **Pricing** — `$49 / $39 / $29` and trial/cancellation terms still marked "awaiting confirmation" in s10; unrelated to this round but still open.

### Conflicts worth raising with the client before building
1. **s3 loses its punchline.** The "2.2 ROAS looks fine but you lost $522" reveal is the page's sharpest moment, and it's built on the profit maths being removed. The replacement argument — *account-level numbers hide which feed items are dragging ROAS* — is weaker on its own and needs a strong visual to carry it. Worth confirming the new angle before rebuilding.
2. **"Find the products costing you money" survives, but it's profit language.** The client explicitly praised this line while also banning the profit frame. Keeping it is fine, but it's the one deliberate exception — flag it so it isn't "corrected" later.
3. **Yellow in s3, red in s9, for the same 2.2 number.** Intentional per the Loom (warning vs. failure), but it will look inconsistent unless the two sections are far apart in the scroll. They are (s3 vs s9), so this should hold — just be deliberate about it.
