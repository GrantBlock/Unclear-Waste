# Molding Press & Furnace — Specification List — Pass date: 2026-08-30 · rev. 2026-09-02

A discovery checklist for the two biggest unsourced systems (#5/#6 Molding Press, #9 Furnace),
built the same way as the muller worksheet: real industry-typical reference ranges where they
exist, clearly flagged as **part-specific** where they don't. Cast volume, cooling cycle time,
molds/hour, alloy quality, and parts/hour aren't independent numbers — they're one linked
calculation running through both systems and the transfer-conveyor loop. Fill in Section A from
Clay & Bailey's part drawings first; everything below it derives from those numbers.

**Rev. 2026-09-02:** the target molding rate is now provided — **60 molds/hour** — from Clay &
Bailey's line spec (`Sand_specs_v2.docx`, "Batch Specifications: Current vs. New"). Sections B, F
and G below are updated to build on it. Section A (part data from the drawings) is still the
gating unknown for cast volume, melt rate, and in-mold cooling time.

## A. Part & mold info — get this from Clay & Bailey's part drawings

This is the one section nothing here can estimate — it comes from the actual parts being cast.

| Field | What it drives | Notes |
|---|---|---|
| Part(s) to be cast | Everything below | Description + CAD/drawing reference for each part number in the mix |
| Net casting weight per part [lb] | Cast volume, melt rate | = part volume [in³] × ~0.097 lb/in³ for common cast aluminum alloys |
| Cavities per mold [#] | Parts/hour | How many parts one mold produces |
| Gating & riser allowance [%] | Metal poured per mold | Sand-cast aluminum typically yields only **50–55%** — riser alone commonly accounts for ~25% of metal poured. Good riser design can push this toward 65–75%, but plan around ~50% until the pattern/gating design says otherwise. |
| Gross metal poured per mold [lb] | Furnace melt rate | = (net casting weight × cavities) ÷ yield% |

**Known from the line spec (`Sand_specs_v2.docx`), not the drawings:** total **mold weight ≈ 350 lb
per cycle** (green sand + metal — same for the current and new line), **green sand bulk density
95 lb/ft³**. So each mold carries roughly 350 lb ÷ 95 lb/ft³ ≈ **3.7 ft³ of sand** (less the metal
weight). Net casting weight per part is a fraction of the 350 lb and still needs the part drawings —
this figure only bounds it from above and sizes the sand throughput in Section B.

## B. Molding press — operational info

| Field | Typical reference | Notes |
|---|---|---|
| Molds per hour | **60/hour** (new-line target); existing line runs **12/hour** | Now provided — `Sand_specs_v2.docx` ("Throughput Rate — Molding", Current 12 → New 60, a 5× step). This is the number every other pass and DWG 7332's station schedule flagged as blank. 60/hour sits in the 50–100 band where a batch muller pairs cleanly (`green-sand-mulling.md`) — but see the sand-supply note below. |
| Parts per hour | = 60 × cavities/mold | molds/hour now fixed at 60; still needs cavities/mold from Section A |
| Mold cycle time [sec/mold] | = 3600 ÷ 60 = **60 sec/mold** (new line); existing line = 3600 ÷ 12 = **300 sec/mold** | Derived from the molds/hour above |
| Squeeze/compaction time [sec] | Varies by mechanism — see `molding-press.md` | Must fit inside the 60 sec/mold index at 60 molds/hour; jolt-squeeze and high-pressure (Seiatsu) mechanisms compact on different timescales — get this from the specific machine once one is shortlisted |
| Mold envelope | 240 × 112 in max, per DWG 7332 Station 5 | Station-5 footprint, not the mold itself; the mold carries ≈ 3.7 ft³ of sand (Section A). This is the one hard constraint already fixed — see `process-map.md` |

> **Sand supply at 60 molds/hour (from `Sand_specs_v2.docx`).** The same spec sizes the sand
> system, and the numbers do not yet close — flag for the team:
>
> - Sand through the press ≈ 60 molds/hour × ~350 lb/mold ≈ **21,000 lb/hour (~10.5 tons/hour)**
>   of green sand to mull and return (most of the 350 lb mold weight is sand).
> - The doc's stated **new muller throughput is 2,100 lb/hour** (700 lb batch ÷ 20 min cycle,
>   Current 420 → New 2,100, also a 5× step). The interim estimate for the existing Simpson "1F"
>   Mix-Muller was **1.75–3.5 tons/hour** (`green-sand-mulling.md`).
> - Both muller figures are **well below ~10.5 tons/hour.** The doc's mixer **cycle time**
>   (Current 50 min, New 20 min per batch) is also ~10× longer than a muller's actual mull cycle
>   (`green-sand-mulling.md` puts it at 3–6 min, ~90 sec floor) — cycle time is the loose variable
>   in the doc's throughput math.
> - **Action:** get the real batch size and cycle time for 1F-0113-1803 from Simpson, and confirm
>   whether a single batch Mix-Muller can feed 60 molds/hour or whether the line needs a continuous
>   muller (Multi-Mull / Palmer continuous) or a sized sand surge hopper between Station 1 and
>   Station 4. This is exactly the batch-vs-continuous question `green-sand-mulling.md` raised —
>   now with a firm 60 molds/hour to size against.
> - Also clarify what "Mold Weight 350 lb per cycle" includes (sand only, sand + metal, or
>   sand + metal + flask) — it drives the sand-throughput number above.

## C. Molding press — process info

| Field | Typical reference | Notes |
|---|---|---|
| Squeeze pressure [psi] | High-pressure/Seiatsu mechanisms run >100 psi on the mold surface | See `molding-press.md` for the mechanism comparison — pressure is a mechanism property, not independently specified |
| Mold hardness target | Set by mechanism + sand condition | No single number to target without a shortlisted machine |
| Sand compactability | 35–45% | Confirmed by the line spec (`Sand_specs_v2.docx`, "Target Compactability 35–45%"). Sand-system property shared across mulling and molding, not press-specific. Grain fineness in the same doc is AFS 50–70 GFN; `green-sand-mulling.md` recommends **AFS 70–100** for thin-wall aluminum surface finish. |

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
| Cast volume per pour [lb] | = gross metal poured per mold (Section A) | One pour typically serves one mold — still needs Section A |
| Pours per hour | = molds/hour (Section B) = **60/hour** (new line), assuming one pour per mold | molds/hour now fixed |
| Required melt rate [lb/hr] | = cast volume per pour × **60** | **This is the number that sizes the furnace** — see `furnace-melting.md` for vendor capacity ranges. Reduces to one unknown (cast volume per pour, from Section A). |
| Holding capacity [lb] | Typically sized as several minutes to an hour of pour demand, as a buffer | At 60 pours/hour a 20-min hold ≈ 20 molds' worth of metal. Buffers melt-rate/pour-rate mismatches the way a sand surge hopper buffers mulling against the press |

## G. Cast cooling cycle time — the number that ties the whole loop together

In-mold cooling/solidification time isn't just a furnace or press number — it sets how long each
mold occupies space on the transfer-conveyor loop (DWG 7332 Stations 6–8), which puts a hard cap
on achievable molds/hour independent of how fast the press or furnace can run.

| Field | Typical reference | Notes |
|---|---|---|
| Time to reach solidification-stage temp | One cited reference: ~240 sec (4 min) to cool to ~600°C after fill | This is time to *begin* solidifying, not time to a safe shakeout temperature — full cooling runs longer and depends heavily on section thickness and part mass |
| Full in-mold cooling time before shakeout | **Part-specific — no generic default.** Governed by section thickness, part mass, and sand thermal properties (roughly follows Chvorinov's-rule-style scaling: cooling time grows with the square of volume-to-surface-area ratio) | This is the number to nail down with real part geometry, ideally validated by a trial pour, before conveyor speed/length gets finalized |
| Total transfer-conveyor length available | Stations 6+7+8 = 414 + 624 + 408 = **1,446 in ≈ 120.5 ft**, per DWG 7332 | Fixed by the drawing already in hand — see `process-map.md` |
| Conveyor dwell capacity check | Molds simultaneously in transit = conveyor length ÷ mold pitch (inches of conveyor per mold, not yet set) | **With molds/hour now fixed at 60** (= 1 mold/minute), the number of molds on the transfer loop at any moment equals the in-mold cooling time in minutes. The drawn 1,446 in loop sustains 60 molds/hour only if **1,446 in ÷ mold pitch [in] ≥ cooling time [min]** — e.g. 24 in pitch → 60 min of cooling capacity, 36 in pitch → 40 min. Now a one-unknown check (mold pitch / index length) against the real cooling time from Section A or a trial pour. If cooling time exceeds that, the loop — not the press — caps output and needs extra length or an off-line cooling buffer before Station 9. |

## How to use this

1. Fill in Section A with real part data from Clay & Bailey. Everything else depends on it.
2. ~~Set a target molds/hour~~ **Done** — target molds/hour is now set at **60/hour**
   (`Sand_specs_v2.docx`); existing line is 12/hour. Sections B, F and G are updated to build
   on it, so the only remaining gate is Section A.
3. Compute required melt rate (Section F) from Section A — cast volume per pour × 60 — that's
   what sizes the furnace pass.
4. Get real in-mold cooling time for the actual parts (Section G, ideally trial-pour validated)
   and the mold pitch, then run the one-unknown dwell check against the fixed 1,446 in conveyor
   length from DWG 7332 — this determines whether the already-drawn transfer loop can sustain
   60 molds/hour, independent of press or furnace capacity.
5. Resolve the sand-supply gap flagged in Section B: get 1F-0113-1803's real batch size and
   cycle time from Simpson and confirm the muller (or a surge hopper) can feed 60 molds/hour.

Sources: `Sand_specs_v2.docx` — Clay & Bailey line spec, "Batch Specifications: Current vs. New" (molds/hour, mold weight, sand density, compactability, grain fineness, muller batch/cycle) ·
[Aluminum 319.0-F, Sand Cast — MatWeb](https://www.matweb.com/search/datasheet.aspx?matguid=a636716c00884d22b201490b0d69ee77) ·
[Aluminum Sand Castings: 319, 356 & 535 Alloys — LB Foundry](https://www.lbfoundry.com/aluminum-sand-castings.html) ·
[Learn About The Temperature of Melting Aluminum Alloys](https://precision-enterprises.com/the-temperature-of-melting-aluminum-alloys/) ·
[Optimization and empirical studies of riser design in sand casting](https://link.springer.com/article/10.1007/s12008-023-01725-7) ·
[Modern Casting — Gating And Risering: Basic Ways To Improve Casting Yield And Quality](https://www.qgdigitalpublishing.com/article/Gating+And+Risering:+Basic+Ways+To+Improve+Casting+Yield+And+Quality/3181881/524204/article.html) ·
[Aluminum Degassing Methods & Measurements — Modern Casting](https://www.moderncasting.com/articles/2015/08/15/aluminum-degassing-methods-measurements) ·
[Degassing in aluminium sand casting — Haworth Castings](https://haworthcastings.co.uk/news/degassing-in-aluminium-sand-casting/) ·
[Aluminum Sand Casting Complete Guide — Huaxiao-alloy](https://www.huaxiao-alloy.com/aluminum-sand-casting-guide.html)
