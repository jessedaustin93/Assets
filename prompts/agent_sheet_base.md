# Agent Sheet Base Prompt

Use this prompt to generate the first production-style agent/crew sprite sheet.

```text
Create a clean sprite sheet of original small sci-fi RTS crew agents for Agent Mesh.

Agent Mesh is a lightweight RTS-style command interface for a real AI homelab. The agents represent real AI helpers, automations, scripts, and task workers.

Style:
- dark sci-fi tactical command interface
- readable small game sprites
- original characters, no copyrighted designs
- clear silhouettes
- cyan/blue base lighting
- role-based accent colors
- low-end hardware friendly
- separated sprites for easy cropping
- no readable text, no labels, no logos

Perspective:
- small top-down, slight isometric, or clean 3/4 tactical sprites
- keep perspective consistent across all agents

Include these roles:
1. engineer - Linux/Docker/server repair
2. developer - coding/Git/tests
3. scientist / LLM operator - model/research/prompt tasks
4. signal officer - SnifferOps/radio/BLE/Wi-Fi analysis
5. security officer - vault/firewall/VPN/secrets
6. cargo bot - media/download/file movement
7. maintenance bot - health checks and cleanup
8. recon drone - sensor/ESP32/field data node

For each role include poses:
- idle
- walking
- typing or working
- alert/warning

Composition:
- arrange in rows by role
- keep each sprite separated with padding
- avoid complex backgrounds
- transparent background preferred; dark neutral background acceptable
- no text inside the image
```

## Notes

After generation, crop useful sprites into `sprites/agents/` and name them using `ASSET_NAMING.md`.
