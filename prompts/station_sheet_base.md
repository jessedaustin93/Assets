# Station Sheet Base Prompt

Use this prompt to generate station icons for the world map layer.

```text
Create a station icon asset sheet for Agent Mesh, a lightweight RTS-style command interface for a real AI homelab.

These station icons represent real machines and nodes in the user's homelab. They should look like tactical RTS map objects, not normal desktop icons.

Style:
- dark sci-fi tactical map
- original station designs
- readable at small sizes
- cyan/blue glow accents
- purple accents for AI compute
- green/blue accents for healthy infrastructure
- yellow/red status accent areas
- no readable text, no labels, no logos
- separated icons for easy cropping
- low-end hardware friendly

Perspective:
- top-down tactical map icons or slight isometric station icons
- keep all icons consistent

Include station types:
1. AI flagship server station
2. media/infrastructure server station
3. Raspberry Pi sensor outpost
4. home automation utility node
5. Chromebook/kiosk console node
6. ESP32 recon node
7. cloud/VPS relay node
8. backup storage station

For each station type include states:
- idle
- busy
- warning
- offline
- selected

Composition:
- arrange in rows by station type
- keep each icon separated with padding
- no text inside the image
- transparent background preferred; dark neutral background acceptable
```

## Notes

After generation, crop useful icons into `sprites/stations/` and name them using `ASSET_NAMING.md`.
