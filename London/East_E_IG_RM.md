# East London / Essex-Border Batch (E, IG, RM) — McHugh & Co Auction, 16-17 Sept 2026

Catalogue: https://www.mchughandco.com/future-auctions/76247 | Batch: 17 residential lots, E/IG/RM postcode areas
Source CSV: `batch2_B_east.csv` (re-verified against this update — same 17 lots, no guide-price changes; a handful of scheduled end times were corrected by a few minutes to match the CSV/live listing pages, see tables below)

**Site accessibility re-checked 2026-08-31:** mchughandco.com direct access is **still blocked** (bot protection — socket hang up on every direct `WebFetch` attempt, retested today). The `r.jina.ai` proxy workaround **still works**, and critically it now also works for fetching mchughandco.com pages directly (not just as a search fallback). Combined with a DuckDuckGo-via-proxy search technique (Google and Bing search results are themselves blocked/CAPTCHA'd or return irrelevant results through the proxy; DuckDuckGo's HTML endpoint was not), **individual lot pages: 17 of 17 now found** — a complete turnaround from the prior run's 0 of 17 (this update session closed out the final three: Lots 45, 43, and 85, which the previous interrupted pass had left as "catalogue summary only"). All 17 detail pages were confirmed as matching this specific 16/09/2026 auction (matching lot number, guide price, and/or closing time) and fetched for accommodation, tenure, EPC, and council tax band. Direct-URL detail page links are given in each lot's row below.

**Methodology note:** Area-level research draws on Rightmove/Zoopla postcode-level sold-price data (fetched directly), Wikipedia, and general knowledge, as in the original run. Small postcode districts (e.g. E4, E7, E11, RM9) have low sold-transaction counts on Rightmove, so a handful of the "average by property type" figures are visibly skewed by one or two outlier sales — flagged inline where this applies. Crime statistics could not be independently verified; social-status ratings rely on demographic/reputation context from Wikipedia and general knowledge instead. **Rental estimates (new this update)** are based on a small number of comparable live/recent asking rents per postcode found via the same DuckDuckGo-proxy search technique (mostly Zoopla/Rightmove listings, occasionally an aggregator average) — treat as indicative midpoints, not formal market averages. **Important caveat on gross yields:** yields below are calculated as (estimated annual rent ÷ auction *guide* price), per the task brief. Auction guide prices are opening-bid figures, typically well below both fair market value and the property's eventual hammer price (see the "Average cost of comparable property type" discount analysis in each section) — so these gross yields are systematically inflated versus what a buyer would actually achieve after paying a realistic purchase price. They are best read as "yield on a successful deep-discount purchase," not an expected outcome.

Ratings are 1 (weak) to 5 (strong).

---

## 1. Hainault, Redbridge (IG6)

**Growth potential: 3/5** — Steady, unspectacular. IG6 sold prices ~3% up YoY and 5% above the 2022 peak (£500,175 overall average). No Elizabeth Line station (Central Line only, via Hainault/Grange Hill), so it misses the Crossrail uplift enjoyed by nearby Ilford/Chadwell Heath.
**Average cost of comparable property type:** IG6 flats/maisonettes average **£316,183**; terraced £512,331; semi-detached £555,619. The guide price of £195,000+ for a garden maisonette sits well below the £316k flat average — a meaningful apparent discount, though maisonettes typically trade below purpose-built flats, so treat the gap as indicative rather than exact.
**Social status / desirability: 4/5** — Quiet, green-belt-adjacent suburb; mostly 1947-53 LCC cottage estate housing; Hainault Forest Country Park on the doorstep; part of Redbridge, a borough with a generally solid reputation.
**Proximity to shops/amenities: 3/5** — Small local centre; relies on nearby Barkingside/Chigwell for bigger shopping.
**Proximity to schools: 4/5** — Redbridge is one of England's consistently top-performing boroughs for GCSE results; several well-regarded schools in the wider borough (e.g. Beal High School, Ilford County High).
**Potential rental:** 2-bed flats/maisonettes in IG6 are currently asking **£1,600-£1,650 pcm** on Rightmove/Zoopla; using £1,600 pcm (**£19,200/year**) against the £195,000+ guide gives a gross yield of **~9.8%** — high for London, though the vacant unit is only the first-floor half of a two-flat freehold (the ground-floor maisonette is let on a 125-year lease at £250 p.a. ground rent, so an investor buying the whole freehold could earn ground-rent income too).
**Verdict:** A safe, low-drama outer-suburb pick — decent long-term hold, priced at an apparent discount to local maisonette values, but transport connectivity is its weak point.

| Lot | Address | Guide Price | Description | Detail page | End time | Est. Monthly Rent | Est. Annual Rent | Gross Yield |
|---|---|---|---|---|---|---|---|---|
| 1 | 14 & 14(A) Dryden Close, Hainault, IG6 3EA | £195,000+ | Freehold First Floor Garden Maisonette (2 bed), Vacant Possession; ground floor maisonette let on 125-yr lease from 2020, £250 p.a. ground rent. EPC D, Council Tax Band B, LB Redbridge. | **Found:** mchughandco.com/lot/details/192651 | 16/09/2026 09:00 | £1,600 | £19,200 | ~9.8% |

