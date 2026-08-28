# Melting Furnace — Specialty Equipment Pass — Pass date: 2026-08-28 (revised)

Tracker line item #9 "Furnace" — currently lists "Stahl Specialty Co" under FROM/MFG. Stahl
Specialty runs permanent-mold aluminum casting plants in both Kingsville and Warrensburg, MO,
and — per the customer — has built its own furnace equipment in-house at Warrensburg for many
years. That's real aluminum furnace expertise, worth a direct conversation, but this revision
puts it alongside the rest of the field on technology terms rather than out front.

## Terminology check: "electric arc furnace" isn't the standard fit for aluminum

An electric *arc* furnace (EAF) is the steelmaking/ferrous-scrap tool — a graphite-electrode arc
struck directly through the charge. That's not how aluminum is melted commercially: aluminum's
low melting point (~660°C) and its sensitivity to hydrogen pickup and oxidative/dross loss make a
direct arc a poor fit — it burns metal and produces inconsistent quality. If "electric arc
furnace" meant "an electric, not gas-fired, melting furnace," electric resistance or induction is
almost certainly the right family — worth confirming before an RFQ goes out.

## Two independent axes of technology

**Heat source:**

| Source | How it heats | Notes |
|---|---|---|
| Gas-fired combustion | Burner + refractory radiant heat | Lower capital cost, more common where electric rates are high; more emissions/dross to manage |
| Electric resistance | Radiant resistance elements above the bath | No electromagnetic stirring, no coil-cooling loss, simple to maintain |
| Electric induction (coreless) | Coil surrounds the crucible; eddy currents heat the whole bath | Built-in stirring aids alloy homogeneity; good for melting from cold charge with frequent alloy changes |
| Electric induction (channel) | Induction field concentrated in a channel/loop within an inductor, heating metal that circulates through it | Suited to continuous holding and large-volume throughput more than melting from cold charge |
| Electric arc | Direct arc through the charge | Ferrous/steel scrap tool — not used for aluminum production melting |

**Furnace architecture** (largely independent of heat source — a reverberatory furnace can be gas
or electric):

| Architecture | How it works | Notes |
|---|---|---|
| Wet-hearth reverberatory | Charge is loaded directly into the molten bath | Simple, low cost, versatile; wet or damp charge carries steam-explosion risk |
| Dry-hearth reverberatory | Charge sits on an inclined hearth above the bath; hot exhaust gas heats it before it melts and drains in | Higher melt rate per unit hearth area than wet-hearth; keeps solid charge separated from the bath, cutting steam-explosion risk |
| Stack / shaft (tower) melter | Charge descends through a vertical shaft counter-current to exhaust gas, preheating on the way down | High thermal efficiency from waste-heat recovery; this is the architecture behind products like StrikoWestofen's StrikoMelter |
| Stationary vs. tilting | Stationary furnaces are cheaper and can hold higher capacity; tilting furnaces cost more but give controlled, low-turbulence discharge | Affects how cleanly metal comes out for whatever downstream transfer method is used |

## Vendor-by-technology

| Vendor | Architecture | Heat source | Notes |
|---|---|---|---|
| Stahl Specialty Co. (Warrensburg, MO) | In-house engineered (bottom-drop quench, heat-treat, tilt casting) | Not published | Real, decades-deep aluminum furnace expertise nearby, built for their own permanent-mold plants rather than sold commercially as a rule — worth a direct call. |
| StrikoWestofen | Shaft/stack melter (StrikoMelter), plus dosing/holding | Gas or electric | Shaft design specifically for high thermal efficiency via waste-heat preheating. |
| Dynamo Furnaces | Reverberatory, tilting (GM-J series) | Gas | Independent US builder of tilting gas reverberatory furnaces. |
| Modern Equipment Company | Reverberatory | Gas or electric resistance | Established independent US builder; public spec detail is thin — go direct for a quote. |
| The Schaefer Group (FW Schaefer) | Reverberatory / melt-hold | Electric resistance | Independent US builder, electric-only product line found this pass. |
| SECO/WARWICK | Multiple (per their aluminum scrap recycling furnace literature) | Gas or electric | International furnace group with published technical material on modern aluminum recycling furnace design — a useful independent technical reference as well as a possible vendor. |
| Ajax TOCCO Magnethermic | Coreless and channel induction | Electric induction | Explicit coreless- and channel-furnace product lines for both ferrous and non-ferrous melting. |
| Inductotherm | Coreless induction (primarily) | Electric induction | Widely cited as a dominant induction power-system supplier in North America; not independently spec-checked this pass. |

## Compatibility check for a unified system

Melt/hold rate (kg/h) is the number that ties this pass to the molding press pass: target
molds/hour × metal weight per mold sets the minimum sustained output the furnace needs to
deliver without starving the line. That number wasn't in the tracker — get it before sizing any
furnace on this list, since capacity is the single biggest cost and footprint driver.

Architecture also has a secondary effect worth flagging even without going deep into pouring
equipment (out of scope for this pass): a tilting furnace discharges more cleanly than a
stationary one, which affects how metal gets from furnace to mold regardless of which method
ends up handling that transfer.

Sources: [Electric Arc Furnace vs Induction Furnace: Efficiency Analysis](https://eureka.patsnap.com/report-electric-arc-furnace-vs-induction-furnace-efficiency-analysis) ·
[Electric arc furnace (Wikipedia)](https://en.wikipedia.org/wiki/Electric_arc_furnace) ·
[Reverberatory aluminium melting furnaces — Aluminium Guide](https://aluminium-guide.com/aluminium-melting-furnaces/) ·
[Aluminium melting: a dry hearth versus a wet bath — Aluminium Guide](https://aluminium-guide.com/aluminium-melting-dry-hearth-wet-bath/) ·
[Choosing the Right Furnace for Your Operation — Modern Casting](https://www.moderncasting.com/articles/2021/09/08/choosing-right-furnace-your-operation) ·
[Modern Furnaces for Aluminum Scrap Recycling — SECO/WARWICK](https://www.secowarwick.com/wp-content/uploads/2017/03/MODERN-FURNACES-FOR-ALUMINUM-SCRAP-RECYCLING-AP.pdf) ·
[Aluminum Tilting Reverberatory Melting Furnace GM-J Series — Dynamo Furnaces](https://dynamofurnaces.com/melting-furnaces/gas/aluminum-tilting-reverberatory-melting-furnace-gm-j-series/) ·
[How To Select The Right Aluminum Furnace — Dynamo Furnaces](https://dynamofurnaces.com/how-to-select-the-right-aluminum-furnace-for-your-casting-operation/) ·
[StrikoWestofen melting and holding furnaces](https://www.strikowestofen.com/melting-and-holding-furnaces/) ·
[Channel Induction Melting Furnaces — Ajax TOCCO](https://www.ajaxtocco.com/products/channel-melting-furnace) ·
[Coreless Induction Melting Furnaces — Ajax TOCCO](https://www.ajaxtocco.com/products/coreless-melting-furnaces) ·
[Stahl Specialty Company background](https://stahlspecialty.com/about-stahl-permanent-mold-aluminum-castings/)
