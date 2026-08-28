# Green Sand Reclamation — Specialty Equipment Pass — Pass date: 2026-08-28 (revised)

Tracker line items #16 "Sand reclamation" and #17 "Reclaimed Sand Elevator" — both already
sourced to Simpson. As with the mulling pass, this revision lays out the underlying reclamation
technologies and independent vendors for each, rather than treating this as settled just because
a vendor is already on file.

## What reclamation is solving

After shakeout, spent green sand still has good silica in it but is loaded with spent bentonite,
sea coal, and fines from the poured mold. Reclamation strips that off so the sand can go back
into the mulling loop instead of being landfilled — this sits on the same closed loop as
mulling, so the two passes are directly linked.

## Three methods, different mechanisms

| Method | Mechanism | Typical process chain | Cost/complexity | Best fit |
|---|---|---|---|---|
| Mechanical (attrition / pneumatic scrubbing) | Sand grains are scrubbed against each other or a surface to strip the spent binder coating off each grain | Shakeout deck → attrition mill → elevator → surge hopper → magnetic separator → screener → classifier (cooling optional) → transport → storage silo → dust collector | Lowest cost and energy of the three | Straight green sand, where contamination is mostly spent bentonite/sea coal rather than heavy organic binder |
| Thermal | Burns off organic/binder material in a heating zone (fluidized bed or rotary drum), then cools the sand | Surge hopper → magnetic separator → metered feed → heating zone → cooling zone → transport → storage silo → high-temp dust collector | Highest cost and energy | Chemically-bonded (no-bake/core) sand, or green sand runs with significant core sand mixed into the reclaim stream |
| Wet | Water-based washing removes organics and contaminants | Less standardized — process varies by system | Moderate-to-high, plus water handling/treatment | More common where regulatory drivers (heavy-metal or organic contaminant limits) require it than as a default choice; more established in European practice than US foundries per the case studies found |

Mechanical and thermal are also commonly combined — mechanical stages bracketing a thermal step —
to balance sand quality against operating cost.

## Vendor-by-technology

| Vendor | Method | Product | Notes |
|---|---|---|---|
| Simpson | Mechanical (pneumatic scrubbing) | Pro-Claim | Already the vendor on file for #16/#17; positioned by Simpson as sufficient for most green sand reclamation without a thermal stage. |
| General Kinematics | Mechanical (vibratory attrition) | VIBRA-MILL (vibratory batch reclaimer), DUCTA-CLAIM (rotary reclaimer) | Independent US manufacturer; VIBRA-MILL is specifically described as reducing lumps to below 20 mesh while preserving original grain size distribution. |
| Palmer Manufacturing & Supply | Thermal | Named as a thermal reclamation system provider in industry coverage | Independent US alternative for the thermal side of the comparison; get direct specs before treating as a fit. |

## Compatibility check for a unified system

- **Ties to mulling:** reclaimed sand has to re-enter the mulling loop at a workable temperature
  and moisture level. A thermal system's hot discharge needs a cooling stage (most thermal process
  chains already include one) before it reaches the muller — check that the muller's water-addition
  control is tuned to accept reclaimed sand at whatever temperature it actually arrives at, not
  just the design spec.
- **Mechanical-only vs. mechanical+thermal** hinges on whether cores (chemically bonded, not green
  sand) will be mixed into the shakeout/reclaim stream. Core-light green sand lines are typically
  well served by mechanical-only reclamation (Pro-Claim, VIBRA-MILL, or similar); a line running
  meaningful core volume should keep thermal capacity in the conversation.
- **Confirm what's actually on order for #16** — Pro-Claim mechanical-only, or something with a
  thermal stage — since that also determines what #17's elevator needs to interface with (a
  single mechanical discharge vs. a multi-stage system's output).

Sources: [Reclaiming Sand is a Process, and a Goal — Simpson](https://www.foundrymag.com/molds-cores/article/55277951/reclaiming-sand-is-a-process-and-a-goal-simpson-technologies) ·
[Pro-Claim Sand Reclamation System — Simpson](https://www.simpsongroup.com/equipment/sand-reclamation/pro-claim/) ·
[Sand Handling, Cooling, and Reclamation — General Kinematics](https://www.generalkinematics.com/product-category/foundry-and-metalcasting-solutions/sand-systems-reclamation/) ·
[Sand Reclamation: VIBRA-MILL Vibratory Batch Sand Reclamation — General Kinematics](https://www.generalkinematics.com/blog/sand-reclamation-vibra-mill-vibratory-batch-sand-reclamation/) ·
[Sand Attrition Equipment — General Kinematics](https://www.generalkinematics.com/product-category/foundry-and-metalcasting-solutions/sand-systems-reclamation/sand-attrition/) ·
[Advances in Sand Reclamation — Foundry Mgmt & Tech](https://www.foundrymag.com/molds-cores/article/21154386/advances-in-sand-reclamation) ·
[Mechanical and thermal methods for reclamation of waste foundry sand — ScienceDirect](https://www.sciencedirect.com/science/article/abs/pii/S030147972031553X) ·
[Wet regeneration treatment for the reclamation of waste foundry sands: a case study](https://www.researchgate.net/publication/282668320_Wet_regeneration_treatment_for_the_reclamation_of_waste_foundry_sands_A_case_study)
