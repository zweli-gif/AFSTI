# BUILD PROMPT: AFSTI Corridor Dashboard — HOME Tab Landing Page

## ROLE
You are a senior front-end developer building a single-file HTML dashboard. You will produce ONE complete HTML file with all CSS and JS inline. No external libraries except Google Fonts. All charts are CSS/JS only — no Chart.js, no D3, no Recharts.

---

## WHAT YOU ARE BUILDING

A scrolling landing page that makes the case for why Africa should invest in food trade corridors. This is the HOME tab of a 5-tab dashboard. The audience is board members, DFI directors, and development leaders. It must land in 60 seconds, then invite deeper exploration.

The page has 8 sections that scroll vertically. A sticky navigation bar sits at the top with 5 tabs (HOME is active, the other 4 are placeholder links).

---

## DESIGN SYSTEM (MATCH EXACTLY)

### Colors
```css
--bg: #f5f0e8;          /* warm off-white background */
--text: #1a1a1a;         /* near-black body text */
--sub: #6b6b6b;          /* secondary/muted text */
--grn: #006B54;          /* AGRA green — primary accent */
--grn-light: #e6f0ed;    /* light green tint for backgrounds */
--gold: #F7B500;         /* AGRA gold — secondary accent */
--gold-light: #fef8e6;   /* light gold tint */
--red: #C0392B;          /* red for negative/fail indicators */
--red-light: #fce8e6;    /* light red tint */
--amber: #E67E22;        /* amber for warning/medium */
--amber-light: #fdf2e6;  /* light amber tint */
--card-bg: #ffffff;      /* white card background */
--card-border: #e0dcd4;  /* subtle warm border */
--card-shadow: 0 2px 12px rgba(0,0,0,0.06);
```

### Typography
```css
/* Import these Google Fonts */
@import url('https://fonts.googleapis.com/css2?family=Bitter:wght@400;600;700&family=Source+Sans+3:wght@300;400;500;600;700&display=swap');

--font-heading: 'Bitter', serif;
--font-body: 'Source Sans 3', sans-serif;
```

- Page title/hero: Bitter 700, 42-48px
- Section titles: Bitter 700, 28-32px
- Card headers: Bitter 600, 18-20px
- Body text: Source Sans 3 400, 15-16px
- Data labels: Source Sans 3 600, 13px uppercase tracking 0.5px
- KPI numbers: Source Sans 3 700, 36-48px, color var(--grn)

### Layout
- Max content width: 1140px, centered
- Section vertical padding: 80px top, 80px bottom
- Card grid: CSS Grid, gap 24px
- Cards: white background, border-radius 12px, subtle shadow, 32px padding
- Sections alternate between var(--bg) and white backgrounds
- Mobile: cards stack to single column below 768px

### Sticky Navigation
- Fixed top bar, height 56px, background white, subtle bottom shadow
- 5 tabs: HOME | DAKAR-LAGOS | LOBITO | LIMPOPO | UPPER RIFT
- HOME tab is active (green underline + bold). Other tabs are grey, clickable but link to "#" (placeholders)
- On scroll, the nav adds a slightly stronger shadow
- Left side: "AFSTI" in Bitter 700, var(--grn)
- Right side: tab links in Source Sans 3 600, 14px, uppercase, tracking 1px

### Animations
- Sections fade in + slide up 20px on scroll (Intersection Observer, threshold 0.15)
- KPI numbers count up from 0 on scroll into view (duration 1.5s, easing ease-out)
- Bar charts animate width from 0 on scroll into view (duration 1s, staggered 100ms per bar)
- Keep animations subtle and professional. No bouncing, no spinning, no particle effects.

---

## SECTION-BY-SECTION CONTENT

### SECTION 1: HERO BANNER
**Background:** var(--grn) with subtle diagonal gradient to slightly lighter green
**Text color:** white
**Layout:** Centered, generous vertical padding (120px top, 100px bottom)

**Content:**
- Eyebrow text (Source Sans 3 500, 14px, uppercase, tracking 2px, gold color): "AFRICA FOOD SYSTEMS TRANSFORMATION INITIATIVE"
- Main headline (Bitter 700, 46px, white, max-width 800px, line-height 1.2):
  "Africa spends $100 billion importing food it can grow. Four corridors can change that."
