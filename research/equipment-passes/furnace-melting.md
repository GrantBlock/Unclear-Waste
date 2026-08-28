# Melting Furnace — Specialty Equipment Pass — Pass date: 2026-08-28

Tracker line item #9 "Furnace" — currently lists "Stahl Specialty Co" under FROM/MFG. Stahl
Specialty is an aluminum foundry (Kingsville, MO), not a furnace manufacturer, so this reads as
the customer's reference/prior employer rather than an actual OEM — **treat as unsourced** for
the TO column.

## Terminology check: "electric arc furnace" isn't the standard fit for aluminum

The request named an electric arc furnace (EAF), but EAFs are the steelmaking/ferrous-scrap
tool — a graphite-electrode arc struck directly through the charge. That's not how aluminum is
melted commercially: aluminum's low melting point (~660°C) and its sensitivity to hydrogen
pickup and oxidative/dross loss make a direct arc a poor fit — it burns metal and produces
inconsistent quality. Aluminum foundries instead use gas-fired reverberatory furnaces,
**electric resistance** furnaces, or **induction** furnaces. If "electric arc furnace" was
shorthand for "an electric (not gas-fired) melting furnace," resistance or induction is almost
certainly the right family to quote — worth confirming with the customer before an RFQ goes out.

| Furnace type | How it heats | Fit for green sand Al | Notes |
|---|---|---|---|
| Electric arc (EAF) | Direct arc through charge | Poor | Steel/ferrous scrap tool; not used for aluminum production melting |
| Electric resistance (reverberatory) | Radiant resistance elements above bath | Good | Common in mid-size Al foundries; no coil cooling loss; simple to maintain |
| Induction (coreless/channel) | Electromagnetic eddy currents | Good, best alloy control | Built-in stirring aids alloy homogeneity; coil cooling reduces net efficiency; higher capital cost |
| Gas-fired reverberatory | Burner + refractory radiant | Good, lower capex | Common where electric rates are high; more emissions/dross to manage |

## Vendor options

| Vendor | Product line | Type | Capacity range | Fit notes | Source |
|---|---|---|---|---|---|
| StrikoWestofen (Norican Group) | StrikoMelter MH II (shaft/stack melter, stationary or tilting), Westomat ProDos dosing furnaces | Electric/gas shaft melting + holding, integrated dosing | MH II series ~750–3,000 kg bath, 500–2,000 kg/h melt rate | Sister company to Simpson (both Norican) — same parent as the customer's existing sand-side equipment. Westomat dosing furnace can feed metal directly to a mold or casting machine, which could fold the "Furnace Pouring Robot" line item (#10) into the furnace package instead of a separate robot cell. | [strikowestofen.com](https://www.strikowestofen.com/melting-and-holding-furnaces/), [StrikoMelter capacity data](https://www.diecastmachinery.com/UserFiles/InventoryFiles/d/DieCastMachinery-2504-059f6d7e86d695b94ab07906ae69309a.pdf) |
| Modern Equipment Company | Reverberatory and resistance melt/hold furnaces | Gas or electric resistance | Sized to order | Established US aluminum furnace builder; came up alongside Lindberg-MPH and FW Schaefer in supplier listings, but public spec detail is thin — go direct for a quote. | [diecastmachinery.com furnace listing](https://www.diecastmachinery.com/Aluminum-Melting-Furnaces.php) |
| The Schaefer Group (FW Schaefer) | Electric aluminum melt/hold furnaces | Electric resistance | Sized to order | Named as a peer to Modern Equipment in the same search pass; not independently verified beyond the vendor page found. | [theschaefergroup.com](https://www.theschaefergroup.com/electric_aluminum.php) |
| Inductotherm | Coreless induction melting | Induction | Wide range, kg to multi-ton | Not directly found in this pass's searches but is the dominant induction-furnace name in North America; include if the customer wants induction quoted for its alloy-control benefit. | Not directly sourced this pass — verify before quoting |

## Recommendation for next step

Get a StrikoWestofen quote first given the Norican/Simpson relationship — ask the Simpson rep
already on this project to make the introduction, since a single-group deal may simplify
commissioning and service. Get Modern Equipment or Schaefer as an independent second quote to
keep pricing honest. Confirm melt-rate requirement (kg/h or lb/h) against the line's target mold
throughput before sizing any of these — that number wasn't in the tracker and drives furnace
size more than anything else.

Sources: [Electric Arc Furnace vs Induction Furnace: Efficiency Analysis](https://eureka.patsnap.com/report-electric-arc-furnace-vs-induction-furnace-efficiency-analysis) ·
[Electric arc furnace (Wikipedia)](https://en.wikipedia.org/wiki/Electric_arc_furnace) ·
[Induction furnace (Wikipedia)](https://en.wikipedia.org/wiki/Induction_furnace) ·
[The Gap Narrows Between Induction and EAF](https://www.foundrymag.com/melt-pour/media-gallery/21931933/the-gap-narrows-between-induction-and-eaf) ·
[StrikoWestofen melting and holding furnaces](https://www.strikowestofen.com/melting-and-holding-furnaces/) ·
[STRIKOMELTER PLUS](https://www.strikowestofen.com/strikomelter-plus/) ·
[Norican Acquires Simpson Technologies](https://www.foundrymag.com/issues-and-ideas/article/21252372/norican-acquires-simpson-technologies-norican-group) ·
[Simpson Joins Norican Group](https://www.simpsongroup.com/news/simpson-joins-norican-group/)
