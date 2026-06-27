# Agent Mesh Asset Generation Prompt Template

Use this template when generating new Agent Mesh art so assets remain visually consistent.

## Master Prompt Template

```text
Create a game asset sheet for Agent Mesh, a lightweight RTS-style command interface for a real AI homelab.

Style: dark sci-fi tactical command UI, readable RTS game assets, space-station control room influence, clean holographic panels, modular shapes, cyan/blue primary glow, purple AI accents, yellow warning accents, red error accents.

Important rules:
- No readable text or labels baked into the image.
- Transparent or easy-to-cut background when possible.
- Assets should be modular and reusable.
- Keep silhouettes clear at small sizes.
- Avoid copyrighted characters, logos, or direct copies of existing games.
- Make it functional and readable before making it highly detailed.
- Low-end hardware friendly.

Asset request:
[DESCRIBE THE SPECIFIC ASSET FAMILY HERE]

Include:
[LIST REQUIRED ITEMS]

States:
[LIST IDLE/BUSY/WARNING/OFFLINE/SELECTED/etc]

Perspective:
[TOP-DOWN / ISOMETRIC / 3/4 / FRONT-FACING]

Output:
A clean organized asset sheet with separate assets spaced apart for cropping.
```

## Agent Sheet Prompt

```text
Create a sprite sheet of small readable sci-fi RTS crew agents for Agent Mesh.

Style: dark sci-fi tactical command interface, original characters, clear silhouettes, small game sprites, cyan/blue UI glow, role-based accents, no text, no logos.

Include these roles:
- engineer
- developer
- scientist / LLM operator
- signal officer
- security officer
- cargo bot
- maintenance bot
- recon drone

For each role include simple poses:
- idle
- walking
- typing or working
- alert/warning

Keep each sprite separated on a clean transparent or dark neutral background for easy cropping.
```

## Station Sheet Prompt

```text
Create a station icon asset sheet for Agent Mesh, a real homelab visualized as an RTS command map.

Style: dark sci-fi tactical map, original station icons, readable at small sizes, cyan/blue glow, subtle purple AI accents, no text or logos.

Include station types:
- AI flagship server
- media/infrastructure server
- raspberry pi sensor outpost
- home automation node
- kiosk console
- ESP32 recon node
- cloud relay node
- backup storage station

For each include states:
- idle
- busy
- warning
- offline
- selected

Make each station distinct and easy to crop.
```

## Room Sheet Prompt

```text
Create modular room interiors for Agent Mesh, a lightweight RTS-style AI homelab command interface.

Style: top-down or slight isometric sci-fi base rooms, dark tactical UI, modular station rooms, readable props, no text or labels.

Include rooms:
- bridge
- AI core
- engineering
- docker bay
- jellyfin theater
- vaultwarden vault
- snifferops radar room
- communications room
- storage room
- build lab

Each room should have open space for agents and obvious interactive objects like consoles, terminals, racks, doors, radar screens, crates, or server cabinets.
```

## UI Sheet Prompt

```text
Create a sci-fi RTS UI component sheet for Agent Mesh.

Style: dark tactical command HUD, clean panels, cyan/blue glow, readable low-noise interface, no text.

Include:
- panel frames
- button frames
- selection rings
- status dots
- progress bar frames
- tooltip frames
- command menu frame
- alert banner frames
- minimap frame
- terminal window frame

All components should be empty with no baked labels so the app can render live text on top.
```

## Effects Sheet Prompt

```text
Create a lightweight visual effects sheet for Agent Mesh.

Style: sci-fi RTS command interface effects, clean transparent-style assets, cyan/blue network effects, purple AI effects, orange build/heat effects, red/yellow warnings.

Include:
- SSH beam
- deploy beam
- packet flow dots
- radar sweep
- warning pulse
- success pulse
- GPU core glow
- CPU heat glow
- storage fill indicator
- construction/update effect

No text. Keep effects separated for cropping and animation.
```
