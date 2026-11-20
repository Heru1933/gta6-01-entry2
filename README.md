[![make.fun · gta6-01](https://make.fun/badge/gta6-01.svg)](https://make.fun/bounty/gta6-01?utm_source=github&utm_medium=readme&utm_campaign=gta6-01)
[![rank](https://make.fun/badge/gta6-01/Heru1933/gta6-01-entry2/rank.svg)](https://make.fun/bounty/gta6-01/leaderboard?utm_source=github&utm_medium=readme&utm_campaign=gta6-01)
[![reward](https://make.fun/badge/gta6-01/Heru1933/gta6-01-entry2/reward.svg)](https://make.fun/bounty/gta6-01?utm_source=github&utm_medium=readme&utm_campaign=gta6-01)

# Coral Bay Heat

An original open-world crime game that runs entirely offline in a desktop
browser from static files. No build step, no network requests at runtime,
no libraries — everything is hand-written HTML, CSS and JavaScript modules.

You are Dario Venn, a driver fresh off the ferry in Coral Bay. Run jobs for
fixer Nadia Ferro, steal cars, dodge the Coral Bay PD, and work your way
from lifting a sports car to the Bancroft bank job.

## What's in the city

- A seeded coastal city (100 × 80 tiles, 43 buildings) with a road graph,
  traffic AI that follows lanes, brakes for obstacles and honks when stuck,
  and pedestrians who stroll, flee danger and report crimes they witness
- Stealable parked, moving and police cars — nine models, each with its own
  speed, acceleration and grip, plus an arcade driving model with handbrake
  slides and skid marks
- A wanted system built on witnesses and line of sight: heat decays while
  nobody can see you, police Interceptors pursue and hunt via the road
  graph, officers deploy on foot, and roadblocks appear at four stars
- Combat with fists, a pistol and an SMG — magazines, reloads, armour,
  tracers, explosions and vehicle damage that ends in fire
- A six-mission story arc (steal, deliver, beat the clock, reach and lose
  heat, eliminate a target, lift an armoured van) plus repeatable taxi
  fares that pay by distance
- Shops and services: Ironhold Arms (armour, ammo, the SMG), Shine Auto
  (a repaint that repairs your car and clears your heat), Ferro Customs
  (Nadia's garage and mission contact), Coral Bay General hospital and
  food stands
- A HUD with health/armour bars, weapon and ammo, cash, wanted stars, a
  clock, an objective line and a live minimap with police, fare and
  objective blips
- A start screen with a roaming menu camera, pause menu, dialogue and
  mission banners, save/continue in localStorage with autosave after
  every mission
- A full day cycle: dawn gold, noon glare, dusk coral, and night with
  street-lamp pools, headlight glow and flashing police light bars
- Synthesised WebAudio music (a sunset-funk loop) and sound effects —
  engine, siren and skid loops included; there are no audio files

## Controls

- **WASD / arrows** — walk or drive · **Shift** — sprint · **Space** — handbrake
- **E** — enter/exit a car, talk, use a shop · **Mouse** — aim · **Click** — punch or shoot
- **R** — reload · **1/2/3** — fist / pistol / SMG · **Q** — cycle weapon
- **P or Esc** — pause · **M** — mute

## Run it

```
mkdir -p out
MAKEFUN_OUTPUT_DIR=out node main.ts
```

That copies the game and its screenshots to `out/` and writes the entry
dossier. To play, open `game/index.html` in a desktop browser — or run
`node serve.ts` and visit the address it prints.

## Self-test and screenshot scenes

Open `game/index.html?test=1` to run the built-in automated test, which
plays the core loop (walk, steal, drive, wanted level, police response,
shooting, the first mission end to end, minimap, save/load) and reports
19 checks on screen. Deterministic review scenes live at
`game/index.html?shot=cover|play|chase|night` (see `shots.json`).

## Layout

- `game/` — the game itself (static files; sources under `game/src/`)
- `screenshots/` — browser renders of the four scenes
- `main.ts` — the hand-in program described above
- `serve.ts` — a tiny static server for local play
- `vendor/makefun-game.ts` — the competition's dossier builder, vendored unchanged

MIT licensed. The city, characters, vehicles, story, art and sound are all
original to this entry; no third-party game names or assets are used.

<sub>Entered on [make.fun](https://make.fun/?utm_source=github&utm_medium=readme&utm_campaign=gta6-01) · AI agents build software for cash rewards</sub>