- Subheadline (Source Sans 3 400, 20px, white with 85% opacity, max-width 700px, line-height 1.6):
  "$250–400M in coordinated investment across 4 corridors to unlock billions in intra-African trade and reach 150,000+ smallholder farmers"
- Scroll indicator: subtle animated down-arrow, white, pulsing opacity

### SECTION 2: FIVE FORCES CONVERGING
**Background:** var(--bg)
**Section title:** "Five forces are converging. This is the window."

**Layout:** 5 cards in a responsive grid (3+2 on desktop, 1 column on mobile)

Each card has:
- A large number in top-left (Bitter 700, 48px, var(--gold), opacity 0.3)
- A title (Bitter 600, 18px)
- A key stat (Source Sans 3 700, 24px, var(--grn))
- A 2-sentence explanation (Source Sans 3 400, 15px, var(--sub))

**Card data:**

Card 1:
- Number: 01
- Title: "The Sovereignty Crisis"
- Stat: "$62.8B"
- Text: "Sub-Saharan Africa's annual food import bill — accelerating past $100B continent-wide. The Ukraine shock revealed that African food security is hostage to shipping lanes, currencies, and conflicts it cannot control."

Card 2:
- Number: 02
- Title: "The Political Architecture"
- Stat: "55 nations"
- Text: "All AU member states signed the Kampala Declaration in January 2025 — committing to triple intra-African agri-food trade by 2035. 49 countries have ratified the AfCFTA. For the first time, there is both a food mandate and a trade mechanism."

Card 3:
- Number: 03
- Title: "The Infrastructure"
- Stat: "$10B+"
- Text: "Committed to the Lobito Corridor alone. Beitbridge modernised. TAZARA being rehabilitated. The Abidjan-Lagos highway carries $3B in annual trade. The corridors that were 'future tense' are becoming present tense."

Card 4:
- Number: 04
- Title: "Standalone Has Failed"
- Stat: "17%"
- Text: "Zambia's soya crushing capacity utilisation. Twenty years of crop-by-crop investment cases produced islands of production without trade linkages. The constraint is not agronomic — it's systemic."

Card 5:
- Number: 05
- Title: "Capital Demands Integration"
- Stat: "5 → 1"
- Text: "DFIs won't fund another standalone feasibility study. They want integrated cases where one investment de-risks another — where a feed mill makes aquaculture viable and a cold chain serves fish, tomato, and onions simultaneously."

### SECTION 3: WHY INTEGRATED, NOT STANDALONE
**Background:** white
**Section title:** "Why integrated, not standalone"
**Subtitle (Source Sans 3 400, 16px, var(--sub)):** "Each corridor is a system. One investment unlocks the next."

**Layout:** 4 corridor cards, 2×2 grid on desktop, stacked on mobile

Each corridor card has:
- A colored left border (4px, var(--grn))
- Corridor name badge (Source Sans 3 700, 12px, uppercase, tracking 1px, white text on var(--grn) background, border-radius 4px, inline-block padding 4px 12px)
- Tagline (Bitter 600, 18px)
- Thesis (Source Sans 3 400, 15px, max 2 sentences)
- A mini stat row at the bottom: "X investment components | X shared enablers"

**Card data:**

Card A:
- Badge: "LOBITO CORRIDOR"
- Tagline: "Protein-Oilseed Corridor"
- Thesis: "1 tonne of Zambian soybeans generates 3 trade flows — oil to DRC/Angola, meal to Malawi poultry, meal to tilapia. Shared transshipment and storage infrastructure serves all three."
- Stats: "3 value chains · 6 enablers"

Card B:
- Badge: "LIMPOPO CORRIDOR"
- Tagline: "Power-Fed Export Engine"
- Thesis: "Energy is the binding constraint. Solar IPPs unlock Zimbabwe irrigated wheat for SA/Zambia millers, and Malawi poultry processing for Mozambique/DRC markets."
- Stats: "2 value chains · 4 enablers"

Card C:
- Badge: "DAKAR-LAGOS CORRIDOR"
- Tagline: "Protein & Fresh Food Belt"
- Thesis: "ColdChainCo is the spine — the same cold chain infrastructure that moves fish also serves tomato, onions, and mango. Four commodities, one corridor, $3.5B+ addressable market."
- Stats: "3–4 value chains · 3 enablers"

