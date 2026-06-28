# Claude Start Here

This file is the handoff guide for Claude, Codex, ChatGPT, or any other agent working on Agent Mesh assets.

## First Rule

Read the docs before changing structure.

Do not invent a new asset layout unless the existing docs are wrong and you update them intentionally.

## Required Reading Order

1. `README.md`
2. `ROADMAP.md`
3. `STYLE_GUIDE.md`
4. `WORLD_LAYOUT.md`
5. `STATIONS.md`
6. `ROOMS.md`
7. `AGENTS.md`
8. `UI_COMPONENTS.md`
9. `EFFECTS.md`
10. `ANIMATION_GUIDE.md`
11. `PROMPT_TEMPLATE.md`
12. `ASSET_NAMING.md`
13. `TODO.md`

## Project Goal

Agent Mesh is an RTS-style command interface for a real homelab and AI-agent ecosystem.

It should look interesting like a strategy game, but it must actually control and represent real systems.

## Non-Negotiables

- Function before polish.
- No baked text in image assets.
- Every station, room, agent, and effect should map to real infrastructure or real work.
- Keep the UI lightweight enough to run on low-end hardware.
- Keep placeholders working before adding final art.
- Do not copy copyrighted game assets.
- Keep the structure predictable for scripts and future agents.

## Asset Loading Target

Build the app so assets can be loaded by:

```text
category / subject / state / variant
```

Examples:

```text
station / t5810_ai_flagship / idle / 01
room / ai_core / busy / 01
agent / engineer / repair / 01
effect / ssh_beam / active / 01
ui / selection_ring / station_selected / 01
```

## Development Order

1. Keep current UI functional.
2. Add asset manifest support.
3. Add placeholder fallback system.
4. Add station and room asset categories.
5. Add agent sprite categories.
6. Add effects and UI pieces.
7. Add animation states.
8. Add reduced-motion and potato mode.
9. Polish theme.

## When Unsure

Choose the simplest readable asset and document the decision.