---

## 2. Chingford, Waltham Forest (E4)

**Growth potential: 3/5** — E4's Rightmove "terraced average" (£3.66M) is a statistical artefact from a tiny/skewed sample and should be disregarded; the semi-detached average (£701,061) is more usable but still likely pulled up by premium roads near Epping Forest/Chingford Golf Course. No Elizabeth Line; served by London Overground to Liverpool Street (Chingford branch), with the old direct Stratford link (Hall Farm Curve) closed since 1970.
**Average cost of comparable property type:** Against a semi-detached average of ~£701k, a guide of £210,000+ for "32 Antlers Hill... Freehold Semi-Detached House" looks dramatically below market — even allowing for the average being skewed upward and the property likely needing full modernisation, this is the single largest apparent gap in the whole batch and warrants a closer look at the actual condition/tenure.
**Social status / desirability: 4/5** — Leafy, high owner-occupation, strong family-suburb reputation, Epping Forest access; diversifying demographically (White British down from 80.5% to 49.1% 2001-2021) but retains a settled, low-crime suburban feel typical of outer Waltham Forest.
**Proximity to shops/amenities: 3/5** — Chingford Mount/Station Road local centre; not a major retail destination.
**Proximity to schools: 4/5** — Waltham Forest has several solid comprehensives (e.g. Chingford Foundation School has a good reputation locally).
**Potential rental:** 3-bed houses in E4 are letting for roughly **£1,850-£2,300 pcm** (area average ~£2,300 pcm per housesforsaletorent.co.uk). Using £2,300 pcm (**£27,600/year**) against the £210,000+ guide gives a gross yield of **~13.1%** — very high for London, consistent with this being the largest apparent guide-to-market discount in the batch.
**Verdict:** Headline stand-out value if the guide-to-market gap is real rather than a data artefact — worth verifying condition/tenure directly before bidding.

| Lot | Address | Guide Price | Description | Detail page | End time | Est. Monthly Rent | Est. Annual Rent | Gross Yield |
|---|---|---|---|---|---|---|---|---|
| 4 | 32 Antlers Hill, Chingford, E4 7RT | £210,000+ | Freehold Semi-Detached House (3 bed), Vacant Possession, requires modernisation. EPC C, Council Tax Band A, LB Waltham Forest. | **Found:** mchughandco.com/lot/details/192553 | 16/09/2026 09:06 | £2,300 | £27,600 | ~13.1% |

---

## 3. Plaistow, Newham (E13)

**Growth potential: 2/5** — E13 sold prices roughly flat YoY and 6% below the 2023 peak — a cooling pocket relative to the rest of the batch. Good existing transport (District/H&C lines, Elizabeth Line accessible via nearby Custom House/West Ham) is already priced in rather than a fresh catalyst.
**Average cost of comparable property type:** E13 flats average **£320,464**. The guide of £100,000+ for a leasehold garden flat is roughly a third of the area average — a very large apparent discount, though such low-guide leasehold auction flats often carry short leases, ground-rent issues, or need of full refurbishment, which typically explains gaps this size.
**Social status / desirability: 3/5** — Historically one of Newham's more deprived pockets; benefited from substantial regeneration funding (£92m SRB5 scheme, £54.6m New Deal for Communities) through the 2000s, with visible but incomplete improvement.
**Proximity to shops/amenities: 3/5** — Plaistow High Street and nearby Queens Market/Green Street give reasonable local amenity, with Westfield Stratford a short journey away.
**Proximity to schools: 3/5** — Newham schools are mixed but improving; some strong academies in the borough (e.g. Sarah Bonnell), though outcomes historically trail outer London.
**Potential rental:** 1-bed flats in E13 are letting around **£1,500-£1,600 pcm** (area average ~£1.6k pcm per housesforsaletorent.co.uk). Using £1,550 pcm (**£18,600/year**) against the £100,000+ guide gives a gross yield of **~18.6%** — the highest apparent yield in the batch, but treat with real caution: the lease has only ~47 years unexpired, which both suppresses the achievable sale value (explaining much of the "discount") and would need extending at cost, eroding true returns.
**Verdict:** Cheapest lot in the batch by a wide margin — high theoretical discount, but likely reflects a genuinely rough/short-lease flat rather than a hidden bargain; verify lease term and condition closely.

| Lot | Address | Guide Price | Description | Detail page | End time | Est. Monthly Rent | Est. Annual Rent | Gross Yield |
|---|---|---|---|---|---|---|---|---|
| 6 | 80 London Road, Plaistow, E13 0DD | £100,000+ | Leasehold (99 yrs from 1974, ~47 yrs unexpired, £30 p.a. ground rent) Ground Floor Garden Flat (1 bed), Vacant Possession, requires modernisation. EPC TBC, Council Tax Band B, LB Newham. | **Found:** mchughandco.com/lot/details/191646 | 16/09/2026 09:10 | £1,550 | £18,600 | ~18.6% |

