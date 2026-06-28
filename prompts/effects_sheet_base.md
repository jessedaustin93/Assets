# Effects Sheet Base Prompt

Use this prompt to generate lightweight activity/status effects.

```text
Create a lightweight sci-fi RTS visual effects sheet for Agent Mesh.

Agent Mesh is a tactical command interface for a real AI homelab. Effects should represent real activity such as SSH, deploys, packet flow, warnings, scans, builds, and system load.

Style:
- sci-fi RTS command interface effects
- clean readable effects
- cyan/blue network effects
- purple AI/model effects
- orange build/heat effects
- yellow warning effects
- red critical/error effects
- no readable text, no labels, no logos
- transparent-style effects separated for cropping
- low-end hardware friendly

Include:
1. SSH beam connecting
2. SSH beam active
3. SSH beam failed
4. deploy beam transfer
5. data packet flow dots
6. radar sweep arc
7. new contact pulse
8. warning pulse
9. error pulse
10. success pulse
11. GPU core glow
12. CPU heat glow
13. storage fill indicator
14. construction/update shimmer
15. service restart pulse

Requirements:
- each effect separated with padding
- make effects reusable as overlays
- avoid huge full-screen particles
- no text inside the image
- transparent background preferred
```

## Notes

After generation, crop effects into `sprites/effects/` and name them using `ASSET_NAMING.md`.
