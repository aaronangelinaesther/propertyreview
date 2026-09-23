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
| `hk_listings_structured.csv` | 1,418 unique listings, one row each, structured fields (see below) |
| `hk_listings_structured.json` | Same data as JSON |
| `hk_listings_deduped.json` | Raw `{link, text}` pairs as scraped, deduplicated by listing URL — kept as an audit trail back to the source text |

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

### Fields requested but not included at this scale: gross sq ft, rental estimate, building age

These three fields are **not present on 28Hse's search-result cards** — only saleable (net) area, price, and tags are. Getting gross floor area, a rental estimate, or building age requires opening each **listing's own detail page** (gross area is sometimes shown there) or looking up the **building/estate** in a separate valuation tool (rental estimates, building age).

At the scale of 1,418 listings across **354 distinct estates**, that would mean 1,000+ additional page fetches for gross area alone, and a similar number of estate lookups for age/rental — well beyond what's practical to do reliably in one pass. Rather than fabricate or estimate these values, they're left out of the bulk dataset.

If useful, the practical next step is targeted enrichment: pick a shortlist (e.g., top N by price/sqft, or all listings in a specific district) and fetch gross area / building age / rental yield for just that subset.

## Methodology & limits (read before trusting the "78%" figure)

- **Extraction technique**: 28Hse's price/area filters and pagination are JavaScript-driven (POST-based, no shareable URL), so this was scripted via direct DOM interaction — clicking the pagination control and scraping each page's listing cards, accumulating them in the browser tab's memory, then exporting via a triggered file download once accumulation finished.
- **Why not 100%**: the browser tab progressively slowed down over ~120 pages of repeated pagination (increasing memory/DOM/ad-script overhead with no cleanup between page loads), causing the automation to periodically time out. The page's own JavaScript kept running in the background after timeouts, which is how coverage kept climbing (1,020 → 1,418 unique) — but the last stretch of pages became too slow to reliably reach in this session.
- **1,860 raw rows → 1,418 unique**: pagination restarted from page 1 more than once after timeouts, so ~24% of raw scraped rows were re-scraped duplicates of earlier pages, removed by de-duplicating on listing URL.
- **"Net sq ft" caveat**: Hong Kong listings almost always quote *saleable* (net) area on portal search cards; this is what `netSqft` captures. Gross floor area (which includes a share of common areas) is typically 15–20% larger and is what's missing per the section above.
- **`location` isn't split into District / Estate**: 28Hse concatenates them ("Yuen Long Palm Springs", "Tuen Mun Castle Peak Road Le Pont") without a consistent delimiter, and Hong Kong's informal neighborhood names don't map cleanly onto the 18 official districts. Splitting reliably would need a maintained estate-name lookup table, which wasn't built for this pass.
- **Occasional portal data glitches carried through as-is**: e.g. a small number of cards show a truncated price-per-sqft ("@1" instead of the full number) — this is how the source site displayed it, not a parsing error on this end.

## Quick stats (1,418 listings)

- Price: HK$5.0M – HK$16.0M, average HK$12.2M
- Saleable area: 900 – 4,500 sq ft, average 1,140 sq ft
- Price per sq ft: roughly HK$8,800 – HK$14,000 for the bulk of listings (a handful of outliers above HK$17,000/sqft and a handful of large village houses below HK$3,500/sqft pull the extremes)
- 354 distinct estates/buildings represented
- Most-listed estates: Yuen Long Palm Springs (44), Shatin Dragons Range (29), Yuen Long Fairview Park (27), Tung Chung Caribbean Coast (27), Tung Chung The Visionary (26)
- Most-active agencies: Centaline (274 listings combined across its branch names), Midland Realty (290 combined), Ricacorp Properties (133)

## Suggested uses

- Filter the CSV by district/estate name to shortlist candidates for a given budget and minimum size.
- Sort by `pricePerSqft` to find relative value within a price band.
- Cross-reference `agent` if you want to consolidate viewings through one agency.
- Use `link` to open the live listing before acting on anything — prices and availability move daily.