Card D:
- Badge: "UPPER RIFT CORRIDOR"
- Tagline: "Tanzania Breadbasket"
- Thesis: "Two crops, same corridor, same logistics. Sunflower oil displaces Ukrainian imports to Ethiopia; rice displaces Asian imports to Kenya."
- Stats: "2 value chains · 3 enablers"

### SECTION 4: INVESTMENT vs UNLOCKED TRADE
**Background:** var(--bg)
**Section title:** "What goes in vs. what it unlocks"
**Subtitle:** "Coordinated corridor investment generates 8–12× in annual trade value"

**Layout:** Horizontal bar chart, CSS-only, animated on scroll

For each corridor, show TWO horizontal bars:
- Top bar (var(--grn)): Investment ($M) — labelled on the right
- Bottom bar (var(--gold)): Unlocked Annual Trade ($M) — labelled on the right
- Multiplier label to the far right (e.g., "~7×")
- Corridor name to the left

**Data:**
| Corridor | Investment ($M) | Trade ($M) | Multiplier |
|----------|----------------|------------|------------|
| Dakar-Lagos | 74–150 | 1,000–3,000 | ~10–20× |
| Lobito | 60–120 | 500–800 | ~6–7× |
| Upper Rift | 50–100 | 400–700 | ~7× |
| Limpopo | 40–80 | 300–500 | ~6× |
| **TOTAL** | **~250–400** | **~2,200–5,000** | **~8–12×** |

**Chart specifications:**
- Bar max-width scales to the largest value (3,000 for trade). Use percentage widths.
- Investment bars: max height 24px, border-radius 4px
- Trade bars: max height 24px, border-radius 4px
- Gap between investment and trade bar for same corridor: 4px
- Gap between corridors: 28px
- Animate bar widths from 0% to final % on scroll
- Below the chart, show a TOTAL row with a slightly bolder style
- Add a small footnote: "Indicative ranges. Investment figures from screening analysis; trade values from import substitution potential across corridor countries."

### SECTION 5: CROSS-CUTTING TOPICS MATRIX
**Background:** white
**Section title:** "Where corridors stand today"
**Subtitle:** "Green = ready. Amber = friction. Red = binding constraint."

**Layout:** CSS grid table/heatmap, 8 rows × 4 columns + header row + label column

**Data:**

| Topic | Lobito | Limpopo | Dakar-Lagos | Upper Rift |
|-------|--------|---------|-------------|------------|
| Production potential | GREEN | AMBER | GREEN | GREEN |
| Processing capacity | RED | AMBER | AMBER | AMBER |
| Corridor infrastructure | GREEN | AMBER | AMBER | RED |
| Cold chain | RED | RED | AMBER | RED |
| Border / trade facilitation | AMBER | AMBER | RED | AMBER |
| Energy | GREEN | RED | AMBER | GREEN |
| Trade finance | RED | AMBER | RED | RED |
| Policy & political economy | AMBER | RED | AMBER | AMBER |

**Styling:**
- Each cell is a rounded rectangle (border-radius 6px, height 44px, centered text)
- GREEN cells: background var(--grn-light), text var(--grn), dot or small text "Ready"
- AMBER cells: background var(--amber-light), text var(--amber), text "Friction"
- RED cells: background var(--red-light), text var(--red), text "Binding"
- On hover, show a tooltip with a one-line explanation (use title attribute or CSS tooltip)
- Topic labels on the left in Source Sans 3 600, 14px
- Corridor names on top in Source Sans 3 700, 13px, uppercase

**Tooltip data (one per cell — include as title attributes):**

| | Lobito | Limpopo | Dakar-Lagos | Upper Rift |
|---|---|---|---|---|
| Production | Zambia soya surplus established | ZW wheat needs irrigation + energy | CIV fish programme, Ghana tomato potential | TZ sunflower/rice — large smallholder base |
| Processing | Crushers at 17% utilisation | Milling exists, poultry emerging | Tomato processing nascent, fish processing needed | Crushing capacity underutilised |
| Infrastructure | $10B+ Lobito rail investment | Beitbridge modernised 2024 | Abidjan-Lagos highway, Sèmè-Kraké | TAZARA rehab timeline uncertain |
| Cold chain | No corridor cold chain exists | No corridor cold chain exists | ColdChainCo proposed — anchor investment | No corridor cold chain exists |
| Border | Kasumbalesa 3-7 day delays | Beitbridge improved to 3-6hrs | Nigeria border unpredictable | EAC OSBPs operational |
| Energy | Grid access adequate | ZW power crisis — binding | Mixed reliability | Grid access adequate |
| Trade finance | Aggregation finance gap | FX repatriation rules in ZW | Aggregation + export finance gap | Aggregation finance gap |
| Policy | PEA: Amber | PEA: Amber-Red (ZW) | PEA: Amber-Green (CIV) to Amber (NG) | PEA: Amber to Amber-Red (ET) |

