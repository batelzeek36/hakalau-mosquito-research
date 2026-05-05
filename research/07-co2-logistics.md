# CO2 Supply Logistics — 27 BG-Mosquitaire Traps, Hakalau (15 acres)

**Goal:** keep 27 Biogents BG-Mosquitaire CO2 traps fed for years with minimum hands-on burden on a non-technical operator. Property is rural Big Island, ~15 miles from Hilo town.

**Demand baseline (timer mode, 8 hr/day):**
- Per trap: 0.37 lb CO2/day
- Whole property: ~10 lb/day, ~300 lb/month, ~3,650 lb/year
- Continuous mode would triple this to ~890 lb/month — not recommended; the BG-CO2 timer cuts consumption ~67% with no measurable catch loss when set to dawn/dusk windows ([Biogents BG-CO2 Timer](https://us-shop.biogents.com/products/bg-co2-timer)).

---

## 1. Cylinder-Size Sizing Math

Days-per-trap and swaps-per-year (timer mode, 0.37 lb/day = 11.1 lb/month):

| Size | Gross weight (full) | Days/trap | Swaps/yr (27 traps) | Notes |
|---|---|---|---|---|
| 5 lb | ~12 lb | 13.5 | 730 | Ridiculous swap rate. Skip. |
| 20 lb | ~50 lb | 54 | 182 | Beverage-industry standard. One person can carry. |
| 50 lb | ~120 lb | 135 | 73 | Two-person lift. Hand-truck mandatory. |
| 100 lb | ~270 lb | 270 | 36 | Industrial. Cart-only. ~48" tall, 14" diameter. ([CryoFX 100 lb dimensions](https://www.cryofx.com/100-lb-co2-tank-dimensions)) |

**Critical multiplier — the BG-CO2 Timer manifolds up to 5 traps onto one cylinder** ([Biogents](https://eu.biogents.com/bg-co2-timer/)). At 5 traps per tank × 0.37 lb/day = 1.85 lb/day per cylinder:

| Size | Days/cluster (5 traps) | Swaps/yr (6 clusters) |
|---|---|---|
| 20 lb | ~11 days | ~170 |
| 50 lb | ~27 days | ~67 |
| 100 lb | ~54 days | ~33 |

**Verdict:** at 27 traps the manifold approach (Section 3) drops swap count from 182 to ~33-67/yr. Raw single-tank-per-trap is operationally untenable.

---

## 2. Hilo Suppliers + Pricing

**Airgas Hilo (W083)** — 525 Kalanianaole Ave · (808) 935-3341 · M-F 7am-4pm ([Airgas Hilo](https://locations.airgas.com/hi/hilo/airgas-store-w083.html)). Stocks beverage- and industrial-grade CO2 in 20/50/100 lb. Contract pricing roughly $25-40 (20 lb), $50-80 (50 lb), $90-130 (100 lb) — verify by phone, Hawaii surcharges apply. Cylinder lease ~$40-60/yr or deposit ~$80-150. ([WeldingWeb HI thread](https://www.weldingweb.com/threads/buying-argon-co2-gas-in-hawaii.703918/) confirms steep specialty-gas pricing in HI.)

**Big Island Welding** is in Captain Cook (Kona side, 100 mi away) and primarily mobile welding/fab, not gas distribution ([bigislandwelding.com](https://bigislandwelding.com)). Not a fit.

**Beverage alternatives:** Hilo restaurant-supply, kegerator/homebrew shops, and soda-fountain installers refill 5-20 lb tanks cheaply ($20-25/swap). Worth phoning Hilo Brewing Co. for a local beverage-grade exchange program — often faster than Airgas.

**Always use beverage-grade.** Industrial cylinders may contain steel filings that block Biogents regulators and release nozzles ([Biogents SEA](https://sea.biogents.com/attractants/carbon-dioxide-biogents-mosquito-traps/)). Cost difference is trivial; risk across 27 traps is not.

**Delivery:** Airgas runs Big Island route trucks. Hakalau (15 mi up Hamakua Coast) likely falls on the Hilo route — schedule recurring monthly drop-off so Amber never drives cylinders.

---

## 3. Manifold / Cluster Systems

**This is the architecture that makes 27 traps tractable.** Group traps into **6 clusters of 4-5 traps**, each with one shared 50 lb cylinder + one BG-CO2 Timer.

**Hardware per cluster:**
- 1× 50 lb beverage-grade CO2 cylinder (rented)
- 1× CGA-320 low-pressure regulator with output ~15 psi (Biogents-spec)
- 1× BG-CO2 Timer (~$140) — manages up to 5 trap outputs, programmable dawn/dusk windows, 9V battery lasts ~9 months
- 4-6 mm polyurethane CO2 line (food-grade), runs up to ~50-100 ft per trap from the timer
- T-fittings or 5-way distribution block (included with timer)

**Layout:** put the cylinder + timer at a covered "CO2 hub" centroid of each cluster (e.g. inside a small ventilated shed or under a roof), then run polyurethane tubing radially out to traps. Tubing is the cheap part; cylinder hubs are the expensive/heavy part. Six hubs × ~5 traps each works cleanly with the timer's 5-trap limit.

**Pros:** single regulator/timer per 5 traps, single refill point per cluster, swap count drops to ~67/yr (50 lb) or ~33/yr (100 lb).

**Cons:** long tubing runs need leak-tested unions and UV-resistant tube; one regulator failure idles 5 traps; pressure drops over very long runs (>200 ft) require a second regulator stage.

**Real-world precedent:** commercial greenhouse CO2 supplementation distributes from one bulk source via low-pressure manifold to dozens of injection points — same architecture ([Greenhouse Mgmt — CO2 enrichment](https://www.greenhousemag.com/article/carbon-dioxide-improve-plant-growth-co2-greenhouse-tech-solutions/)). The Mega-Catch CO2 Gas System uses the same beverage-cylinder + low-pressure-regulator pattern Biogents recommends ([Megacatch](https://megacatch.com/co2-gas-system/)).

---

## 4. Bulk Liquid CO2 Dewar

A 180 L liquid dewar holds ~330 lb at 350 psi, ~500 lb gross ([Airgas CD 180LT350](https://www.airgas.com/product/Gases/Carbon-Dioxide/p/CD%20180LT350)). Refills run $0.30-0.60/lb bulk vs $1-2/lb on small cylinders — annual gas drops ~$3,000 → ~$1,500. But: 1-3%/day boil-off losses, $60-100/mo dewar lease, and a real plumbing project (vaporizer + trunk line + 27 takeoffs, $2-5k). Single point of failure for the whole property. **Verdict:** makes sense only above ~500-700 lb/month with contractor install. At 300 lb/month, stick with cylinder clusters.

---

## 5. DIY / Alternative CO2 Sources

**Yeast + sugar fermentation** — 5 g yeast + 280 g sugar in 300 mL water generates ~32 ml/min CO2 for ~27 hr, ~94 g total ([Saitoh et al. 2017](https://www.sciencedirect.com/science/article/pii/S2221169117309802); [Smallegange et al. 2010](https://pmc.ncbi.nlm.nih.gov/articles/PMC2984570/)). Biogents sells a [BG-CO2 Generator](https://eu.biogents.com/bg-co2-generator/) for this. Output is ~5-10× lower flow than bottled, but field studies show yeast-baited BG traps catch **as many or more** mosquitoes than industrial-CO2 traps. Catch is real, not a scam. At 27 traps, refreshing 27 × 2 L bottles every 24-36 hr is a part-time job — useful as a **gap-filler** during delivery delays or for 2-3 high-priority traps near the lanai. Not primary.

**Dry ice** — sublimes 12-24 hr, daily Hilo runs, infeasible. **Compost CO2** — too low, unmetered. **Propane combustion** (Mosquito Magnet) — propane catalytically converts to CO2 + water at ~1 lb/day per unit ([Mosquito Magnet](https://www.mosquitomagnet.com/advice/how-it-works)). Hacking burners into Biogents = real engineering project (catalyst, ignition, safety interlocks); Mosquito Magnet platform itself has high failure rates. Skip.

---

## 6. Recommended Workflow for Amber

**Architecture:** 6 clusters × ~4-5 traps × 1 shared 50 lb cylinder + BG-CO2 Timer.

**Why 50 lb, not 100 lb:** 50 lb (~120 lb gross) rolls onto a $100 hand truck and Amber swaps it solo. 100 lb (~270 lb gross) needs two adults or a powered cart. The 100 lb option saves ~30 swaps/yr but adds an injury risk she shouldn't own.

**Cadence:** ~27 days per cluster × 6 = ~1 swap every 4-5 days, ~67/yr. Pair with monthly Airgas route delivery: 6 fresh in, 6 empties out, ~$300-500/mo gas + delivery. Amber's task: wheel full cylinder out, swap valve, wheel empty to staging pad. 15-20 min/swap.

**Storage:** Outdoor or open-sided shelter only. CO2 is heavier than air and pools in closed spaces — asphyxiation risk ([CO2Meter](https://www.co2meter.com/blogs/news/co2-tank-safety-precautions)). One shaded staging pad for full + empty cylinders, all chained upright. Each cluster hub gets a small lean-to roof with cylinder chained to a post.

**Transport:** Hand truck with cylinder strap for short hauls. UTV/Polaris Ranger bed with cylinder rack for cross-pasture moves. Never closed-cab.

---

## 7. Costs (5-Year Projection)

**Initial setup (6 clusters):**
| Item | Unit | Qty | Cost |
|---|---|---|---|
| 50 lb cylinder deposit (lease) | $100 | 12 (6 in service + 6 spare swap) | $1,200 |
| CGA-320 regulator | $80 | 6 | $480 |
| BG-CO2 Timer | $140 | 6 | $840 |
| Polyurethane tubing + fittings (~150 ft/cluster) | $100 | 6 | $600 |
| Hand truck + chains + brackets | — | 1 set | $250 |
| **Initial total** | | | **~$3,400** |

**Recurring (annual):**
- Gas refills: 67 swaps/yr × ~$60 (50 lb beverage-grade) = ~$4,000
- Delivery surcharge (rural Big Island): ~$50/visit × 12 = ~$600
- Cylinder lease (if not deposit-based): ~$50/yr × 12 = ~$600
- Tubing/regulator maintenance: ~$200/yr
- **Annual recurring: ~$5,400**

**5-year total: ~$30,400** ($3,400 setup + 5 × $5,400). Roughly $80-100/trap/month all-in. Compares favorably to propane Mosquito Magnets (~$15/trap/month propane + frequent unit replacement) once you account for unit reliability.

---

## 8. Safety

- **CO2 is heavier than air.** Never store cylinders in a basement, root cellar, closed shed, or any low-lying enclosed space. Outdoor or open-sided shelter only ([CO2Meter](https://www.co2meter.com/blogs/news/co2-tank-safety-precautions))
- **Securement.** Every cylinder chained or strapped upright at all times — full or empty. A falling 120 lb cylinder can shear a valve and become a projectile.
- **CO2 alarm rule.** International Fire Code requires a CO2 area alarm wherever >100 lb of CO2 is stored indoors. Open-air storage avoids this; if Amber wants a tool shed for the cylinders, install a $200 wall-mount CO2 monitor.
- **Transport.** Cylinders in pickup beds or UTV racks, valve-cap on, never in a sealed cab.
- **Hydro-test dates.** Airgas handles this on leased cylinders; check the stamped date on owned cylinders every refill. Don't refill an expired cylinder.
- **Hawaii regs.** No Hawaii-specific CO2 storage rules above CGA / NFPA federal baseline. Hawaii County may require permitting only if total on-site exceeds ~750 lb (verify with County Fire Prevention if dewar option ever revisited).
- **PPE.** Leather gloves on swap (cold valve burn risk); safety glasses. No special respirator needed outdoors.

---

## Final Recommendation

| Item | Spec |
|---|---|
| Architecture | 6 clusters of ~4-5 traps, manifolded via BG-CO2 Timer |
| Cylinder size | **50 lb beverage-grade CO2** |
| Cylinder count | 12 (6 active + 6 swap spares) |
| Swap cadence | ~1 cluster every 4-5 days; ~67 swaps/yr |
| Supplier | **Airgas Hilo** (525 Kalanianaole Ave, 808-935-3341), monthly route delivery |
| Setup cost | ~$3,400 |
| Recurring | ~$5,400/yr (~$450/month) |
| Operator burden | ~15-20 min per swap, ~1 swap per 4-5 days, ~5-7 hours/month |

This is the right balance for Amber: minimum lifting risk, predictable monthly cost, single supplier relationship, no exotic plumbing, and a clear escalation path (yeast generators as backup, dewar if scale grows).

---

## Sources

- [Biogents — Using CO2 to boost catch rate](https://us-shop.biogents.com/pages/using-co2-as-a-mosquito-attractant)
- [Biogents BG-CO2 Timer (US shop)](https://us-shop.biogents.com/products/bg-co2-timer)
- [Biogents BG-CO2 Timer (EU page — manifold-up-to-5-traps spec)](https://eu.biogents.com/bg-co2-timer/)
- [Biogents BG-CO2 Generator (yeast)](https://eu.biogents.com/bg-co2-generator/)
- [Biogents SE Asia — CO2 grade requirements](https://sea.biogents.com/attractants/carbon-dioxide-biogents-mosquito-traps/)
- [Airgas Hilo branch (W083)](https://locations.airgas.com/hi/hilo/airgas-store-w083.html)
- [Airgas 180L liquid CO2 dewar (CD 180LT350)](https://www.airgas.com/product/Gases/Carbon-Dioxide/p/CD%20180LT350)
- [Big Island Welding](https://bigislandwelding.com)
- [WeldingWeb — Hawaii gas pricing thread](https://www.weldingweb.com/threads/buying-argon-co2-gas-in-hawaii.703918/)
- [CryoFX 100 lb CO2 tank dimensions](https://www.cryofx.com/100-lb-co2-tank-dimensions)
- [CryoFX 50 lb CO2 tank dimensions](https://www.cryofx.com/50-lb-co2-tank-dimensions)
- [CO2Meter — CO2 tank safety](https://www.co2meter.com/blogs/news/co2-tank-safety-precautions)
- [CO2Meter — CO2 purity grade chart](https://www.co2meter.com/blogs/news/co2-purity-grade-charts)
- [Saitoh et al. 2017 — Yeast-generated CO2 for BG-Sentinel traps](https://www.sciencedirect.com/science/article/pii/S2221169117309802)
- [Smallegange et al. 2010 — Sugar-fermenting yeast CO2 for Anopheles](https://pmc.ncbi.nlm.nih.gov/articles/PMC2984570/)
- [Mosquito Magnet — How it works (propane catalysis)](https://www.mosquitomagnet.com/advice/how-it-works)
- [HowStuffWorks — Mosquito Magnet propane mechanism](https://home.howstuffworks.com/mosquito-magnet2.htm)
- [Megacatch — CO2 Gas System for mosquito traps](https://megacatch.com/co2-gas-system/)
- [Greenhouse Management — CO2 enrichment distribution](https://www.greenhousemag.com/article/carbon-dioxide-improve-plant-growth-co2-greenhouse-tech-solutions/)
- [Saftcart — 180L CO2 liquid dewar](https://saftcart.com/dewar-liquid-180-liter-co2/)
