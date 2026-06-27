# Agent Mesh Assets

This repository is the canonical visual design system, asset library, and prompt library for Agent Mesh.

Agent Mesh is an RTS-style command interface for a real homelab and AI-agent ecosystem. The visuals should be interesting like a strategy game, but every major object should represent something real: a machine, service, task, agent, connection, alert, or terminal session.

## Core Rule

Make it work first. Make it pretty second.

The assets in this repo should support a functional UI before they become polished game art.

## Design Philosophy

- RTS command interface, not a static dashboard.
- Every station, room, unit, and effect should map to real infrastructure or real work.
- Agents move because tasks are running, not just because animations look cool.
- Drill-down navigation should feel like zooming through a strategy map.
- Text should be rendered by the app, not baked into images.
- Assets should be modular, reusable, and lightweight enough to run on low-end hardware.

## Visual Inspiration

This project takes loose inspiration from RTS and tactical interfaces: galactic maps, base interiors, command bridges, unit selection, status bars, alerts, and mission panels. The goal is not to copy any existing game. The goal is to build an original visual language for a working AI operating system.

## Current Folder Structure

```text
concepts/       Concept art, asset sheets, mockups, moodboards
sprites/        Agents, stations, rooms, drones, props, effects
ui/             Buttons, panels, icons, status bars, HUD pieces
backgrounds/    Maps, grids, space fields, room backdrops
prompts/        Reusable prompts and style references
```

## Recommended Working Folders

```text
docs/           Design bible and implementation notes
concepts/       Broad visual exploration
sprites/agents/ Character and bot sprites
sprites/stations/ Machine and node sprites
sprites/rooms/ Service-room interiors
sprites/effects/ Deploy, SSH, packet, alert, and status effects
ui/panels/      HUD panels and command windows
ui/icons/       Service and status icons
prompts/        Generation prompts and prompt templates
```

## Asset Rules

1. No baked text in art.
2. Keep perspective consistent inside each asset family.
3. Prefer transparent PNGs for sprites and UI pieces.
4. Keep source prompts beside generated assets when possible.
5. Use predictable file names.
6. Generate in sheets when exploring, then crop into individual production assets later.
7. Performance matters: simple readable assets beat huge over-detailed assets.

## Primary Documents

- `ROADMAP.md` - Development phases and priorities.
- `STYLE_GUIDE.md` - Visual style rules.
- `WORLD_LAYOUT.md` - Drill-down hierarchy.
- `STATIONS.md` - Host/machine visual mapping.
- `ROOMS.md` - Service-room concepts.
- `AGENTS.md` - Crew roles and behaviors.
- `UI_COMPONENTS.md` - HUD and control components.
- `EFFECTS.md` - Visual effects library.
- `ANIMATION_GUIDE.md` - Animation states and rules.
- `PROMPT_TEMPLATE.md` - Reusable asset generation prompt.
- `ASSET_NAMING.md` - File naming conventions.
- `TODO.md` - Current task list.
