# Molding Press — Specialty Equipment Pass — Pass date: 2026-08-28 (revised)

Tracker line items #5 "Molding Hopper" and #6 "Molding Press" — both unsourced. This revision
compares the actual molding mechanisms across the field rather than leading with any one vendor,
since the mechanism chosen here determines what the rest of the line has to look like.

## Four real mechanisms, not four brands

| Mechanism | How it compacts the mold | Flask handling | Typical speed | Changeover |
|---|---|---|---|---|
| Vertical flaskless shot + squeeze | Sand is shot into a vertical chamber and squeezed between two pattern halves facing each other, producing cope and drag in one stroke, ejected as a continuous string of molds | Flaskless — no flask to return | Fastest of the four — up to 450–500 molds/hour on the largest machines | Historically the least flexible for frequent pattern swaps; hybrid designs address this (see below) |
| Horizontal matchplate flaskless | Pattern mounted on both faces of a plate; sand is blown/jolted and squeezed horizontally, mold ejected onto a conveyor | Flaskless — no flask to return | Moderate — roughly 100 molds/hour on a mid-size machine | Fast — swap the matchplate, not the whole tool set; well suited to jobbing work |
| Horizontal high-pressure ("Seiatsu") flaskless | Same horizontal matchplate layout, but squeeze pressure is higher and more uniformly applied than jolt-based compaction | Flaskless — no flask to return | Fast — up to 200 molds/hour on the highest-rate machine found this pass | Similar to standard matchplate; pressure control adds mold hardness/dimensional consistency |
| Tight-flask jolt-squeeze | Sand compacted in a flask that returns to the machine after each cycle, via jolt, squeeze, or high-pressure squeeze | Flask-based — needs a flask-return loop | Varies by machine | Flask handling adds mechanical complexity but is a mature, well-understood process |

**The fork that matters most for system design:** flaskless vs. tight-flask. A flaskless choice
means the mold-handling conveyors just carry a self-contained mold through the line. A tight-flask
choice means the conveyor system has to return empty flasks to the press — a materially different
mold-handling design, not a drop-in swap.

## Vendor-by-technology, with real throughput where found

| Vendor | Product | Mechanism | Rated speed | Notes |
|---|---|---|---|---|
| DISA | DISAMATIC (D-series) | Vertical flaskless shot + squeeze | Up to 450–500 molds/hour | Highest volume option; DISA's own material says the straight DISAMATIC line isn't the best fit for smaller shops with frequent pattern changes. |
| DISA | DISA MATCH | Vertical shot/squeeze combined with horizontal matchplate tooling | Not published in this pass | Positioned specifically to bring DISAMATIC-grade compaction to jobbing-style pattern flexibility. |
| Hunter Foundry Machinery | HMP-20 | Horizontal matchplate flaskless | Up to 100 molds/hour | Specifically called out for aluminum work; US-based (Illinois). |
| Hunter Foundry Machinery | HLM | Horizontal matchplate flaskless, magnetically-coupled rodless cylinders | Not published in this pass | Positioned for jobbing foundries and fast ROI; rate not found in public sources this pass — get directly from Hunter. |
| Sinto / Heinrich Wagner Sinto (HWS) | FBO | Horizontal high-pressure (Seiatsu) flaskless | ~130 molds/hour average (80/hr without core-setting, 50/hr with, in one cited application) | German/Japanese-engineered line (Sinto Group), US sales and service through Sinto America. |
| Sinto / HWS | FCMX | Horizontal high-pressure (Seiatsu) flaskless | Up to 200 molds/hour | Described by Sinto as the fastest flaskless molding machine available at introduction. |
| EMI + Savelli | Automatic Tight Flask / Jolt & Squeeze, Formimpress | Tight-flask, including a patented high-pressure squeeze system | Not published in this pass | US manufacturer (Cleveland, OH) partnered with Savelli (Italy); the one tight-flask option in this set — would require a flask-return conveyor loop instead of the pass-through layout the other options use. |

## Compatibility check for a unified system

Three numbers have to line up across the whole sand/metal loop, and the molding press sets the
pace for two of them:

1. **Mulling supply rate** — a 450-molds/hour DISAMATIC-class machine needs continuous mulling
   (Multi-Mull or a Palmer continuous unit); a 50–100 molds/hour matchplate machine can run on
   the batch Mix-Muller already on site. See `green-sand-mulling.md`.
2. **Furnace melt/hold rate** — molds/hour × metal weight per mold sets the minimum kg/h the
   furnace needs to sustain. See `furnace-melting.md`.
3. **Flaskless vs. tight-flask** — decides whether the mold-handling conveyors are simple
   pass-throughs or need a flask-return loop, which is a structural difference in the rest of the
   line's layout, not just a machine spec.

Get target mold size and molds/hour fixed first — every number above (mulling architecture,
furnace size, conveyor design) is downstream of that one decision.

Sources: [DISAMATIC (Wikipedia)](https://en.wikipedia.org/wiki/DISAMATIC) ·
[DISAMATIC D3 — DISA](https://www.disagroup.com/d3/) ·
[Matchplate moulding for green sand casting explained — DISA](https://disagroup.com/en-us/matchplate-explained) ·
[A New Look for High-Volume Moldmaking — Foundry Mgmt & Tech](https://www.foundrymag.com/molds-cores/article/21930769/a-new-look-for-high-volume-moldmaking) ·
[Hunter HMP-20 spec (Alumco)](https://alumco.net/equipment/sand-preparation-moulding-equipment/hunter-hpm-20/) ·
[Hunter Foundry Machinery](https://hunterfoundry.com/) ·
[Flaskless Moulding Machines and Lines — Heinrich Wagner Sinto](https://www.wagner-sinto.de/en/products/flaskless-moulding-machines-and-lines/) ·
[FBO Flaskless Molding Machine — Sinto America](https://sintoamerica.com/product/fbo-flaskless-molding-machine/) ·
[FCMX — The Industry-Defining Automatic Molding Machine — Foundry Mgmt & Tech](https://www.foundrymag.com/molds-cores/article/21214290/fcmx-the-industry-defining-automatic-molding-machine-sinto-america-inc) ·
[EMI green sand molding solutions](https://emi-inc.com/green-sand-molding-solutions/) ·
[EMI molding machines](https://emi-inc.com/molding-machines/)
