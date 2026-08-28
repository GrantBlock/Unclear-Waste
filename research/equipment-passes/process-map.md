# Process Map — Ground Truth — DWG 7332, Block Concepts LLC, 2026-06-13

Source: `ClayBailey_ProcessMap.pdf` (DWG NO. 7332, "7332 Concept Assembly — Sand Molding
Line," rev 1, 6/13/2025), supplied by the customer. This is Block Concepts' own overhead layout
and utility schedule for the 9-station sand loop — the authoritative source for footprint and
utility figures the other passes had been flagging as unknown. It does **not** yet fix mold size
or cycle rate — those fields are blank in the drawing's own station schedule, confirming that gap
is real, not just missing from the tracker.

## Station schedule (as drawn)

| # | Station | Footprint (L × W) | Air | Electrical | Flow |
|---|---|---|---|---|---|
| 1 | Sand Mixer + Hopper | 144 in × 120 in | 80 psi · 4 cfm | 480V · 3φ · 30A | Vertical |
| 2 | Incline Sand Conveyor | 216 in × 18 in | — | 480V · 3φ · 10A | Vertical |
| 3 | Horizontal Sand Conveyor | 240 in × 24 in | — | 480V · 3φ · 10A | Right → Left |
| 4 | Molding Hopper | 114 in × 112 in | 80 psi · 3 cfm | 480V · 3φ · 15A | Vertical |
| 5 | Molding Press | 240 in × 112 in | 80 psi · 8 cfm | 480V · 3φ · 60A | Left → Right |
| 6 | Transfer Conveyor | 414 in × 24 in | — | 480V · 3φ · 12A | Left → Right |
| 7 | Transfer Conveyor | 624 in × 24 in | — | 480V · 3φ · 15A | Vertical |
| 8 | Transfer Conveyor | 408 in × 24 in | — | 480V · 3φ · 12A | Right → Left |
| 9 | Sand Reclamation | 108 in × 96 in | 80 psi · 6 cfm | 480V · 3φ · 25A | Vertical |

**Utilities summary (as drawn):** Main power 480V 3φ · Control 120V 1φ · Compressed air 80 psi ·
Air consumption ~21 cfm total · 9 stations. Summing nameplate amps across all 9 stations gives
~189A at 480V 3φ — a rough upper bound for service sizing, not a demand-factored load; get an
actual demand calc once real equipment (not concept placeholders) is selected.

## Physical loop, as drawn

Station 1 (Sand Mixer + Hopper) discharges up into Station 2 (Incline Sand Conveyor), which
feeds Station 3 (Horizontal Sand Conveyor, flowing right to left) into Station 4 (Molding
Hopper), which feeds Station 5 (Molding Press, flowing left to right). Finished molds discharge
onto Station 6 (Transfer Conveyor), turn the corner into Station 7 (a long vertical transfer run
down the right side of the cell), turn again into Station 8 (Transfer Conveyor, flowing right to
left along the bottom), and finally up into Station 9 (Sand Reclamation), which returns reclaimed
sand back into Station 1 — closing the loop exactly as described in `README.md`'s system diagram.

## The one thing this drawing settles, and the one thing it doesn't

**Settles:** footprint and utility targets for the stations already in scope. Notably, Station 1
("Sand Mixer + Hopper") is drawn as a single combined station with one vertical in/out — a batch
sand mixer, not the standalone in-line feed a continuous muller (Multi-Mull, Palmer continuous)
typically wants. That's a point in favor of staying batch (see `green-sand-mulling.md`) unless
the molding press ends up needing continuous-rate throughput.

**Doesn't settle:** the furnace. It's drawn as a separate, unconnected box labeled
"FURNACE — TENTATIVE" off to the side of Station 7, with no flow arrow tying it into the loop at
all. That's the clearest confirmation yet that metal-side integration (furnace placement, and
however molten aluminum actually reaches the molds on this conveyor loop) is still an open
design question, not just an unsourced line item — see `furnace-melting.md`. It also means
whatever furnace gets chosen needs a physical tie-in point designed against this layout, most
likely somewhere along the Station 5–7 run where poured molds are moving.

## Compatibility notes tying this to the technology passes

- **Molding press envelope:** 240 in × 112 in (20 ft × 9.3 ft), 60A @ 480V 3φ, 8 cfm @ 80 psi.
  None of the vendor products compared in `molding-press.md` (DISAMATIC, DISA MATCH, Hunter
  HMP-20/HLM, Sinto FBO/FCMX, EMI/Savelli) had published footprint or utility draw in this pass —
  that's the next concrete thing to request from each vendor: does their machine fit this
  envelope, and does 60A at 480V 3φ cover it (high-pressure Seiatsu-class machines in particular
  may draw more).
- **Sand mixer + hopper:** 144 in × 120 in, 30A @ 480V 3φ, matches a Simpson Mix-Muller-class
  batch unit; confirms the batch-vs-continuous read in `green-sand-mulling.md`.
- **Sand reclamation:** 108 in × 96 in, 25A @ 480V 3φ, 6 cfm @ 80 psi — a compact footprint
  consistent with a mechanical (Pro-Claim-class) system rather than a multi-stage thermal line,
  which typically needs more floor space for the heating/cooling zones. Supports leaning
  mechanical-only per `green-sand-reclamation.md`, pending confirmation of core sand volume.
- **Furnace:** no footprint or utility budget exists yet in this drawing — it has to be added,
  not fit into leftover space, once a technology and vendor are chosen from
  `furnace-melting.md`.
