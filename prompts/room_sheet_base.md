# Room Sheet Base Prompt

Use this prompt to generate modular room interiors.

```text
Create a modular room interior asset sheet for Agent Mesh, a lightweight RTS-style command interface for a real AI homelab.

Each room represents a real service, project, or control area. The rooms should look interesting like RTS base interiors, but they must stay readable and functional.

Style:
- dark sci-fi tactical base interior
- modular station rooms
- original design, no copyrighted game copying
- cyan/blue holographic UI glow
- purple AI accents where appropriate
- yellow/red warning accent areas
- readable props and interaction points
- no readable text, no labels, no logos
- separated rooms for easy cropping
- low-end hardware friendly

Perspective:
- top-down or slight isometric
- keep perspective consistent across all rooms

Include these rooms:
1. Bridge / command overview
2. AI Core with GPU/model reactor
3. Engineering with terminals and repair bench
4. Docker Bay with container racks
5. Jellyfin Theater with media screen and shelves
6. ARR Cargo Office with crates/download dock
7. Vaultwarden Vault with vault door and lock console
8. SnifferOps Radar Room with radar screen and signal consoles
9. Communications Room with network map/SSH/VPN consoles
10. Storage Room with drive racks and backup crates
11. Build Lab with compile/test workbench

Room requirements:
- leave open space for agent sprites
- include obvious clickable objects such as terminals, consoles, racks, doors, screens, crates, antennas, or server cabinets
- avoid baked text
- avoid busy clutter
- make each room visually distinct

Composition:
- arrange rooms in a clean grid
- keep each room separated with padding
- transparent background preferred; dark neutral background acceptable
```

## Notes

After generation, crop useful rooms into `sprites/rooms/` and name them using `ASSET_NAMING.md`.