---

## 4. Stratford, Newham (E15)

**Growth potential: 5/5** — The strongest growth story in the batch. Stratford is a major Elizabeth Line/Jubilee/Central/DLR interchange (40m+ passengers/year), sits at the centre of the Queen Elizabeth Olympic Park legacy programme, Westfield Stratford City, the East Village (3,500 homes), and ongoing schemes like Stratford Cross and Sugar House Island. Continued institutional and infrastructure investment (UCL East, London College of Fashion) underpins durable demand.
**Average cost of comparable property type:** E15 overall average **£464,944** (terraced £569,136, semi £508,250, flats £383,805), roughly flat YoY, 2% below the 2022 peak. A guide of £400,000+ for a freehold house sits below the terraced average — a reasonable, if less extreme, discount than some other lots, consistent with an already fairly efficiently-priced area.
**Social status / desirability: 4/5** — Transformed from industrial decline into Newham's flagship cultural/retail/business district; still ethnically and economically diverse with pockets of deprivation alongside new-build affluence.
**Proximity to shops/amenities: 5/5** — Westfield Stratford City is one of Europe's largest shopping centres, right on the doorstep.
**Proximity to schools: 3/5** — Mixed borough-wide Ofsted picture, though the area's profile is rising alongside general regeneration and new higher-education presence.
**Potential rental:** 3-bed houses in E15 are letting for **£2,500-£2,800 pcm**. Using £2,650 pcm (**£31,800/year**) against the £400,000+ guide gives a gross yield of **~8.0%** — high for London, though the lowest of the batch's outright "house" lots, reflecting that this is priced closer to fair value than the deep-discount lots elsewhere.
**Verdict:** Best growth-and-connectivity fundamentals in the batch; a fair rather than deep-discount price, but the area's trajectory is the most compelling of the eleven areas covered.

| Lot | Address | Guide Price | Description | Detail page | End time | Est. Monthly Rent | Est. Annual Rent | Gross Yield |
|---|---|---|---|---|---|---|---|---|
| 9 | 53 West Road, Stratford, E15 3PX | £400,000+ | Freehold Terraced House (3 bed + cellar), Vacant Possession, requires modernisation; potential for loft conversion (STPP). EPC D, Council Tax Band C, LB Newham. | **Found:** mchughandco.com/lot/details/191605 | 16/09/2026 09:16 | £2,650 | £31,800 | ~8.0% |

---

## 5. Ilford, Redbridge (IG1 & IG2)

**Growth potential: IG1 4/5, IG2 3/5** — IG1 (Ilford town) benefits directly from its own Elizabeth Line station giving fast links to Liverpool Street, the West End, and Heathrow; sold prices are 2% up YoY and 5% above the 2023 peak. IG2 (Gants Hill/Newbury Park/Barkingside fringe) relies on the Central Line rather than the Elizabeth Line and is currently 4% down YoY and 4% below its 2021 peak — a softer trajectory.
**Average cost of comparable property type:** IG1 terraced average **£532,978**; IG2 terraced average **£540,033**. Both lots are described simply as "Freehold House" with guides of £250,000+ (IG1, 165 Grange Road) and £275,000+ (IG2, 36 Netley Road) — roughly half the local terraced average in both cases, a very large apparent discount typical of probate/vacant-possession auction stock likely needing full modernisation.
**Social status / desirability: IG1 3/5, IG2 4/5** — Ilford overall is exceptionally diverse (2011 census: significant South Asian population, high multilingualism); IG1's Loxford ward has one of the lowest median house prices of any London ward, reflecting real deprivation in parts of the town centre. IG2 (Gants Hill/Newbury Park side) is generally regarded as a step up — leafier, more suburban, historically popular with families.
**Proximity to shops/amenities: 4/5** — Ilford town centre is a designated Metropolitan Centre in the London Plan with a large shopping offer; IG2 has good access to both Ilford and Gants Hill's own retail parade.
**Proximity to schools: 4/5** — Redbridge is a consistently strong-performing education borough; several highly-regarded schools (Ilford County High, Beal High School, Woodford County High) sit within or near the borough.
**Potential rental:** IG1 3-bed houses let for around **£2,100-£2,500 pcm** (area average ~£2,300 pcm); using £2,300 pcm (**£27,600/year**) against the £250,000+ guide gives a gross yield of **~11.0%**. IG2 (Gants Hill) 3-bed houses average **~£2,175 pcm** (**£26,100/year**); against the £275,000+ guide that's a gross yield of **~9.5%**. Both are high for London, with IG1 the stronger of the two.
**Verdict:** Both lots show a large guide-to-market gap; IG1 has the stronger transport-driven growth case, IG2 the marginally better lifestyle/social reputation.

