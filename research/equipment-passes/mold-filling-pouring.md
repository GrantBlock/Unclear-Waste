# Mold Filling / Pouring — Specialty Equipment Pass — Pass date: 2026-08-28

Tracker line item #10 "Furnace Pouring Robot" — currently "None" on both FROM and TO. This is
the step between the furnace (#9) and the filled-mold conveyors (#12/#13): transferring molten
aluminum from the furnace into each poured mold, consistently and at a rate matching the molding
line's output.

## Two ways to solve this — decide before quoting

1. **Integrated dosing furnace** — a furnace with a built-in metering/dosing spout (e.g.
   StrikoWestofen Westomat) delivers a preset metal charge straight into the mold on the
   conveyor line, no separate ladling robot required. Simpler cell, one vendor, one service
   contract — but ties the pouring method to whichever furnace gets selected.
2. **Separate ladling robot** — an industrial robot arm carries a bottom-pour ladle from a
   conventional holding furnace to each mold. Works with any furnace choice, adds a second piece
   of capital equipment and a second automation vendor to integrate and maintain.

If StrikoWestofen is selected for the furnace pass (see `furnace-melting.md`), option 1 likely
eliminates this line item as separate scope — confirm with Striko whether their dosing furnace
can hit the target pour cycle time before dropping the robot from the plan.

## Vendor options (if a separate pouring robot is needed)

| Vendor | Approach | Notes | Source |
|---|---|---|---|
| StrikoWestofen (Norican Group) — Westomat ProDos | Furnace-integrated dosing, not a standalone robot | Metal drawn from below the bath surface (low dross pickup), fed directly to mold or casting machine automatically. Sister company to Simpson — see cross-cutting note in the pass README. | [strikowestofen.com](https://www.strikowestofen.com/) |
| ABB (with Rimrock or similar bottom-pour ladle) | Standard 6-axis industrial robot + custom bottom-pour ceramic ladle | Used in production at Edelbrock Foundry (2 units) alongside a Shamrock unit; bottom-pour design pulls metal from below the surface for lower dross/turbulence. Off-the-shelf robot arm, foundry-specific ladle tooling. | [ABB-7600 + Rimrock bottom pour ladle demo](https://www.youtube.com/watch?v=JR1OkA3fQQQ), [Edelbrock green sand process page](https://edelbrockfoundry.com/products-services/green-sand-aluminum-foundry-processes/) |
| Shamrock | 100 lb bottom-pour ladling robot | Also in production use at Edelbrock alongside ABB units; foundry-focused robot/ladle integrator rather than a generic robot arm supplier. | [Edelbrock green sand process page](https://edelbrockfoundry.com/products-services/green-sand-aluminum-foundry-processes/) |
| SA-Foundry | Automatic melt pouring system / dosing robot | Came up in this pass's search but wasn't cross-verified beyond its own product page — treat as a lead, not a vetted vendor. | [sa-foundry.com pouring robot](https://sa-foundry.com/product/robot-zalivshhik-avtomaticheskij-dozator-rasplava/?lang=en) |

## Recommendation for next step

Settle the furnace vendor first (see `furnace-melting.md`) — it determines whether this is even
a separate purchase. If it stays separate, ABB-with-bottom-pour-ladle is the best-precedented
option found this pass (real foundry running it at scale, standard industrial robot hardware
that's easy to get service/parts for). Get the target pour cycle time and mold weight from the
molding-press sizing (see `molding-press.md`) before requesting quotes — both determine ladle
size and cycle speed.

Sources: [Green Sand Aluminum Foundry Processes (Edelbrock)](https://edelbrockfoundry.com/products-services/green-sand-aluminum-foundry-processes/) ·
[Robotic Pouring (Carpenter Brothers)](https://www.carpenterbrothersinc.com/foundry_equipment/casting-shakeout/robotic-pouring/) ·
[ABB-7600 Robot with Rimrock Bottom Pour Ladle](https://www.youtube.com/watch?v=JR1OkA3fQQQ) ·
[StrikoWestofen](https://www.strikowestofen.com/) ·
[Melt pouring robot — SA-Foundry](https://sa-foundry.com/product/robot-zalivshhik-avtomaticheskij-dozator-rasplava/?lang=en)
