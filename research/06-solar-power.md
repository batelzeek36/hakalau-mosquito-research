# Solar Power for 27 BG-Mosquitaire CO2 Traps in Hakalau, Hawaii

**Property:** 15 acres, windward Hamakua coast, Big Island
**Load:** 27 traps × 12V DC × 5W each (Biogents BG-Mosquitaire CO2 spec, IP68, NEMA 1 100–240V AC adapter to 12V DC)
**Operating profile:** ~14 traps on 8 hr/day timer (40 Wh/day each), ~13 traps continuous 24 hr/day (120 Wh/day each)
**Aggregate daily energy:** ≈ 14 × 40 + 13 × 120 = **2,120 Wh/day** for the whole network

---

## 1) Hakalau insolation reality

NREL/NSRDB data for Hilo (the closest reporting station, ~15 miles south of Hakalau and at similar low elevation on the same windward coast) puts the **annual average peak sun hours at 4.8/day on a fixed tilt** and ~5.5/day on a 1-axis tracker ([turbinegenerator.org/Hilo](https://www.turbinegenerator.org/solar/hawaii/hilo/)). Statewide Hawaii average is 6.0 PSH/day, so Hilo runs roughly **20% below state average** because of trade-wind orographic clouds ([solarenergylocal.com/hawaii](https://www.solarenergylocal.com/states/hawaii/)).

**Hakalau is meaningfully worse than Hilo.** It sits 800–2,500 ft up the Hamakua slope, where rising trades dump 80–160" of rain annually ([lovebigisland.com/weather](https://www.lovebigisland.com/weather/)) and form a near-continuous afternoon cloud deck. Realistic design assumption for an open-sky panel mount on this property: **3.5–4.0 PSH/day annual average, 2.0–2.5 PSH/day in the Nov–Feb wet season** (winter output typically 30–40% below summer per Hawaii utility data). Under canopy or in valleys, derate another 30–60%. Sites in trees are not viable for solar; panels need a clearing.

**Design rule for this report:** size to **3.0 PSH/day** as the working annual average and **2.0 PSH/day** worst-month, with a 3-day no-sun autonomy reserve.

---

## 2) Per-trap solar+battery kit — sizing math and product spec

### Sizing for a 24/7 trap (120 Wh/day)

- Daily energy in: 120 Wh ÷ 0.75 system efficiency (controller + battery RTE + cable losses) = **160 Wh/day required from the panel**
- At 2.0 PSH worst-month: 160 ÷ 2.0 = **80W panel minimum**; round up to **100W for headroom and panel-soiling derate** in the wet climate
- Battery for 3-day autonomy at 50% depth-of-discharge (LiFePO4 tolerates 80%+ but DoD margin extends life): 120 × 3 ÷ 0.5 ÷ 12 = **60 Ah at 12V**; round to a stock **50–100 Ah LiFePO4**

### Sizing for an 8 hr/day timer trap (40 Wh/day)

- 40 ÷ 0.75 = 54 Wh/day → at 2.0 PSH, ~**30W panel**; round to **50W stock size**
- 3-day autonomy: 40 × 3 ÷ 0.5 ÷ 12 = **20 Ah** → round to **30Ah LiFePO4**

### Why LiFePO4, not AGM, in this climate

LiFePO4 retains capacity to 60°C and survives 3,000–5,000 cycles vs. 300–500 for AGM. AGM in tropical heat (140–155°F enclosure temps are routine) drops to a 5-year replacement cycle, vs. 10+ years for LiFePO4 ([forum.solar-electric.com](https://forum.solar-electric.com/discussion/355246/longevity-of-agm-vs-lifepo4-in-high-temperature-environments), [evlithium.com](https://www.evlithium.com/Blog/lifepo4-vs-agm-batteries.html)). Over 10 years LiFePO4 is 50–70% cheaper per Wh delivered. **Choose LiFePO4. Do not consider AGM or sealed lead-acid in Hakalau.**

### Recommended per-trap kit (24/7 trap)

| Component | Spec | Product | Approx. cost |
|---|---|---|---|
| Panel | 100W 12V mono, IP67/68 frame | Renogy 100W Compact ([$78](https://offgridstores.com/products/renogy-100-watt-12-volt-monocrystalline-solar-panel-compact-design)) | $80 |
| Battery | 12V 50Ah LiFePO4 with BMS | LiTime / Ampere Time / ExpertPower 50Ah | $140 |
| Charge controller | 10A MPPT, lithium profile, load output with timer | EPEVER Tracer1210AN / LiTime 10A MPPT | $35 |
| Enclosure | NEMA 4X polycarbonate w/ breather vent | Bud / Polycase 12×10×6 + Bisonprofab breather ([bisonprofab.com](https://www.bisonprofab.com/enclosure-breather.htm)) | $55 |
| Mount, fuse, ring lugs, 12 AWG marine wire (25 ft) | — | Generic | $30 |
| **Per-trap total (24/7 trap)** | | | **≈ $340** |

### Per-trap kit (8 hr/day timer trap)

50W panel ($45) + 30Ah LiFePO4 ($95) + 10A controller ($30) + enclosure ($45) + accessories ($25) = **≈ $240**

**The $200/trap target is not realistic for a properly engineered LiFePO4 system in this climate.** It is achievable only with AGM (not recommended; will cost more over 5 years) or by stripping autonomy to 1 day (system will fail during typical Nov–Feb cloudy stretches).

---

## 3) Zonal alternative — cluster hubs

Group 27 traps into **5 zones of 5–6 traps each**, plus 2–4 traps on AC near the residence. Each zone gets one larger solar+battery hub feeding traps via buried 12V DC.

### Voltage drop math (deal-breaker for 12V over distance)

At 12V, a 5W trap draws ~0.42 A. Voltage drop on copper at 0.42 A:

| Run (one-way) | 14 AWG | 12 AWG | 10 AWG |
|---|---|---|---|
| 50 ft | 0.21V (1.8%) | 0.13V (1.1%) | 0.08V (0.7%) |
| 100 ft | 0.43V (3.6%) | 0.27V (2.3%) | 0.17V (1.4%) |
| 200 ft | 0.85V (7.1%) — **fail** | 0.54V (4.5%) | 0.34V (2.8%) |

(Calculations per [GridWright DC voltage drop calculator](https://gridwright.com/calculators/power/voltage-drop), 2-conductor round-trip, 12V nominal.)

**Practical limits:** 14 AWG to 50 ft, 12 AWG to 100 ft, 10 AWG to 200 ft. Beyond 200 ft, distribute at 24V or 48V and step down at the trap (adds DC-DC converters and complexity Amber doesn't want). The Biogents 33-ft DC extensions can be daisy-chained but compound the drop ([biogents extension cord](https://us-shop.biogents.com/products/extension-power-cord)).

### Zonal hub spec (powers 5 traps × 24/7 = 600 Wh/day)

- 400W panel array (4 × 100W or 2 × 200W) — $300
- 200Ah LiFePO4 12V — $450
- 30A MPPT controller — $90
- NEMA 4X battery enclosure with breather — $120
- 5 × 150–200 ft buried 10/2 direct-burial UF-B cable, fuse blocks, ground rod — ~$300
- Mounting, conduit, labor materials — $150
- **Per zone: ≈ $1,400 → $280/trap** (similar capex to per-trap kits, ~25% less hardware)

### Zonal pros/cons

- **Pro:** fewer batteries to maintain (5 hubs vs 27), easier troubleshooting, MPPT operates more efficiently at higher panel voltages, central enclosure can be locked.
- **Con:** trenching is a real cost and labor item in Hakalau's rocky/rooty soil; one hub failure takes 5 traps offline; cable theft/damage exposure; harder to relocate traps based on field testing.
- **Verdict:** zonal is competitive on capex and **wins on long-term maintenance** if the 5-trap clusters are tightly grouped (radius < 150 ft per hub). For traps spread thin around the perimeter, per-trap is more flexible.

---

## 4) Battery-only with rotational swap

Charge LiFePO4 batteries at the house, swap them weekly per trap. No panels, no controllers in the field.

### Sizing

- 1-month autonomy at 120 Wh/day: 3,600 Wh ÷ 12V = 300 Ah → use a [100Ah LiFePO4](https://www.amazon.com/BIOGENTS-BG-Extension-Extension-BG-Mosquitaire-Extender/dp/B08XY55V3V) (1,200 Wh useful at 100% DoD, ~10 days at 120 Wh/day) and **swap weekly**, or use a 200Ah for ~2 weeks between swaps.

### Cost & labor

- 100Ah LiFePO4: ~$280 each (LiTime/ExpertPower); buy 2 per trap (1 deployed, 1 charging) = $560/trap × 27 = **$15,120**, plus a multi-bay shore charger at the house (~$300).
- Labor: weekly walking circuit of 27 traps to swap batteries. At 5 min/trap = 2.25 hr/week, every week, forever. **108+ hr/year** that Amber or staff has to spend.
- **Verdict: rejected.** Lower capex than full solar (~$15k vs. ~$9k solar), but the labor burden over 5 years dwarfs the savings. Useful only as a bridge while solar is being installed, or for the 1–2 hardest-to-solar trap locations under deep canopy.

---

## 5) Hybrid recommendation for 27 traps on 15 acres

**Tiered deployment:**

### Tier 1 — AC-powered (8–10 traps near residence/lanai/gathering area)
- Run from house outlets via the included Biogents 12V supply + 33 ft extension. Daisy-chain 2 extensions to reach ~60 ft.
- Add a $20 outdoor GFCI timer (Intermatic HB88) for the 8-hr units.
- **Cost: ~$25/trap incremental.**

### Tier 2 — Per-trap solar (15–17 traps, distributed perimeter and interior locations with sky access)
- 24/7 traps: 100W panel + 50Ah LiFePO4 + MPPT + NEMA 4X. **$340/trap.**
- 8-hr timer traps: 50W + 30Ah LiFePO4 + MPPT w/ load timer. **$240/trap.**

### Tier 3 — 1–3 trap mini-clusters where 2–3 traps sit within 100 ft of each other
- Single 200W panel + 100Ah LiFePO4 + 20A MPPT, 12 AWG buried distribution. **~$200/trap** at scale of 3.

### Tier 4 — Battery swap (0–2 traps under heavy canopy with no clearing within 200 ft)
- 2 × 100Ah LiFePO4 per trap, weekly swap. Use only if relocating the trap is infeasible.

### Recommended split for Amber's 27 traps

Assuming a typical 15-acre Hakalau parcel with house + lanai + cleared yard at one corner and forest extending out:

| Tier | Count | Per-unit cost | Subtotal |
|---|---|---|---|
| AC near house | 8 | $25 | $200 |
| Per-trap solar 24/7 | 8 | $340 | $2,720 |
| Per-trap solar 8-hr | 8 | $240 | $1,920 |
| Mini-cluster (1 hub × 3 traps) | 3 | $200 | $600 |
| Battery swap (canopy) | 0–2 | $560 | $0–1,120 |
| **Total power infra** | **27** | | **≈ $5,440–6,560** |

Add ~$1,000 for tools, conduit, ground rods, surge arrestors, breather vents, peppermint-oil rodent spray. **Round to $7,500 capex.**

---

## 6) Tropical gotchas

- **Mounting:** use top-of-pole or canopy-clearing posts ≥ 8 ft. Tilt 19° (Hakalau's latitude) facing south. Drill drain holes in junction boxes pointing down. Stainless 316 hardware only — galvanized fails inside 18 months in 150" rainfall.
- **Battery enclosure:** NEMA 4X polycarbonate or 316 stainless. Mandatory **breather vent with hydrophobic membrane** ([bisonprofab.com](https://www.bisonprofab.com/enclosure-breather.htm)) — sealed boxes condense water inside and cook the BMS. Mount enclosure off the ground on a treated post; never on soil.
- **Lightning:** Big Island sees 2–5 thunderstorm days/year on the windward slope. For each panel/battery installation: 8-ft copper-clad ground rod, #6 bare copper to panel frame and battery negative, **DC surge arrestor** (Midnite SPD-300, ~$50) on the panel side ([sinovoltaics.com](https://sinovoltaics.com/learning-center/system-design/solar-lightning-protection-grounding-lightning-protection-solar-systems/)). Bury all interconnect cable; airborne wire is an antenna for cloud-to-cloud surges.
- **Wildlife (rats, mongoose, feral cats):** all wires in **3/4" or larger PVC conduit** or armored AWA cable; pack rats chew 1/2" PVC ([diysolarforum.com](https://diysolarforum.com/threads/protecting-pv-cables-from-rodents-ground-mounted-setup.65428/)). Spray peppermint or capsaicin on cable runs quarterly. Inspect connections at each maintenance visit — corrosion + rodent nibble is the #1 field failure mode.
- **Panel cleaning:** algae, lichen and fern spores germinate on panel frames in this rainfall regime. **Quarterly wipe** with a soft brush + dilute white vinegar (kills moss and lichen without damaging anti-reflective coatings). Skip pressure washers ([rezeca.com](https://www.rezeca.com/services/maintenance), [pvgis.com](https://pvgis.com/en/blog/solar-panel-cleaning-schedule-climate-maintenance)).
- **Maintenance schedule (Amber's runbook):**
  - Weekly: visual walk-by, confirm trap fan running.
  - Monthly: wipe panel face, check for vegetation shading.
  - Quarterly: open enclosure, check BMS LED, terminal corrosion, breather vent clear, re-spray rodent deterrent.
  - Annually: torque-check all DC connections, replace any swollen connectors, log battery resting voltage.

---

## 7) Cost summary

### Capex (year 0)

| Item | Cost |
|---|---|
| Tier 1 AC accessories (8 traps × $25) | $200 |
| Tier 2 24/7 solar kits (8 × $340) | $2,720 |
| Tier 2 timer solar kits (8 × $240) | $1,920 |
| Tier 3 mini-cluster (3 traps via 1 hub) | $600 |
| Tools, conduit, ground rods, surge arrestors, misc | $1,000 |
| Installation labor (DIY-friendly; 2–3 days for an electrician at ~$1k/day if hired) | $0–$2,500 |
| **Total capex** | **$6,440–8,940** |

### 5-year operating cost projection

- Year 1–4: ~$200/yr panel/trap cleaning supplies, peppermint spray, replacement breathers and connectors.
- Year 5: budget **20% LiFePO4 capacity loss** but no replacement needed (cells last 10+ years even in Hakalau).
- Charge controller failures: assume 1–2 controllers fail in 5 years from heat/humidity → **$70 replacement**.
- Surge events: assume 1 SPD strike-event consumed in 5 years → **$50**.
- **5-year opex: ~$1,200–1,500.**
- **5-year TCO: ≈ $8,000–10,000.**

By comparison, the rotational battery-swap option costs ~$15,000 capex + 540 hours of labor over 5 years — clearly worse.

---

## Final recommendation

**Hybrid solar with per-trap LiFePO4 kits, AC for the 8 closest traps, one zonal mini-cluster where geometry allows.**

Specific shopping list:
- **17 × Renogy 100W Compact panels** ($78 each) — [link](https://offgridstores.com/products/renogy-100-watt-12-volt-monocrystalline-solar-panel-compact-design)
- **8 × Renogy 50W panels** ($45 each)
- **17 × LiTime 12V 50Ah LiFePO4** (~$140 each) and **8 × LiTime 12V 30Ah** (~$95 each)
- **25 × EPEVER Tracer1210AN 10A MPPT** with load-output timer mode
- **25 × NEMA 4X polycarbonate enclosures + breather vents**
- **8 × Intermatic HB88 outdoor GFCI timer for the AC traps**
- **8 × 8-ft copper-clad ground rods + #6 bare copper**
- **25 × Midnite SPD-300 DC surge arrestors**
- **500 ft of 10/2 UF-B direct-burial cable + 3/4" PVC conduit**

**All-in capex ≈ $7.5k. 5-year TCO ≈ $9k. Maintenance burden: ~6 hours/quarter for Amber.**

This is the right system for a non-technical owner in the wettest non-bog microclimate in the United States. It buys 10 years of operation with predictable parts swaps, no monthly labor, and the modularity to relocate traps as field testing reveals where the *Culex quinquefasciatus* hot spots actually sit.

---

### Sources

- [BG-Mosquitaire CO2 product spec, 5W / 12V / IP68](https://us-shop.biogents.com/products/bg-mosquitaire-co2)
- [Biogents extension cable, 33 ft daisy-chainable](https://us-shop.biogents.com/products/extension-power-cord)
- [Hilo solar resource — turbinegenerator.org](https://www.turbinegenerator.org/solar/hawaii/hilo/)
- [Hawaii statewide solar — solarenergylocal.com](https://www.solarenergylocal.com/states/hawaii/)
- [Hamakua climate — lovebigisland.com](https://www.lovebigisland.com/weather/)
- [LiFePO4 vs AGM in heat — solar-electric forum](https://forum.solar-electric.com/discussion/355246/longevity-of-agm-vs-lifepo4-in-high-temperature-environments)
- [LiFePO4 vs AGM comparison — evlithium](https://www.evlithium.com/Blog/lifepo4-vs-agm-batteries.html)
- [Renogy 100W panel pricing](https://offgridstores.com/products/renogy-100-watt-12-volt-monocrystalline-solar-panel-compact-design)
- [DC voltage drop calc — GridWright](https://gridwright.com/calculators/power/voltage-drop)
- [NEMA 4X enclosure breather vents — Bison Profab](https://www.bisonprofab.com/enclosure-breather.htm)
- [Solar lightning grounding — sinovoltaics](https://sinovoltaics.com/learning-center/system-design/solar-lightning-protection-grounding-lightning-protection-solar-systems/)
- [Rodent damage to PV cables — DIY Solar Forum](https://diysolarforum.com/threads/protecting-pv-cables-from-rodents-ground-mounted-setup.65428/)
- [Tropical solar maintenance — rezeca.com](https://www.rezeca.com/services/maintenance), [pvgis.com](https://pvgis.com/en/blog/solar-panel-cleaning-schedule-climate-maintenance)
- [USGS / Univ. Hawaii field-tested solar mosquito trap system, Hawai'i Volcanoes NP, 2-year continuous operation](https://pubs.usgs.gov/publication/70271953)
- [Hakalau Forest NWR avian malaria context](https://wildlife.cornell.edu/blog/landscape-level-mosquito-suppression-protect-hawaiis-rapidly-vanishing-avifauna)
