# Melbourne Older-Stock Comparison — September 2026

A desk-based screening comparison of **older-build units and Victorian terraces for sale across thirteen Melbourne suburbs** — interwar/Art Deco walk-ups, postwar "six-pack" blocks, and period terraces — pulled from realestate.com.au listings live 18–21 September 2026.

Unlike the UK auction reviews in this repo, this isn't an auction catalogue: these are ordinary private-treaty and auction listings on the open market, gathered by browsing realestate.com.au suburb by suburb rather than working through a single seller's catalogue.

## The comparison page

**[melbourne-period-stock.html](melbourne-period-stock.html)** — a self-contained, offline-capable HTML page (no external fonts, scripts, or map tiles) with:

- **58 listings across 13 suburbs**: St Kilda, Elwood, Balaclava, Caulfield, Hawthorn, Carlton, Fitzroy, Northcote, Essendon, Preston, Coburg, Ivanhoe, Albert Park
- A sortable/filterable table — filter by suburb, dwelling type (Unit/Terrace) and era, sort by price/rent/yield
- Per-listing: price, beds/baths, nearest transport, nearby school, shopping strip, an estimated weekly rent and gross yield, and an area-safety indicator, plus a link to the live listing
- A schematic (non-geocoded) suburb map, clickable to filter the table
- Full methodology and caveats in the page's own footer

Open the file directly in any browser — it needs no internet connection once saved. A live, shareable copy is also published at **https://claude.ai/artifact/6L5ajUhcoJQYbr4cgRbbBJ**.

## Scope and grouping

Suburbs were chosen to cover the three main eras of older Melbourne housing stock:

- **Interwar / Art Deco (1920s–30s)**: St Kilda, Elwood, Balaclava
- **Postwar "six-pack" walk-ups (1960s–70s)**: Caulfield, Hawthorn, Preston, Coburg, Ivanhoe, Essendon, Northcote
- **Victorian/Edwardian terraces (pre-1901–1910s)**: Carlton, Fitzroy, Albert Park

Within each suburb, "era" is a **proxy guess, not a confirmed fact** — inferred from unit-block size and unit-numbering patterns (a low single/double-digit unit number in a small block suggests an older low-rise; a three-digit unit number usually means a large modern mid/high-rise). Several suburbs' current listings turned out to skew toward newer stock despite the suburb's older-stock reputation (notably Northcote and most of Essendon) — those lots are honestly tagged **"Newer build (non-target)"** in the tool rather than mislabelled.

## Method notes / limitations

- **Estimated rent** is a rough weekly figure from general knowledge of each suburb's rental band for the dwelling type and bedroom count — not a rent appraisal.
- **Estimated yield** is simply (rent × 52) ÷ price — a starting point for comparison, not a return likely to be cleared once agent fees, vacancy, land tax, owners corporation fees and maintenance are accounted for.
- **Area safety** reflects general reputation and background knowledge, not official crime statistics. For verified, LGA-level figures, check the Crime Statistics Agency Victoria at [crimestatistics.vic.gov.au](https://www.crimestatistics.vic.gov.au).
- Session web-search quota was exhausted partway through this research; most data was gathered via direct browser navigation of realestate.com.au rather than search, and a handful of specific comparable-price claims (e.g. street-level sold prices referenced in chat but not carried into the page) were not independently re-verified.
- Desk-based screening only — **not** a valuation, rental appraisal or investment advice. Verify every figure independently before acting on anything here.
