# appaday-028-pixel-quest

**Category:** G — Games and Interactive  
**Date:** 2026-06-04  
**Live URL:** https://augustineiacopelli.github.io/appaday-028-pixel-quest/

## What It Does

A full top-down overworld RPG built entirely in vanilla HTML/CSS/JS with no dependencies. Explore a 60×38 tile world map, enter castle and village sub-maps, fight enemies, grind for gold and XP, upgrade your gear, and defeat the Lich King to win.

## How to Play

- **Move:** Arrow keys (desktop) or D-pad (mobile)
- **Enter buildings:** Walk onto a castle gate (WIN tile) or village path to teleport inside
- **Shop:** Step onto a shop tile inside a village to buy weapons, armor, or potions
- **Inn:** Step onto an inn tile to restore all HP and MP for 15 gold
- **Battle:** Random encounters trigger on danger tiles (forest, cave, sky road, castle halls). Tap the dialogue box to advance text.
- **ACT before SPARE:** Most enemies need you to ACT first to unlock the SPARE option
- **Magic:** Costs 4 MP, bypasses enemy DEF — essential against the Lich King
- **Goal:** Reach Castle Darkhorn, fight through the halls, find the throne room, defeat or spare the Lich King

## World Map

| Zone | Tile | Danger |
|------|------|--------|
| Grassy Plains | Green | No |
| Dark Forest | Dark green | Yes — Slimes, Werewolves, Skeletons |
| Crystal Cave | Purple | Yes — Golems, Skeletons, Fire Imps |
| Sky Road | Dark blue | Yes — Dragons, Fire Imps |
| Dungeon | Near-black | Yes — Golems, Dark Knights |
| Castle Hall | Stone | Yes — Dark Knights, Skeletons, Werewolves |
| Village Road | Brown | No |
| Castle Gate | Gold | No (entry trigger) |

## Enemies

| # | Name | HP | Notes |
|---|------|----|-------|
| 0 | Slime | 12 | Easy starter |
| 1 | Stone Golem | 22 | Mid-tier |
| 2 | Shadow Dragon | 35 | Hard |
| 3 | Dark Knight | 30 | Castle guard |
| 4 | Lich King | 200 | Final boss — DEF 8, bypasses your armor |
| 5 | Skeleton | 16 | Cave/dungeon |
| 6 | Fire Imp | 14 | High ATK |
| 7 | Werewolf | 28 | Forest |

## Equipment Slots

One weapon, one armor, one magic tome equipped at a time. Buying a new item auto-equips it. Owned but unequipped items can be swapped free from the shop menu.

## Technical Notes

- Single-file vanilla HTML/CSS/JS — zero dependencies, no build step
- Tile maps stored as 2D JS arrays; camera follows hero via offset math
- Sub-maps (castle/village interiors) swap in via `enterInterior()` — same renderer, different tile array
- `recalcStats()` derives all combat stats from base level + equipped gear — no stacking bugs
- Random encounters: 32% chance per step on danger tiles with a 2-step cooldown
- Lich King fight: bypasses 70% of hero DEF, 200 HP, ATK 22 — requires grinding to beat

## Definition of Complete

- [x] Functional — plays start to finish without errors
- [x] Single purpose — explore, fight, upgrade, beat final boss
- [x] Mobile friendly — D-pad controls, 375px viewport compatible
- [x] Visually polished — pixel art tile rendering, per-biome battle backgrounds, HUD
- [x] Published — live GitHub Pages URL before midnight
