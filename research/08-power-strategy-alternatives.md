# Power & CO2 Strategy Alternatives — Hakalau 27-Trap Deployment

**Site:** ~15 acres, Hakalau, Big Island. ~150" rain, frequently cloudy, year-round operation, non-technical operator (Amber).
**Default plan:** 27 BG-Mosquitaire CO2 with per-trap solar + per-trap 22-lb cylinder = 27 power install points + 27 cylinder swaps. This document evaluates alternatives that reduce that distributed-maintenance burden.
**Date:** May 2026.

---

## 1. Propane self-powered traps revisited

The pitch: catalytic propane combustion produces CO2 and thermoelectric power for the fan. One 20-lb tank ≈ 21 days (Patriot) or 30 days (Executive fuel-save). No batteries, one fuel source.

**2026 reality:** Mosquito Magnet (Woodstream) still sells Patriot Plus MM4200B and Executive MM3300B ([mosquitomagnet.com](https://www.mosquitomagnet.com/mosquito-magnet-executive-mosquito-trap-mm3300b)). 2026 reviews repeat the same failure modes: thermocouple corrosion at 6–12 mo, switch defects, typical failure after one season, no service centers within 3 states of most US buyers ([Today's Homeowner 2026](https://todayshomeowner.com/pest-control/reviews/mosquito-magnet-review/), [Home Depot MM4200B](https://www.homedepot.com/p/reviews/Mosquito-Magnet-Patriot-Plus-1-Acre-Outdoor-Trap-Silent-Ready-to-Use-Odorless-Trap-for-Mosquitoes-Black-Flies-and-No-See-Ums-MM4200B/305302047/1)). SkeeterVac SV5100 still at retail but never a serious vector unit; AMCA position: propane catalytic traps "not recommended due to notoriously high mechanical failure rates" ([mosquitoreviews.com 2026](https://mosquitoreviews.com/reviews/best-mosquito-trap/)). No surviving European or ABC-era alternative — refurbs share wear parts with Woodstream units.

**Logistics math for 27 Patriots:**

| Variable | Value |
|---|---|
| Tanks/yr (21-day cycle × 27) | 459 |
| Propane @ $25/refill | $11,475 |
| Octenol cartridges | $810 |
| ~30%/yr failures × $200 service | $1,600 |
| Year-1 capex (Patriots @ ~$700) | $18,900 |
| **5-yr TCO** | **~$88,000** |

vs. BG-Mosquitaire CO2 baseline ($62K/5yr, [05-recommendations.md](./05-recommendations.md)): propane is ~40% more expensive AND less reliable AND has zero peer-reviewed eradication evidence. The "simplification" is a mirage — 27 cylinder swaps + 27 solar checks become 459 propane swaps/yr (8.8/week — that *is* a route walk) plus a ~30%/yr failure rate Amber can't fix.

**Verdict: do not deploy propane self-powered.**

---

## 2. Hybrid deployment by tier

Pick the cheapest, most-reliable power per trap location.

| Tier | Location | Traps | Power |
|---|---|---|---|
| **T1 — House cluster** | <100 ft from residence | 6–8 | AC via outdoor GFCI + 33-ft Biogents weatherproof extension ($46, [Biogents](https://us-shop.biogents.com/en/mosquito-trap-accessories/bg-mosquitaire-extension-cable)). 5W = $5/trap/yr at HECO rates. |
| **T2 — Mid-zone** | 100–500 ft | 12–15 | Solar (per-trap or hub — see §3). Wet/cloudy → oversize panel 3× nameplate. |
| **T3 — Deep bush** | Gulches, far edges | 4–6 | BG-GAT passive, no power, no CO2; ~87% reduction in Aedes bites ([Biogents BG-GAT](https://us-shop.biogents.com/products/bg-gat-mosquito-trap-double-set)). |

This structural move drops the active-power install count from 27 → ~21 and active-CO2 cylinders from 27 → ~21. **Adopt regardless of which other options you also pick.**

---

## 3. Zonal solar hubs

One hub (300W panel + 100Ah LiFePO4 + MPPT + DC distribution) serves 5–7 nearby traps over buried 12 AWG cable.

**Voltage drop check (worst case, 200 ft, 5W):** 0.42 A × 0.32 Ω = **0.13 V (1.1%)** ✓ ([Renogy](https://www.renogy.com/blogs/buyers-guide/what-size-cable-for-12v-solar-panel)). Even a 7-trap trunk with all loads on one leg: <3% drop on 12 AWG out to 100 ft.

**Hub sizing for 6 traps × 5W × 12-hr timer = 360 Wh/day:**
- 100 Ah LiFePO4 = 1,200 Wh = 3+ days reserve at 80% DoD ([ExpertPower 10-yr cycle life](https://www.expertpower.us/products/ep1210-10ah))
- 300W panel × ~3 sun-hours (Hakalau cloudy derate) = ~900 Wh/day → 2.5× margin

**Cost for 4 hubs covering 24 traps:**
| Item | Cost |
|---|---|
| 4 hub kits (panel + LiFePO4 + MPPT + enclosure) | $4,800 |
| 12 AWG direct-burial + 1" PVC conduit (~1,500 ft) | $1,500 |
| Connectors, mounts, surge suppressors | $600 |
| **Hub system capex** | **~$6,900** |

vs. 24 × per-trap solar @ $220 = $5,280. **Hubs cost ~$1,600 more in capex** but consolidate failure surface from 24 panels/batteries to 4. One big LiFePO4 in a shaded enclosure outlives 24 small ones in baking trap-mounted boxes.

**Risks/mitigations:** lightning (Hakalau gets convective cells — ground every hub, surge-protect the trunk); wildlife (THWN-2 in 1" PVC conduit); single-hub failure cascades to 6 traps (keep one full spare hub kit in storage).

**Verdict: zonal hubs are the right T2 architecture.** Capex roughly equal, ~6× fewer points of failure, simpler annual inspection.

---

## 4. Battery swap from house

27 LiFePO4 12V 25Ah packs (~300 Wh @ ~$80/ea) charged at the house, swapped on rotation.

**Math:** 5W × 12 hr/day = 60 Wh/day. 300 Wh pack = 5-day runtime. 33 packs (27 + 6 spares) × $80 = **$2,640**. Plus 4-channel charger ~$300. **Capex ~$3,000.**

**Labor (the killer):** 5–6 swaps/day average over 27 traps. Walk time on 15 acres: 1.5–2 hr/day × 365 = **548–730 hr/yr**. At even $20/hr: **$11K–$15K/yr in labor alone**. For Amber this is a part-time job.

**Failure modes:** drop in mud, polarity errors at night, charging-station fire risk if a damaged pack is recharged.

**Verdict: economically and ergonomically bad as primary.** Per-trap solar already removes the charge-management problem. **Keep ~5 spare packs as field-emergency replacements** when a hub or AC line fails — that is a real win.

---

## 5. Reduced-trap-count alternative

Drop from 27 active CO2 → **17 active CO2 + 10 BG-GAT + Bti rotation + In2Care contractor**.

- 17 CO2 traps focused on residence + perimeter belt where AC + small solar are easy
- 10 BG-GAT in the deep bush (no power, no CO2; sticky-card swap every 6–8 wk)
- In2Care contractor (~$5K/yr for 10 stations) covers gulch breeding sites

**Logistics:** 17 power install points (vs. 27), 17 cylinder swaps (vs. 27), trivial BG-GAT service. **~37% reduction in service-touch points.**

**Coverage outcome:** 80–88% suppression vs. 90%+ in the 27-trap plan (per AMCA dose-response). Residual 10–15% sits in the deep bush — not where Amber actually is.

**Verdict: viable downshift if logistics is the binding constraint.** Honest tradeoff: lose ~5–10% interior suppression, lose ~37% service load.

---

## 6. Real-world large-deployment case studies

- **Soneva Fushi / Kunfunadhoo, Maldives** ([blog.biogents.com](https://blog.biogents.com/biogents_and_soneva)): ~500 traps on a 41-ha resort island, **95–98% suppression.** **CO2 source: yeast + sugar + water fermentation in 5L bottles — not compressed cylinders** ([Jahir 2022, PMC9503984](https://pmc.ncbi.nlm.nih.gov/articles/PMC9503984/)). Power: traps run on mains 12V DC adapters; the resort has its own microgrid with distributed outdoor outlets — they integrated into existing infrastructure rather than solving off-grid.
- **Puerco Island, Philippines** ([Knols 2023, PMC10531793](https://pmc.ncbi.nlm.nih.gov/articles/PMC10531793/)): same yeast-sugar protocol, complete elimination in 5 months.
- **Florida vector control** running BG-Sentinel use mains AC or 2–3-day battery swaps — no permanent off-grid arrays at this scale.

**Critical finding the original Hakalau plan missed.** Maldives uses yeast-sugar for CO2, not cylinders. Per station: 5L bottle, 3L water, 700g sugar, 20–40g yeast (or 20g BG-CO2 powder), refreshed weekly ([eu.biogents.com](https://eu.biogents.com/bg-co2-generator/), [yeast CO2 paper](https://www.sciencedirect.com/science/article/pii/S2221169117309802)). DIY cost: **~$2/trap/wk vs. ~$25/trap/wk for cylinder refills**. This eliminates the "27 cylinder swap points" problem — it becomes a kitchen task, not a route walk with a hand truck.

---

## 7. Final master recommendation

**Architecture: tiered hybrid with zonal solar hubs and yeast-sugar CO2.** This is what Soneva Fushi actually does, scaled to 15 acres.

| Tier | Traps | Power | CO2 |
|---|---|---|---|
| **T1 — House (8)** | BG-Mosquitaire CO2 | AC via 33-ft Biogents ext. to outdoor GFCIs | Yeast-sugar in 5L bottles, weekly batch in mudroom |
| **T2 — Mid-zone (13)** | BG-Mosquitaire CO2 | 3 zonal solar hubs (300W + 100Ah LiFePO4 + MPPT + 12 AWG buried trunk to 4–5 traps each) | Yeast-sugar refreshed on weekly walk |
| **T3 — Deep bush (6)** | BG-GAT passive | None | None |
| **Backstop** | ~10 In2Care | Contractor-serviced | n/a |

**Itemized year-1 capex:**

| Item | Qty | Unit | Subtotal |
|---|---|---|---|
| BG-Mosquitaire CO2 trap | 21 | $299 | $6,279 |
| BG-GAT trap | 6 | $40 | $240 |
| BG outdoor power supply + 33-ft ext (T1) | 8 | $83 | $664 |
| Solar hub kit (300W + 100Ah LiFePO4 + MPPT + box) | 3 | $1,200 | $3,600 |
| 12 AWG direct-burial + conduit + connectors | — | — | $1,500 |
| Yeast-CO2 station kits (5L bottle + tubing + insulator) | 27 | $25 | $675 |
| BG-CO2 powder starter | 5 | $35 | $175 |
| Bti year supply | — | — | $400 |
| Spare-parts kit + 5 emergency LiFePO4 swap packs | — | — | $1,100 |
| **Capex total** | | | **~$14,600** |

**Annual opex:**

| Item | Cost |
|---|---|
| Sugar (50 lb/wk × 52 wk × $0.60/lb wholesale) | $1,560 |
| Yeast (bulk active dry) | $200 |
| BG-Sweetscent + replacement lures | $810 |
| Bti year supply | $400 |
| Trap parts (~7%/yr × 27 × ~$60) | $115 |
| In2Care contractor (10 stations × $50/mo) | $6,000 |
| Misc (electricity ~$50, panel cleaning, etc.) | $300 |
| **Annual opex** | **~$9,385** |

Down from ~$12,000 in the cylinder-based plan. The cylinder savings alone fund most of the In2Care contract.

**Labor estimate (non-technical operator or hired help):**

| Task | Frequency | Hours |
|---|---|---|
| Yeast-sugar batch prep (kitchen) | Weekly | 0.5 |
| Route walk: refresh CO2 bottles + empty catch bags | Weekly | 2.0 |
| Solar hub inspection + battery voltage check | Monthly | 0.5 |
| BG-GAT sticky-card swap | Every 6 wk | 0.5 |
| Bti broadcast (gulches) | 10 d wet / 21 d dry | ~6/mo |
| **Monthly total** | | **~16 hr** |

vs. ~30 hr/mo in the original cylinder + per-trap-solar plan. **~47% labor reduction.**

**Failure modes:** hub solar failure → trap dark, yeast keeps producing ~48 hr, emergency LiFePO4 pack restores fan; >5-day cloud stretch → 100 Ah bank holds 3+ days at 80% DoD; yeast batch fails → ambient-CO2 mode (~70% drop in catch, visible at next refresh); fan motor death → 2-yr Biogents warranty + spares kit, <10 min replace; hub battery EOL at 8–10 yr → one swap per hub; hurricane → AC traps dark with grid, hubs ride through if panels survive (mount low, behind windbreak).

**5-year TCO:** ~$14,600 capex + 5 × $9,385 opex = **~$61,500** — roughly parity with the cylinder plan despite folding in the In2Care contractor, because yeast CO2 is ~10× cheaper per trap-week than cylinders.

**Bottom line.** Drop compressed cylinders entirely (yeast-sugar per Maldives protocol). Drop per-trap solar in favor of 3 zonal hubs (T2) plus AC at the house cluster (T1). Use BG-GAT in the deep bush (T3). Backstop the gulches with a contracted In2Care service. Service load drops to one weekly walk and one weekly kitchen batch — feasible for a non-technical operator or low-effort hired help.