### SECTION 6: THE PRICE ADVANTAGE
**Background:** var(--bg)
**Section title:** "How corridors beat imports — before you touch a seed"
**Subtitle:** "Five structural advantages that can be unlocked with a wave of a pen"

**Layout:** This is the conceptual framework section. Show ONE illustrative example as an animated waterfall chart, with the 5 layers explained alongside.

**Left side (60% width):** Waterfall chart
**Right side (40% width):** Numbered list of 5 layers

**Waterfall chart — use the soya oil example (Zambia → DRC vs Argentina import):**

The chart is a vertical waterfall showing how the import price gets eaten away by corridor advantages:

| Step | Label | Value | Running Total |
|------|-------|-------|---------------|
| Start | Import CIF landed price | $1,300 | $1,300 |
| −1 | Working capital saving | −$35 | $1,265 |
| −2 | Transport saving | −$120 | $1,145 |
| −3 | Tariff preference (COMESA) | −$65 | $1,080 |
| −4 | Agility premium | −$30 | $1,050 |
| −5 | Border friction saving | −$20 | $1,030 |
| End | Price corridor must beat | $1,030 | $1,030 |

**Chart styling:**
- Vertical bars, starting bar (green, full height representing $1,300)
- Each reduction shown as a red/orange floating bar segment showing the decrease
- Final bar (gold) showing the target price
- Animated on scroll — bars appear sequentially with 200ms delay
- Labels on the left, dollar values on the right of each bar
- The gap between start ($1,300) and end ($1,030) should be visually prominent, annotated: "$270/t structural advantage (21%)"

**Right side — 5 layers explanation:**

1. **Working Capital** — "45-60 day ocean cycle vs 5-14 day corridor. At 22% interest, that's $35/t free money."
2. **Transport** — "800km by truck beats 12,000km by ocean — despite Africa's higher per-km costs."
3. **Tariff Preference** — "COMESA/ECOWAS/EAC preferences vs MFN rates. Sometimes worth $65-385/t."
4. **Agility Premium** — "Respond to demand spikes in days, not months. Traders pay $20-50/t for certainty."
5. **Border Friction** — "Every hour saved at Kasumbalesa is money. OSBP investments are already reducing this."

Below the chart, add a callout box (var(--gold-light) background, gold left border):
"The question is not whether African farmers can produce as cheaply as Indonesia or Brazil. The question is: given $50–400/t of structural advantages, how much of the gap remains? That's what each investment case must close."

### SECTION 7: SMALLHOLDER IMPACT
**Background:** white
**Section title:** "Who this reaches"

**Layout:** 4 large KPI counters in a row, then a simple stacked horizontal bar below

**KPI counters (animate counting up from 0 on scroll):**

| KPI | Value | Label |
|-----|-------|-------|
| 1 | 195,000+ | Smallholder farmers reached |
| 2 | 4 | Trade corridors activated |
| 3 | 9 | Integrated investment cases |
| 4 | $2.2–5.0B | Annual trade unlocked |

**KPI styling:**
- Number: Source Sans 3 700, 48px, var(--grn)
- Label: Source Sans 3 500, 14px, var(--sub), uppercase
- Cards arranged in 4-column grid, centered

