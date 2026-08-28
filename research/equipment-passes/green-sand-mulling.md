# Green Sand Mulling — Specialty Equipment Pass — Pass date: 2026-08-28 (revised)

Tracker line item #2 "Sand Mixer" — already sourced: **Simpson, "1F mix-muller," serial
1F-0113-1803**. This revision reframes the pass around the underlying technology and how it
needs to interface with the rest of the line, rather than leading with any one vendor.

## The technology: mulling vs. mixing

Mulling is a specific, more intensive form of sand preparation: muller wheels press the sand
against the chamber wall while plows shear and blend it, applying compression and controlled
shear rather than just stirring components together. That shear/compression is what fully
develops the sand-clay-additive bond — a plain paddle or turbine mixer doesn't get there. The
practical payoff is lower discharge sand temperature, more consistent moisture and compactability
run to run, and less scrap from bad sand; per ton mixed, mulling also tends to use less new sand,
power, and bentonite than turbine-style mixing.

## The real decision: batch vs. continuous architecture

Within mulling, the technology choice that actually drives system design is batch vs. continuous:

| Architecture | How it works | Throughput | Recipe flexibility | Best matched to |
|---|---|---|---|---|
| Batch | Sand, clay, water, and additives are charged into one chamber, mulled for a fixed cycle, then discharged | Lower steady-state throughput per unit of installed power — one foundry comparison found two 200 hp batch mullers were needed to match a single continuous unit of the same class | High — easy to trim water/recipe per batch, easy to change sand blend between jobs | Jobbing lines with a slower, less continuous molding rate (roughly 50–100 molds/hour) |
| Continuous | Sand is fed in one end and mulled in transit through multiple stages, discharging at a steady rate | Roughly double the throughput of a batch muller of comparable size/power | Lower — tuned for a steady recipe, less convenient for frequent formula changes | High-speed automatic molding lines (150+ molds/hour), where the muller has to keep pace continuously rather than in bursts |

## Vendor-by-technology

| Vendor | Batch product(s) | Continuous product(s) | Notes |
|---|---|---|---|
| Simpson | Mix-Muller, Speedmullor (high-speed batch) | Multi-Mull | The existing "1F mix-muller" on the tracker is almost certainly a Mix-Muller size designation — already a batch unit. |
| Palmer Manufacturing & Supply (Springfield, OH) | Batch sand mixers (M-Series and others) | Continuous sand mixers — Palmer markets itself as offering the most complete line of high-speed continuous sand mixers available | Independent US alternative with both architectures; worth a direct spec pull if a second quote is wanted. |

Other muller builders (e.g., National Engineering, Beardsley & Piper-descended lines) weren't
turned up with verifiable public specs in this pass — worth a direct inquiry if a broader
technology bake-off is wanted, but not enough here to compare responsibly.

## Compatibility check for a unified system

The sizing question isn't "which vendor" — the existing Mix-Muller is already batch, already on
site. It's **whether batch throughput matches whatever molding press gets selected**:

- A batch muller pairs cleanly with a horizontal matchplate press in the 50–100 molds/hour range
  (Hunter HMP-class) — see `molding-press.md`.
- A high-speed vertical or Seiatsu-class flaskless press (150–500 molds/hour) would very likely
  outrun a single batch Mix-Muller's cycle time and call for either a continuous muller (Multi-Mull
  or a Palmer continuous unit) or a sized sand surge hopper as a buffer between the two.

Get the "1F" Mix-Muller's rated batch size and cycle time from Simpson (serial 1F-0113-1803
should trace to exact specs) before the molding press decision is finalized — it's the upstream
constraint the press choice has to respect, not the other way around.

Sources: [Multi-Mull Continuous Mixer — Simpson](https://www.simpsongroup.com/multi-mull/) ·
[Muller Options for Foundry Mixing — Simpson](https://www.simpsongroup.com/muller-options/) ·
[Mix-Muller batch mixer — Simpson](https://www.simpsongroup.com/equipment/sand-preparation/mix-muller) ·
[Speedmullor Sand Mixer Overview — Simpson](https://www.simpsongroup.com/speedmullor/) ·
[Simpson Multi-Mull Continuous Mixer](https://www.simpsongroup.com/multi-mull-continuous-mixer/) ·
[Batch Sand Mixers — Palmer Manufacturing](https://www.palmermfg.com/batch-mixers.php) ·
[M-Series Sand Mixers — Palmer Manufacturing](https://www.palmermfg.com/m-series-mixers-options.php) ·
[Continuous Sand Mixers — Palmer corporate brochure](https://www.palmermfg.com/pdfs/2018-Palmer_CorporateBrochure-ENG_LR.pdf)
