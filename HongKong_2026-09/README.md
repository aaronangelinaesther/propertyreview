# Hong Kong Property Search — HK$5M–16M, ≥900 sq ft (Sept 2026)

A standalone dataset of Hong Kong resale apartment listings pulled from [28Hse](https://www.28hse.com), a Hong Kong property portal that (unlike Squarefoot or Midland) is directly scriptable without hitting a bot-detection wall.

This is a **separate analysis** from the UK Savills auction reviews and the Melbourne comparison in this repo — different market, different data source, different methodology. It is not merged into either.

## Origin and scope

This started as a quick gauge of how accessible Hong Kong listing data is (compared to portals that block automated access). Once 28Hse proved workable, the filter was set to the criteria below and the full result set was pulled.

**Filter applied on 28hse.com:**
- Transaction type: Sale (Buy), apartments
- Price: HK$5,000,000 – HK$16,000,000
- Saleable area: ≥ 900 sq ft

The portal reported **1,812 matching listings** at the time of the pull (result counts on 28Hse shift in real time as listings are added/removed/re-priced, so this is a snapshot, not a fixed universe).

## What's in this dataset

| File | Contents |
|---|---|
| **`hk-listings-explorer.html`** | **Self-contained, offline-capable filter page** — filter by district, area, estate name, price range and size range, sort by any column, click through to the live listing. Just double-click to open in a browser; no server or internet connection needed. |
| `hk_listings_structured.csv` | 1,418 unique listings, one row each, structured fields including building age (see below) |
| `hk_listings_structured.json` | Same data as JSON |
| `hk_listings_deduped.json` | Raw `{link, text}` pairs as scraped, deduplicated by listing URL — kept as an audit trail back to the source text |
| `hk_island_enriched.csv` / `.json` | The 74 listings in Hong Kong Island districts (Central and Western, Wan Chai, Eastern, Southern) only, with building age and estimated rent/yield added — see below |

### Using the filter page

Open `hk-listings-explorer.html` directly (double-click, or drag into a browser tab). All 1,418 listings are embedded in the file itself, so it works fully offline.

- **District** — the 18 official Hong Kong districts (Yuen Long, Sha Tin, Kowloon City, etc.)
- **Area** — a dropdown of ~50 finer-grained neighborhoods, derived by matching each listing's district+estate text against a known area-name list; the Area list narrows automatically to whichever District is selected (see caveat below on why this split is a best-effort heuristic, not official data)
- **Estate / building name** — free-text search against the full location string
- **Price** and **Saleable area** — min/max range filters
- **Bedrooms** — exact match where the portal listed it
- **Sort** — by price, HK$/sqft, or size in either direction; column headers are also clickable to sort/toggle
- Every row links straight to the live 28Hse listing
- Every row shows a **Building age** column (hover for the exact occupation date, confidence level, and source) — see below for coverage and methodology
- For the four **Hong Kong Island** districts only, an additional **Est. rent / yield** column appears (hover for the source note). All other districts show "–" for this one — see below for why.

### Building age (all districts)

**Building age is populated for 1,296 of 1,418 listings (91.4%), across 310 of the dataset's 354 unique estates (87.6%)** — real, sourced data, not an estimate. Each unique estate's own 28Hse listing page states an "Occupation Date" / "Building age" field directly (28Hse pulls this from Hong Kong Buildings Department–derived data), so every one of the 354 estates was looked up individually via its own listing page — not just Hong Kong Island (that was the first pass; a second pass extended the same technique to the remaining ~315 estates across all other districts).

- Hover the "Building age" cell in the explorer page for the exact occupation date, confidence level, and source.
- Two of the largest Hong Kong Island estates (North Point City Garden, 17 listings; Quarry Bay Kornhill, 2 listings) were cross-checked against Wikipedia and match. One estate (Baguio Villa) is Wikipedia-sourced directly. Every other estate's age comes from its own 28Hse listing page.
- **The ~44 estates (mostly standalone village houses / "Tsuen" / "Village" listings) without an age**: these don't have a formal multi-unit estate record on 28Hse, so there's no "Occupation Date" field on their listing page at all — left blank rather than guessed.
- **One data-quality catch**: Ho Man Tin Belfran Mansion's listing page showed an implausible "590 Year" building age (clearly a source-site data error) — excluded rather than trusted.
- **One internally inconsistent source**: Causeway Bay Lai Chi Building's own listing page has two disagreeing dates (occupation date vs. "estate entry date," ~2 years apart) — flagged Low confidence rather than arbitrarily picking one.
- This required roughly 354 individual page fetches (one representative listing per unique estate, since age is a building-level fact, not a per-listing one) — done directly against each estate's own 28Hse detail page rather than web search, since building age isn't reliably available any other way at this scale.

### Hong Kong Island rental estimate

For the 74 listings across the four Hong Kong Island districts (Central and Western, Wan Chai, Eastern, Southern), an **Est. rent / yield** column was also added — but this one is genuinely an estimate, not sourced data: 28Hse's rental search is JavaScript-driven with no shareable URL (the same limitation documented below for the sale-side pagination), so live comparable rents weren't pulled. Instead this is a **district-level rate estimate**: HK$/sqft/month figures from general knowledge of the Hong Kong secondary rental market (Central & Western ~HK$29/sqft, Wan Chai ~HK$32/sqft, Eastern ~HK$30/sqft, Southern ~HK$27/sqft), applied to each listing's own saleable area, with gross yield computed against its asking price. This is the same methodology the Melbourne comparison in this repo uses for its rent estimates — **a market-rate approximation, not a rent appraisal or a live comparable**. Resulting yields average ~3.0% gross (range ~2.2%–4.9%), consistent with typical published Hong Kong Island secondary-market yield bands, which is a reasonable sanity check but not independent verification.

This rental estimate was only done for Hong Kong Island (unlike building age, which now covers all districts) because it relies on district-level rate assumptions researched specifically for those four districts; extending it to the other 14 districts would need the same rate research repeated for each.

**Coverage: 1,418 of ~1,812 listings (~78%).** The gap is explained below under Methodology & limits — it's a result of the extraction technique, not a deliberate exclusion.

### Fields captured per listing

| Field | Source | Notes |
|---|---|---|
| `link` | Listing detail-page URL | Use this to open the live listing |
| `location` | Search-card text | District + estate name, e.g. "Tung Chung Caribbean Coast" (not split further — see caveats) |
| `floorTower` | Search-card text | Floor band (High/Mid/Low), tower/block/unit where shown |
| `netSqft` | "Saleable Area" on the card | This is the **net/saleable area** the portal quotes — see caveats on "net vs gross" below |
| `pricePerSqft` | Search card ("@X" next to saleable area) | HKD per saleable sq ft, as quoted by the portal |
| `priceHKDMillions` | Search card | Asking price, HK$ millions |
| `bedrooms` / `bathrooms` | Search card tags | Not always present on the card |
| `agent` | Search card | Listing agency, or "Owner (landlord)" for no-agent direct listings |
| `tags` | Search card | Orientation, developer, amenities (sea view, clubhouse, MTR nearby, etc.) — free text, unparsed |
| `buildingAge` / `ageOccupationDate` / `ageConfidence` / `ageSource` | Each estate's own 28Hse listing page | Building age in years; blank for the ~44 estates with no age field on their page (see "Building age" section below) |

### Fields requested but not included at this scale: gross sq ft, rental estimate

Two fields are **not present on 28Hse's search-result cards or on individual listing pages at bulk scale** — building age turned out to be fetchable per-estate (see below), but gross floor area and rental estimate are not: gross area sometimes appears on a listing's own detail page but inconsistently, and rental comparables require 28Hse's separate, JavaScript-driven rental search (no shareable URL, so not bulk-scriptable the way the sale-side pagination was).

Rather than fabricate or estimate these across all 1,418 listings, they're left out of the bulk dataset. Hong Kong Island gets a rental estimate anyway, but as a clearly-flagged district-level approximation, not a scraped figure — see below.

If useful, the practical next step for gross floor area is the same targeted approach used for rental yield: pick a shortlist and fetch/estimate for just that subset.

## Methodology & limits (read before trusting the "78%" figure)

- **Extraction technique**: 28Hse's price/area filters and pagination are JavaScript-driven (POST-based, no shareable URL), so this was scripted via direct DOM interaction — clicking the pagination control and scraping each page's listing cards, accumulating them in the browser tab's memory, then exporting via a triggered file download once accumulation finished.
- **Why not 100%**: the browser tab progressively slowed down over ~120 pages of repeated pagination (increasing memory/DOM/ad-script overhead with no cleanup between page loads), causing the automation to periodically time out. The page's own JavaScript kept running in the background after timeouts, which is how coverage kept climbing (1,020 → 1,418 unique) — but the last stretch of pages became too slow to reliably reach in this session.
- **1,860 raw rows → 1,418 unique**: pagination restarted from page 1 more than once after timeouts, so ~24% of raw scraped rows were re-scraped duplicates of earlier pages, removed by de-duplicating on listing URL.
- **"Net sq ft" caveat**: Hong Kong listings almost always quote *saleable* (net) area on portal search cards; this is what `netSqft` captures. Gross floor area (which includes a share of common areas) is typically 15–20% larger and is what's missing per the section above.
- **`location` isn't split into District / Estate in the CSV/JSON**: 28Hse concatenates them ("Yuen Long Palm Springs", "Tuen Mun Castle Peak Road Le Pont") without a consistent delimiter, and Hong Kong's informal neighborhood names don't map cleanly onto the 18 official districts. The HTML explorer's "Area" filter does attempt a split — matching each `location` string against a ~50-entry list of known Hong Kong area names — but that's a heuristic built for this page, not a verified field, and a handful of small/unusual locations (e.g. standalone building names with no area prefix) fall back to just their first word.
- **Occasional portal data glitches carried through as-is**: e.g. a small number of cards show a truncated price-per-sqft ("@1" instead of the full number) — this is how the source site displayed it, not a parsing error on this end.

## Quick stats (1,418 listings)

- Price: HK$5.0M – HK$16.0M, average HK$12.2M
- Saleable area: 900 – 4,500 sq ft, average 1,140 sq ft
- Price per sq ft: roughly HK$8,800 – HK$14,000 for the bulk of listings (a handful of outliers above HK$17,000/sqft and a handful of large village houses below HK$3,500/sqft pull the extremes)
- 354 distinct estates/buildings represented
- Most-listed estates: Yuen Long Palm Springs (44), Shatin Dragons Range (29), Yuen Long Fairview Park (27), Tung Chung Caribbean Coast (27), Tung Chung The Visionary (26)
- Most-active agencies: Centaline (274 listings combined across its branch names), Midland Realty (290 combined), Ricacorp Properties (133)
- Building age: known for 1,296 listings (91.4%), ranging 3–70 years old, average 29 years — see "Building age" section above for methodology and the ~9% gap

## Suggested uses

- Filter the CSV by district/estate name to shortlist candidates for a given budget and minimum size.
- Sort by `pricePerSqft` to find relative value within a price band.
- Cross-reference `agent` if you want to consolidate viewings through one agency.
- Use `link` to open the live listing before acting on anything — prices and availability move daily.