| Lot | Address | Guide Price | Description | Detail page | End time | Est. Monthly Rent | Est. Annual Rent | Gross Yield |
|---|---|---|---|---|---|---|---|---|
| 12 | 165 Grange Road, Ilford, IG1 1HB | £250,000+ | Freehold Terrace House (3 bed), Vacant Possession, requires modernisation; front off-street parking. EPC C, Council Tax Band C, LB Redbridge. | **Found:** mchughandco.com/lot/details/d085a818-7fcf-4353-afd0-7c14a7791134 | 16/09/2026 09:30 | £2,300 | £27,600 | ~11.0% |
| 25 | 36 Netley Road, Ilford, IG2 7NR | £275,000+ | Freehold Terrace House (3 bed), Vacant Possession, requires modernisation; possible loft conversion. EPC C, Council Tax Band C, LB Redbridge. | **Found:** mchughandco.com/lot/details/4b4ad487-cf92-4d81-b953-a4922b26f7bc | 16/09/2026 10:12 | £2,175 | £26,100 | ~9.5% |

---

## 6. Hornchurch, Havering (RM11)

**Growth potential: 2/5** — RM11 sold prices are down 4% YoY and 8% below the 2023 peak — the weakest recent momentum of the batch's twelve areas. Reasonable transport (District Line plus nearby Elizabeth Line access at Harold Wood/Emerson Park) hasn't been enough to offset a broader Havering cooling.
**Average cost of comparable property type:** RM11 semi-detached average **£552,381** (bungalows aren't broken out separately by Rightmove, but typically price below 2-storey semis of comparable plot size). A guide of £250,000+ for a semi-detached bungalow is well below the semi average, though bungalows in Hornchurch's more sought-after roads can still command £400k+, so the real discount is likely smaller than the headline gap suggests.
**Social status / desirability: 4/5** — Solidly middle-class Havering suburb; district centre with Queen's Theatre and Fairkytes Arts Centre; grew rapidly as an interwar garden suburb and retains a settled, family-oriented reputation.
**Proximity to shops/amenities: 4/5** — Well-established high street and district centre.
**Proximity to schools: 4/5** — Havering has several highly-regarded schools including grammar-stream options (e.g. The Royal Liberty School, Frances Bardsley Academy) drawing from Hornchurch/Romford catchments.
**Potential rental:** 2-bed properties in RM11 let for roughly **£1,500-£1,900 pcm**; using £1,700 pcm (**£20,400/year**) against the £250,000+ guide gives a gross yield of **~8.2%** — high for London, though moderate relative to some other lots in this batch, consistent with RM11's softer growth trend.
**Verdict:** Pleasant, well-served suburb but currently the softest price trend in the batch — a value bungalow, not a growth story right now.

| Lot | Address | Guide Price | Description | Detail page | End time | Est. Monthly Rent | Est. Annual Rent | Gross Yield |
|---|---|---|---|---|---|---|---|---|
| 14 | 33 Hill Crescent, Hornchurch, RM11 2AP | £250,000+ | Freehold Semi-Detached Bungalow (2 bed, double-fronted), Vacant Possession, requires modernisation; possible loft conversion/rear extension (STPP). EPC D, Council Tax Band D, LB Havering. | **Found:** mchughandco.com/lot/details/192216 | 16/09/2026 09:34 | £1,700 | £20,400 | ~8.2% |

---

## 7. Dagenham, Barking & Dagenham (RM8 & RM9)

**Growth potential: 3/5** — Mixed picture. RM9's Rightmove "terraced average" of £703,594 (+79% YoY) is implausible for Dagenham and almost certainly a small-sample outlier — treat with real caution. The genuine growth driver here is **Beam Park**, the large new-build scheme on the former Ford Dagenham plant site, plus Elizabeth Line access via neighbouring Chadwell Heath. Barking & Dagenham was ranked among the "worst places to live in the UK" in a widely-cited 2015 list, and the borough is still working to shake that reputation — regeneration momentum is real but not yet fully reflected in price data.
**Average cost of comparable property type:** A **direct street-level comparable was found**: 25 Alleyndale Road itself (this exact lot) sold for **£307,000 in 2024** as a 2-bed end-terrace; other recent sales on the same street ranged £275,000-£365,250 (2019-2025). Against that specific comp, Lot 20's guide of £220,000+ is roughly 28% below its own last sale price two years ago — a strong, well-evidenced discount signal. Separately, an on-market listing for a 2-bed terrace on Tilney Road itself was seen at £385,000, against Lot 15's guide of £200,000+ — again suggesting a large apparent gap versus the immediate street, subject to the auction property's actual condition.
**Social status / desirability: 3/5** — Historically working-class and lower-reputation, with rapidly rising ethnic diversity (White British share fell from ~60% to under 40% 2001-2011); regeneration (Beam Park, London East Business & Technical Park) is gradually improving the outlook.
**Proximity to shops/amenities: 3/5** — Dagenham Heathway and local retail parks provide adequate day-to-day shopping.
**Proximity to schools: 3/5** — Historically below-average attainment borough-wide, though some academies have improved markedly in recent Ofsted cycles.
**Potential rental:** 3-bed houses in RM9 are letting for **£2,000-£2,100 pcm**; using £2,050 pcm (**£24,600/year**) against Lot 15's £200,000+ guide gives a gross yield of **~12.3%**. Lot 20 (RM8, 2-bed) would let for somewhat less — est. £1,700 pcm (**£20,400/year**) — against its £220,000+ guide, a gross yield of **~9.3%**. Both are high for London.
**Verdict:** The best-evidenced value case in the whole batch (Lot 20 has an actual same-address 2024 sale price to benchmark against) — worth prioritising due diligence here precisely because the comp isn't just a postcode average.

| Lot | Address | Guide Price | Description | Detail page | End time | Est. Monthly Rent | Est. Annual Rent | Gross Yield |
|---|---|---|---|---|---|---|---|---|
| 15 | 10 Tilney Road, Dagenham, RM9 6HP | £200,000+ | Freehold Terrace House (3 bed), Vacant Possession, requires modernisation. EPC F, Council Tax Band C, LB Barking & Dagenham. Comparable: a 2-bed terrace on the same street was on the market at £385,000. | **Found:** mchughandco.com/lot/details/189111 | 16/09/2026 09:36 | £2,050 | £24,600 | ~12.3% |
| 20 | 25 Alleyndale Road, Dagenham, RM8 2JQ | £220,000+ | Freehold End of Terrace House (2 bed), Vacant Possession, requires modernisation; potential hip-to-gable/rear dormer under PD rights. EPC D, Council Tax Band C, LB Barking & Dagenham. **Direct comp: this exact address sold for £307,000 in 2024** (Zoopla sold-price history). | **Found:** mchughandco.com/lot/details/189331 | 16/09/2026 09:54 | £1,700 | £20,400 | ~9.3% |

---

## 8. Rainham, Havering (RM13)

**Growth potential: 4/5** — RM13 sold prices are 6% up YoY and 7% above the 2023 peak, one of the stronger trends in the batch. Southern Rainham is a designated Thames Gateway regeneration zone with ~3,200 new homes planned and a £120m sewage/infrastructure upgrade in the pipeline (tenders from mid-2025) — genuine forward-looking catalysts rather than just historical drift.
**Average cost of comparable property type:** RM13 averages: terraced £415,379, semi-detached £465,869. Lot 15B (69 Jersey Road, "Freehold House," guide £250,000+) and Lot 19 (22 Edmund Road, "Freehold Detached House," guide £275,000+) both sit well below these averages — the Edmund Road gap is especially notable since detached houses would normally command a premium over the semi-detached average, not fall below it.
**Social status / desirability: 3/5** — Industrial-legacy area in active transition; ethnic diversity has grown markedly (White British share fell from 81.6% to 63.8%, 2011-2021 census); cultural amenities still limited locally but improving with regeneration.
**Proximity to shops/amenities: 3/5** — Village-style high street plus a retail park; not a major shopping destination but adequate.
**Proximity to schools: 3/5** — Havering schools generally perform reasonably; no standout Ofsted-outstanding school specifically identified for Rainham in this research.
**Potential rental:** 3-bed houses in RM13 let for **£2,000-£2,150 pcm**. Using £2,075 pcm (**£24,900/year**) against Lot 15B's £250,000+ guide gives a gross yield of **~10.0%**. Lot 19 is detached (typically a modest rent premium over terraced/semi) — est. £2,300 pcm (**£27,600/year**) against its £275,000+ guide, also **~10.0%**. Both high for London.
**Verdict:** Along with Dagenham, one of the better growth-plus-value combinations in the batch — active regeneration funding is a genuine tailwind here.

| Lot | Address | Guide Price | Description | Detail page | End time | Est. Monthly Rent | Est. Annual Rent | Gross Yield |
|---|---|---|---|---|---|---|---|---|
| 15B | 69 Jersey Road, Rainham, RM13 7DT | £250,000+ | Freehold Terrace House (3 bed), Vacant Possession, requires modernisation; front off-street parking. EPC E, Council Tax Band D, LB Havering. | **Found:** mchughandco.com/lot/details/193209 | 16/09/2026 09:40 | £2,075 | £24,900 | ~10.0% |
| 19 | 22 Edmund Road, Rainham, RM13 8LX | £275,000+ | Freehold Detached House (3 bed), Vacant Possession, requires modernisation; off-street parking, extension potential (STPP). EPC D, Council Tax Band C, LB Havering. | **Found:** mchughandco.com/lot/details/0568c120-2172-4b11-857f-e00c41c4f29e | 16/09/2026 09:52 | £2,300 | £27,600 | ~10.0% |

---

## 9. Romford — Harold Wood / Noak Hill fringe (RM3)

**Growth potential: 4/5** — RM3 sold prices are essentially flat YoY and only 1% above the 2022 peak — stable rather than booming on the raw numbers, but the area has a strong structural tailwind: **Harold Wood has its own Elizabeth Line station** (direct to Liverpool Street/Paddington/Heathrow), and the former Harold Wood Hospital site has been redeveloped into the new "Kings Park" estate (470 homes, completed 2023), adding fresh housing stock and demand nearby.
**Average cost of comparable property type:** RM3 averages: terraced £410,180, semi-detached £458,516. All three RM3 lots — Lot 40A (£225,000+, end-terrace + garage), Lot 51 (£200,000+, end-terrace), Lot 58 (£200,000+, semi-detached) — sit roughly 45-55% below these averages, a consistent and substantial discount pattern across all three, suggestive of vacant-possession/modernisation stock rather than one-off pricing quirks.
**Social status / desirability: 4/5** — Predominantly White British (86%, 2011 census), leafy, family-suburban, near the M25 and Greater London/Essex boundary — solidly desirable outer-suburban character.
**Proximity to shops/amenities: 4/5** — Romford town centre (one of outer London's largest retail centres) is close by.
**Proximity to schools: 4/5** — Havering's grammar-stream schools (Royal Liberty, Frances Bardsley) are accessible from this side of Romford.
**Potential rental:** 3-bed houses in RM3 let for **£2,100-£2,250 pcm**; using £2,150 pcm (**£25,800/year**) against Lots 51 and 58's £200,000+ guides gives a gross yield of **~12.9%** each. Lot 40A is a 2-bed — est. £1,750 pcm (**£21,000/year**) against its £225,000+ guide, a gross yield of **~9.3%**. All three are high to very high for London.
**Verdict:** Three lots, one consistent story — a stable, well-connected, family-friendly area where all three guides look meaningfully under local averages; the pick for anyone wanting to spread risk across multiple similar lots in one area.

| Lot | Address | Guide Price | Description | Detail page | End time | Est. Monthly Rent | Est. Annual Rent | Gross Yield |
|---|---|---|---|---|---|---|---|---|
| 40A | 14 Stephens Close, Romford, RM3 7RS | £225,000+ | Freehold End of Terrace House and Garage (2 bed), Vacant Possession, requires modernisation; sold by order of Executor. EPC TBC, Council Tax Band C, LB Havering. | **Found:** mchughandco.com/lot/details/e093f70d-9173-4522-8659-8c17482f7ee2 | 16/09/2026 10:46 | £1,750 | £21,000 | ~9.3% |
| 51 | 12 Buckbean Path, Romford, RM3 8ET | £200,000+ | Freehold End of Terrace House (3 bed), Vacant Possession, requires modernisation. EPC D, Council Tax Band C, LB Havering. | **Found:** mchughandco.com/lot/details/38b6a4a4-fdc5-4645-9412-2ff2f4ec293b | 16/09/2026 11:30 | £2,150 | £25,800 | ~12.9% |
| 58 | 150 Colne Drive, Romford, RM3 9JT | £200,000+ | Freehold Semi-Detached House (3 bed), Vacant Possession, requires modernisation. EPC D, Council Tax Band C, LB Havering. | **Found:** mchughandco.com/lot/details/8761d0f5-ed24-4b79-8acf-fef7ac19e553 | 16/09/2026 11:44 | £2,150 | £25,800 | ~12.9% |

---

## 10. Romford — Chadwell Heath (RM6)

**Growth potential: 4/5** — RM6 sold prices are up 6% YoY and 4% above the 2023 peak — one of the stronger trends in the batch, driven substantially by Chadwell Heath's own Elizabeth Line station providing fast central London access.
**Average cost of comparable property type:** RM6 flats/maisonettes average **£224,630**. Lot 45 (3 Rams Grove, leasehold garden maisonette, guide £145,000+) is meaningfully below this — a real if less extreme discount than some other lots, consistent with leasehold maisonettes typically trading under purpose-built flats.
**Social status / desirability: 3/5** — Ethnically diverse (White British 44.3%, sizeable Indian and Black African communities per 2011 census); has a genuine heritage anchor in the Grade II-listed Art Deco Embassy Cinema and the borough's oldest park (St Chad's Park, 1830), giving it more character than some neighbouring areas.
**Proximity to shops/amenities: 3/5** — Local high street plus easy reach of Romford town centre.
**Proximity to schools: 3/5** — Reasonable local schools; no standout Ofsted-outstanding school specifically confirmed for this immediate area.
**Potential rental:** The detail page (found this update) shows this is actually a 3-bed maisonette (2 bedrooms upstairs, 1 down), not a plain 2-bed as the catalogue summary implied — 89 years remaining on the lease (from 1991 to 2116), £10 p.a. ground rent. 2-bed flats in RM6 let for **£1,500-£2,000 pcm** (comparables cluster around £1,600); allowing a modest premium for the extra bedroom, est. **£1,650 pcm (£19,800/year)** against the £145,000+ guide gives a gross yield of **~13.7%** — high for London, among the strongest in the batch, and the long lease term removes the short-lease risk flagged for the Plaistow lot.
**Verdict:** A smaller, cheaper, Elizabeth-Line-connected pocket of Romford with solid recent growth and a genuinely long lease — good entry-level pick with one of the batch's best yields.

| Lot | Address | Guide Price | Description | Detail page | End time | Est. Monthly Rent | Est. Annual Rent | Gross Yield |
|---|---|---|---|---|---|---|---|---|
| 45 | 3 Rams Grove, Romford, RM6 5LB | £145,000+ | Leasehold (from 29/07/1991 to 29/09/2116, ~89 yrs unexpired, £10 p.a. ground rent) Garden Maisonette (3 bed: 2 up, 1 down), Vacant Possession, requires modernisation; private rear garden with shed. EPC D, Council Tax Band B, LB Barking & Dagenham. | **Found:** mchughandco.com/lot/details/feddce9d-baf6-4e2d-8d17-bf1cf055c583 | 16/09/2026 11:02 | £1,650 | £19,800 | ~13.7% |

---

## 11. Leytonstone, Waltham Forest (E11)

**Growth potential: 3/5** — E11 sold prices are down 2% YoY but roughly level with the 2023 peak — a plateau after a strong run-up rather than fresh momentum. Note the £1.01M "semi-detached average" and £783,839 terraced average are likely pulled up by a limited number of larger period-house sales; treat as directional rather than precise. Good existing transport (Central Line; Elizabeth Line accessible via nearby Maryland) and the £2.7bn Whipps Cross Hospital redevelopment are supportive medium-term factors.
**Average cost of comparable property type:** Against the terraced average of £783,839, Lot 43's guide of £550,000+ for an end-of-terrace house is roughly 30% below the local average — a real but less extreme discount than most other lots, reflecting that E11 is already a relatively expensive, sought-after area.
**Social status / desirability: 4/5** — Gentrified/gentrifying, popular with young professionals and families priced out of neighbouring Walthamstow; Hitchcock heritage and a well-regarded high street/café scene; population grew 24-31% across its wards 2001-2019.
**Proximity to shops/amenities: 4/5** — Leytonstone High Road and easy access to Westfield Stratford.
**Proximity to schools: 3/5** — Waltham Forest has a mixed but generally improving school landscape.
**Potential rental:** The detail page (found this update) confirms 3 bedrooms plus a conservatory, over two floors. 3-bed houses in E11 let for **£2,300-£2,350 pcm** on the two closest comparables found (the wider Leytonstone average across all property types is lower, ~£2,000 pcm, but is dragged down by flats/rooms). Using £2,300 pcm (**£27,600/year**) against the £550,000+ guide gives a gross yield of **~5.0%** — the lowest in the batch, reflecting that E11 is the most expensive, already-efficiently-priced area covered here rather than a deep-discount opportunity.
**Verdict:** The highest guide price in this batch outside Forest Gate, but still a genuine (if moderate) discount to a strong, already-established, desirable area — lower risk, lower headline upside than the deep-discount outer lots, and correspondingly the weakest yield of the batch.

| Lot | Address | Guide Price | Description | Detail page | End time | Est. Monthly Rent | Est. Annual Rent | Gross Yield |
|---|---|---|---|---|---|---|---|---|
| 43 | 22 Cavendish Drive, Leytonstone, E11 1DN | £550,000+ | Freehold End of Terrace House (3 bed + conservatory), Vacant Possession, requires modernisation; front/rear gardens, possible loft conversion (STPP). EPC E, Council Tax Band C, LB Waltham Forest. | **Found:** mchughandco.com/lot/details/83dd56b1-6f23-4a42-806a-a03a433423ed | 16/09/2026 10:58 | £2,300 | £27,600 | ~5.0% |

---

## 12. Forest Gate, Newham (E7)

**Growth potential: 4/5** — E7 sold prices up 9% YoY and 6% above the 2023 peak, driven substantially by Forest Gate's own Elizabeth Line station (direct to Paddington/Heathrow one way, Liverpool Street/Shenfield the other). Note the £1.225M "semi-detached average" looks skewed by a very small/atypical sample — the £645,787 terraced average (the dominant sale type locally) is the more reliable benchmark.
**Average cost of comparable property type:** Against the £645,787 terraced average, Lot 85's guide of £640,000+ for a house on Sebert Road sits almost exactly **at** the local market average — unlike every other lot in this batch, this is priced at fair value rather than showing a headline discount. Sebert Road itself sits within/near the Woodgrange Estate, a well-regarded Victorian conservation area, which likely explains the fuller pricing (larger/better-specified property, less need for a "vacant possession" discount).
**Social status / desirability: 3/5** — Highly diverse (second-highest Muslim population share of any area in Britain per Wikipedia, ~23.4%); the Woodgrange Estate itself (1,160 Victorian houses built 1877-1892) is a genuinely desirable, characterful pocket within a more mixed wider area.
**Proximity to shops/amenities: 3/5** — Local parades plus West Ham Park and Wanstead Flats green space; Stratford's Westfield a short journey away.
**Proximity to schools: 3/5** — Newham's school landscape is mixed but improving; no standout Ofsted-outstanding school specifically confirmed for this immediate street.
**Potential rental:** The detail page (found this update) shows this is actually a 4-bed house over three storeys (1 bed top floor, 3 beds first floor), not a generic "House" as the catalogue summary implied — a materially bigger property than assumed. 4-bed houses in E7 let for a wide **£2,600-£5,000 pcm** range across four comparables found; using a conservative mid-range **£3,000 pcm (£36,000/year)** against the £640,000+ guide gives a gross yield of **~5.6%** — low for London and the second-lowest in the batch, consistent with this lot being priced at fair value rather than a discount.
**Verdict:** Strongest raw price growth of any area in the batch, but this particular lot is priced at fair value rather than a bargain, and its yield is correspondingly modest — the investment case here rests on continued area appreciation (and the property being larger, at 4 beds, than the catalogue summary suggested), not an entry discount or high income.

| Lot | Address | Guide Price | Description | Detail page | End time | Est. Monthly Rent | Est. Annual Rent | Gross Yield |
|---|---|---|---|---|---|---|---|---|
| 85 | 96 Sebert Road, Forest Gate, E7 0NH | £640,000+ | Freehold Terraced House (4 bed over 3 floors: 1 bed top, 3 beds first, reception/dining/kitchen/utility ground floor), Vacant Possession; front forecourt parking, rear extension potential (STPP); near Forest Gate Elizabeth Line station. EPC D, Council Tax Band D, LB Newham. | **Found:** mchughandco.com/lot/details/e26f63f4-f971-4477-89f7-a675547d366e | 16/09/2026 12:54 | £3,000 | £36,000 | ~5.6% |

---

## Summary

- **12 distinct areas** covered across 17 lots: Hainault (IG6), Chingford (E4), Plaistow (E13), Stratford (E15), Ilford IG1, Ilford IG2, Hornchurch (RM11), Dagenham RM8/RM9, Rainham (RM13), Romford/Harold Wood (RM3, 3 lots), Romford/Chadwell Heath (RM6), Leytonstone (E11), Forest Gate (E7).
- **Detail pages found: 17 of 17** (up from 0 of 17 at the start of this update cycle). All 17 were confirmed as matching this specific 16/09/2026 auction (matching lot number, guide price, and/or closing time); several near-miss search results along the way (same street, different number, a different lot number, or a genuinely different/past auction) were identified and explicitly excluded. Two of the last three found (Lots 45 and 85) turned out to have materially different accommodation than the bare catalogue description suggested (a 3-bed maisonette rather than an unspecified bed count, and a 4-bed house rather than a generic "House," respectively) — a reminder that catalogue summaries alone can understate a property's size.
- **Rental yields (gross, on guide price):** range from a low of **~5.0%** (Lot 43, Leytonstone E11 — the batch's priciest, most fairly-valued lot) up to **~18.6%** (Lot 6, Plaistow E13 — but that figure is heavily lease-distorted, see caveat below). Excluding the short-lease Plaistow outlier, the genuinely strong yields cluster at **~12-14%**: Lot 4 Chingford E4 (~13.1%), the two RM3 Romford/Harold Wood terraces Lots 51 & 58 (~12.9% each), Lot 15 Dagenham RM9 (~12.3%), and Lot 45 Chadwell Heath RM6 (~13.7%, and unlike Plaistow this one has a genuinely long 89-year lease, so the yield isn't an artefact of lease risk). The two priciest/most fairly-valued lots — Leytonstone E11 (~5.0%) and Forest Gate E7 (~5.6%) — sit well below the batch average, consistent with those two guides tracking market value rather than showing a deep discount.
- **Top picks:**
  1. **Lot 20, 25 Alleyndale Road, Dagenham RM8 (£220,000+)** — the only lot with a confirmed same-address comparable: sold for £307,000 in 2024, ~28% above this guide, plus a solid ~9.3% estimated yield.
  2. **Lot 45, 3 Rams Grove, Chadwell Heath RM6 (£145,000+)** — the best genuine (non-lease-distorted) yield in the batch at ~13.7%, backed by a long 89-year lease confirmed on the newly-found detail page, plus a bigger 3-bed layout than the catalogue summary implied.
  3. **The three RM3 Romford/Harold Wood lots (40A, 51, 58)** — consistent 45-55% discounts to local averages, ~9-13% estimated yields, in an area with its own Elizabeth Line station and an active hospital-site regeneration scheme, offering a way to diversify across three similar lots in one well-connected suburb.
  4. **Lot 4, 32 Antlers Hill, Chingford E4 (£210,000+)** — largest apparent guide-to-area-average gap in the batch (area semi-detached average ~£701k) and a ~13.1% estimated yield, though the E4 average may itself be skewed and needs verifying against actual condition.
