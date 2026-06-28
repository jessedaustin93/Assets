# UI Components Base Prompt

Use this prompt to generate tactical UI/HUD assets.

```text
Create a sci-fi RTS UI component sheet for Agent Mesh.

Agent Mesh is a lightweight RTS-style command interface for a real AI homelab. The UI components should look like a tactical command HUD but remain clean, readable, and usable.

Style:
- dark tactical command HUD
- clean sci-fi panels
- cyan/blue glow accents
- low-noise readable interface
- original design, no copied game UI
- no readable text, no labels, no logos
- empty frames that the app can render live text into
- low-end hardware friendly

Include:
1. panel frames
2. button frames
3. hover/selected frames
4. station selection rings
5. room selection rings
6. agent selection rings
7. status dots
8. warning/error icons without text
9. progress bar frames
10. tooltip frames
11. command menu frame
12. alert banner frames
13. minimap frame
14. terminal window frame
15. small resource bar frames

Requirements:
- no baked labels
- leave blank centers for rendered app text
- keep elements separated for cropping
- include multiple sizes where useful
- make shapes readable on dark backgrounds

Composition:
- organized asset sheet
- separated components with padding
- transparent background preferred; dark neutral background acceptable
```

## Notes

After generation, crop useful UI pieces into `ui/` and name them using `ASSET_NAMING.md`.
