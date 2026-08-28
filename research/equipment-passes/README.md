# Equipment Research Passes — Clay & Bailey Manufacturing (Aluminum Casting Production Line)

Companion research to `Equipment Changeover Tracking` (Clay & Bailey Manufacturing, Aluminum
Casting Production Line, dated 2026-08-27). Four passes below cover the core sand-and-metal loop
— mulling, molding, melting, and reclamation — comparing the underlying **technologies and
mechanisms** across independent manufacturers, not just naming one vendor per gap. The goal is to
work out what's actually compatible (throughput, mold-handling architecture, sand chemistry) and
sketch a coherent system before any RFQ goes out — vendor selection is a later step.

| Pass | Line item(s) on tracker | File |
|---|---|---|
| Process map (ground truth) | Overhead layout, footprints, and utility schedule for all 9 stations, from the customer's DWG 7332 | [process-map.md](process-map.md) |
| Green sand mulling | #2 Sand Mixer (already Simpson — "1F mix-muller"; primer + sizing/compatibility check) | [green-sand-mulling.md](green-sand-mulling.md) |
| Molding press | #5 Molding Hopper, #6 Molding Press (both currently "-", unsourced) | [molding-press.md](molding-press.md) |
| Melting furnace | #9 Furnace (listed "Stahl Specialty Co" — a Kingsville/Warrensburg, MO permanent-mold aluminum foundry with real in-house furnace-building experience, per the customer) | [furnace-melting.md](furnace-melting.md) |
| Mold filling / pouring | #10 Furnace Pouring Robot (currently "None") — not revised this pass; see file for prior notes | [mold-filling-pouring.md](mold-filling-pouring.md) |
| Green sand reclamation | #16 Sand reclamation, #17 Reclaimed Sand Elevator (already Simpson; primer + method/compatibility check) | [green-sand-reclamation.md](green-sand-reclamation.md) |

**How the four passes tie together:** target mold size and molds/hour is the number everything
else is downstream of. It sets whether the molding press needs batch or continuous sand supply
(mulling pass), whether it needs flaskless or tight-flask mold handling (molding press pass), and
what melt/hold rate the furnace needs to sustain (furnace pass) — while reclamation has to hand
sand back to mulling at a workable temperature and moisture regardless of which method is chosen
(reclamation pass). Fix mold size/rate before evaluating vendors on any of the four.

**One factual note, not a recommendation:** Simpson (already supplying #2, #16, #17) was acquired
by Norican Group in 2022, whose other foundry brands include DISA (molding machines) and
StrikoWestofen (melting/dosing furnaces). That's real information — a common parent can simplify
commissioning and service — but it's one data point among several vendors per technology in the
tables below, not the basis for narrowing the field before the technology comparison is done.

**Not yet researched (open for a future pass):** #7/#8/#12/#13 mold transfer conveyors (gravity
roller — likely fine as a commodity buy, low research value), #11 Chiller Conveyor, #15 Part
Picking Robotics. Flag if you want these picked up next.
