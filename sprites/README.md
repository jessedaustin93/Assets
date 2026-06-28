# Sprites

This folder contains visual pieces used by Agent Mesh.

Sprites should be cropped from concept sheets, named consistently, and organized by role.

## Subfolders

```text
agents/       Crew, bot, drone, and worker sprites
stations/     World-map machine and node sprites
rooms/        Service-room and station-interior sprites
effects/      Activity, alert, deploy, packet, scan, and status effects
props/        Consoles, crates, racks, antennas, terminals, doors
placeholders/ Generic fallback sprites
```

## Rules

- Prefer transparent PNG for individual sprites.
- Keep assets readable at small sizes.
- Do not bake text into sprites.
- Use names from `ASSET_NAMING.md`.
- Keep concept sheets in `concepts/`.
- Keep cropped usable pieces here.

## Meaning

Every sprite should represent a real object or state in Agent Mesh.

Examples:

- station sprite = real host or machine
- room sprite = real service or project area
- agent sprite = AI helper, automation, or task worker
- effect sprite = real activity or alert