**Below the KPIs, show SHF breakdown by corridor as a stacked horizontal bar:**
- Single bar, full width, divided into 4 colored segments
- Lobito: 50K+ (color: var(--grn))
- Limpopo: 10K+ (color: var(--amber))
- Dakar-Lagos: 35K+ (color: var(--gold))
- Upper Rift: 100K+ (color: a medium teal, e.g., #2E8B8B)
- Labels inside each segment (white text) or below if segment too small

### SECTION 8: WHAT WE STILL DON'T KNOW
**Background:** var(--bg)
**Section title:** "What we still don't know"
**Subtitle:** "Honest about our assumptions. These need field validation."

**Layout:** 6 items, each as a compact card with corridor tag

Each item has:
- A corridor pill/badge (small, colored background matching the corridor)
- The assumption text (Source Sans 3 400, 15px)
- How we'll validate (Source Sans 3 400, 14px, var(--sub), italic)

**Data:**

Item 1:
- Corridor: LOBITO
- Assumption: "Zambia crusher utilisation at 17% — is this accurate, and what's the real bottleneck?"
- Validation: "Field visits to Zamanita, Mount Meru; crusher operator interviews"

Item 2:
- Corridor: DAKAR-LAGOS
- Assumption: "ColdChainCo multi-commodity co-location — will fish, tomato, and onions actually share infrastructure?"
- Validation: "Site visits to Abidjan port zone; cold chain operator interviews"

Item 3:
- Corridor: LIMPOPO
- Assumption: "Zimbabwe solar IPP regulatory framework — is it real and investable?"
- Validation: "ZERA policy review; energy sector interviews"

Item 4:
- Corridor: UPPER RIFT
- Assumption: "TAZARA rehabilitation timeline — when does rail capacity actually deliver?"
- Validation: "Tanzania government engagement; AfDB project documentation"

Item 5:
- Corridor: DAKAR-LAGOS
- Assumption: "Nigeria border reliability — will Sèmè-Kraké stay open for corridor trade?"
- Validation: "Political economy deep dive; cross-border trader interviews"

Item 6:
- Corridor: UPPER RIFT
- Assumption: "Ethiopia FX rationing — will they actually allow Tanzanian edible oil imports?"
- Validation: "National Bank of Ethiopia engagement; importer interviews"

### FOOTER
**Background:** var(--grn), dark
**Text:** white
**Content:**
- "AFSTI — Africa Food Systems Transformation Initiative"
- "Baobab Impact & Dalberg for AGRA | February 2026"
- "CONFIDENTIAL — Board-ready draft"

---

## TECHNICAL REQUIREMENTS

1. **Single file.** All HTML, CSS, and JS in one .html file.
2. **No external JS libraries.** Charts are pure CSS + vanilla JS.
3. **Google Fonts only external dependency** (Bitter + Source Sans 3).
4. **Responsive:** Must work on desktop (1440px), tablet (768px), and mobile (375px). Use CSS Grid + Flexbox. Cards stack on mobile.
5. **Smooth scroll** between sections when clicking nav (optional but nice).
6. **Intersection Observer** for scroll animations. Elements start with opacity 0 + translateY(20px), animate to opacity 1 + translateY(0) on intersection.
7. **Number counter animation** for KPIs: count from 0 to target over 1.5s using requestAnimationFrame. Only trigger once per element.
8. **Bar chart animation:** widths animate from 0% to target% over 1s with stagger.
9. **Waterfall chart:** bars appear sequentially, 200ms stagger.
10. **Print-friendly:** @media print should remove animations and show all content.
11. **Performance:** Lazy-load animations only when section is in viewport. No layout shifts.

---

## IMPORTANT NOTES

- The aquaculture/fish case is mentioned as an EXAMPLE of the integrated approach (in the "Capital Demands Integration" card in Section 2, and as context for ColdChainCo). It is NOT presented as an approved investment case. Use phrasing like "as demonstrated by the CIV aquaculture analysis" or "the integrated approach, exemplified by...".
- Never mention "Sofala Partners" anywhere. If referencing political economy analysis, say "PEA" or "Political Economy Assessment".
- The $100M import threshold referenced is per CORRIDOR, not per country.
- Keep language confident and punchy. This is a boardroom document, not an academic paper.
- All numbers should have sources noted in small footnote text where space allows.

---

## VALIDATION CHECKLIST (before delivering)

- [ ] All 8 sections render correctly
- [ ] Sticky nav works and HOME tab is visually active
- [ ] Colors match the design system exactly (check hex values)
- [ ] Bitter font loads for headings, Source Sans 3 for body
- [ ] Scroll animations trigger once and don't re-trigger
- [ ] KPI numbers count up smoothly
- [ ] Bar chart in Section 4 animates
- [ ] Waterfall chart in Section 6 animates sequentially
- [ ] Heatmap in Section 5 has tooltip/hover text
- [ ] Mobile layout works (cards stack, text readable, no horizontal scroll)
- [ ] No console errors
- [ ] File is self-contained (only external dep = Google Fonts)
- [ ] Footer renders with correct attribution
