# Molding Press & Furnace — Specification List — Pass date: 2026-08-30

A discovery checklist for the two biggest unsourced systems (#5/#6 Molding Press, #9 Furnace),
built the same way as the muller worksheet: real industry-typical reference ranges where they
exist, clearly flagged as **part-specific** where they don't. Cast volume, cooling cycle time,
molds/hour, alloy quality, and parts/hour aren't independent numbers — they're one linked
calculation running through both systems and the transfer-conveyor loop. Fill in Section A from
Clay & Bailey's part drawings first; everything below it derives from those numbers.

## A. Part & mold info — get this from Clay & Bailey's part drawings

This is the one section nothing here can estimate — it comes from the actual parts being cast.

| Field | What it drives | Notes |
|---|---|---|
| Part(s) to be cast | Everything below | Description + CAD/drawing reference for each part number in the mix |
| Net casting weight per part [lb] | Cast volume, melt rate | = part volume [in³] × ~0.097 lb/in³ for common cast aluminum alloys |
| Cavities per mold [#] | Parts/hour | How many parts one mold produces |
| Gating & riser allowance [%] | Metal poured per mold | Sand-cast aluminum typically yields only **50–55%** — riser alone commonly accounts for ~25% of metal poured. Good riser design can push this toward 65–75%, but plan around ~50% until the pattern/gating design says otherwise. |
| Gross metal poured per mold [lb] | Furnace melt rate | = (net casting weight × cavities) ÷ yield% |

## B. Molding press — operational info

| Field | Typical reference | Notes |
|---|---|---|
| Molds per hour | No default — set by target output, not the machine | This is the number every other pass has been flagging as blank in the tracker and in DWG 7332's own station schedule. It's not derivable from anywhere except a production target Clay & Bailey sets. |
| Parts per hour | = molds/hour × cavities/mold | Direct multiplication once both are known |
| Mold cycle time [sec/mold] | = 3600 ÷ molds/hour | |
| Squeeze/compaction time [sec] | Varies by mechanism — see `molding-press.md` | Jolt-squeeze and high-pressure (Seiatsu) mechanisms compact on different timescales; get this from the specific machine once one is shortlisted |
| Mold envelope | 240 × 112 in max, per DWG 7332 Station 5 | This is the one hard constraint already fixed — see `process-map.md` |

## C. Molding press — process info

| Field | Typical reference | Notes |
|---|---|---|
| Squeeze pressure [psi] | High-pressure/Seiatsu mechanisms run >100 psi on the mold surface | See `molding-press.md` for the mechanism comparison — pressure is a mechanism property, not independently specified |
| Mold hardness target | Set by mechanism + sand condition | No single number to target without a shortlisted machine |
| Sand compactability | 35–45% | Same target as the mulling pass — this is a sand-system property shared across mulling and molding, not press-specific |

## D. Furnace — charge & composition info

| Field | Typical reference | Notes |
|---|---|---|
| Alloy designation | Common sand-cast aluminum grades: **356/A356, 319, 355, 535** | Get this from Clay & Bailey/the part spec — alloy choice depends on the part's mechanical and corrosion requirements, not the equipment |
| Chemistry spec / cert requirement | Typically to ASTM B26 or a customer-specified chemistry | Confirms what the furnace and any in-house lab need to verify per heat |
| Charge mix | % new ingot vs. % in-house returns (gates/risers/scrap re-melted) | At ~50% casting yield, roughly half the metal poured comes back as returns — the furnace needs charge capacity for a returns-heavy mix, not just ingot |

## E. Furnace — melt quality info

| Field | Typical reference | Notes |
|---|---|---|
| Pour temperature | **1300–1450°F**, ~1382°F (750°C) commonly cited as a working target | Varies by alloy and section thickness — thinner-wall parts generally want the higher end for fill |
| Hydrogen level | <0.10 ml/100g-Al is the generally cited unacceptable threshold; **~0.07 ml/100g** is a commonly cited optimum after degassing | High hydrogen shows up as gas porosity, reduced fluidity, and poor mechanical properties — this is a real spec to hold the furnace/degassing setup to, not just a nice-to-have |
| Degassing method | Rotary (nitrogen/argon) is standard practice; lance or tablet degassing are lower-cost alternatives | Ties directly to furnace selection — some furnace/dosing packages (e.g., StrikoWestofen's line) integrate degassing, others need a separate station |
| Grain refinement / modification | Ti-B rod for grain refinement; Sr modification for Si-bearing alloys (356/319-class) | Standard practice for these alloy families — confirm against the specific alloy chosen |
| Melt cleanliness | Flux practice + filtration (ceramic foam filter is standard) at the pour point | Affects inclusion content in the casting, independent of furnace technology |

## F. Furnace — operational info

| Field | How to get it | Notes |
|---|---|---|
| Cast volume per pour [lb] | = gross metal poured per mold (Section A) | One pour typically serves one mold |
| Pours per hour | = molds/hour (Section B), assuming one pour per mold | |
| Required melt rate [lb/hr] | = cast volume per pour × pours/hour | **This is the number that sizes the furnace** — see `furnace-melting.md` for vendor capacity ranges to check it against |
| Holding capacity [lb] | Typically sized as several minutes to an hour of pour demand, as a buffer | Buffers against melt-rate/pour-rate mismatches the way a sand surge hopper buffers mulling against the press |

## G. Cast cooling cycle time — the number that ties the whole loop together

In-mold cooling/solidification time isn't just a furnace or press number — it sets how long each
mold occupies space on the transfer-conveyor loop (DWG 7332 Stations 6–8), which puts a hard cap
on achievable molds/hour independent of how fast the press or furnace can run.

| Field | Typical reference | Notes |
|---|---|---|
| Time to reach solidification-stage temp | One cited reference: ~240 sec (4 min) to cool to ~600°C after fill | This is time to *begin* solidifying, not time to a safe shakeout temperature — full cooling runs longer and depends heavily on section thickness and part mass |
| Full in-mold cooling time before shakeout | **Part-specific — no generic default.** Governed by section thickness, part mass, and sand thermal properties (roughly follows Chvorinov's-rule-style scaling: cooling time grows with the square of volume-to-surface-area ratio) | This is the number to nail down with real part geometry, ideally validated by a trial pour, before conveyor speed/length gets finalized |
| Total transfer-conveyor length available | Stations 6+7+8 = 414 + 624 + 408 = **1,446 in ≈ 120.5 ft**, per DWG 7332 | Fixed by the drawing already in hand — see `process-map.md` |
| Conveyor dwell capacity check | Molds simultaneously in transit = conveyor length ÷ mold pitch (inches of conveyor per mold, not yet set) | Once cooling time and mold pitch are known: max sustainable molds/hour = (conveyor length ÷ mold pitch) ÷ (cooling time in hours). If that's lower than the press's rated molds/hour, the conveyor loop — not the press — is the bottleneck. |

## How to use this

1. Fill in Section A with real part data from Clay & Bailey. Everything else depends on it.
2. Set a target molds/hour (Section B) — this is a business decision (target output), not
   something equipment specs can derive.
3. Compute required melt rate (Section F) from the result — that's what sizes the furnace pass.
4. Get real in-mold cooling time for the actual parts (Section G, ideally trial-pour validated)
   and check it against the fixed conveyor length from DWG 7332 — this determines whether the
   already-drawn transfer loop can actually sustain the target molds/hour, independent of press
   or furnace capacity.

Sources: [Aluminum 319.0-F, Sand Cast — MatWeb](https://www.matweb.com/search/datasheet.aspx?matguid=a636716c00884d22b201490b0d69ee77) ·
[Aluminum Sand Castings: 319, 356 & 535 Alloys — LB Foundry](https://www.lbfoundry.com/aluminum-sand-castings.html) ·
[Learn About The Temperature of Melting Aluminum Alloys](https://precision-enterprises.com/the-temperature-of-melting-aluminum-alloys/) ·
[Optimization and empirical studies of riser design in sand casting](https://link.springer.com/article/10.1007/s12008-023-01725-7) ·
[Modern Casting — Gating And Risering: Basic Ways To Improve Casting Yield And Quality](https://www.qgdigitalpublishing.com/article/Gating+And+Risering:+Basic+Ways+To+Improve+Casting+Yield+And+Quality/3181881/524204/article.html) ·
[Aluminum Degassing Methods & Measurements — Modern Casting](https://www.moderncasting.com/articles/2015/08/15/aluminum-degassing-methods-measurements) ·
[Degassing in aluminium sand casting — Haworth Castings](https://haworthcastings.co.uk/news/degassing-in-aluminium-sand-casting/) ·
[Aluminum Sand Casting Complete Guide — Huaxiao-alloy](https://www.huaxiao-alloy.com/aluminum-sand-casting-guide.html)
