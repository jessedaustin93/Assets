# Agent Mesh Asset Workflow

This workflow keeps Agent Mesh assets organized from idea to runtime use.

## 1. Start With Function

Before generating art, identify what the asset represents.

Ask:

- Is this a station, room, agent, effect, UI piece, icon, prop, or background?
- What real machine, service, task, or state does it represent?
- What states are needed now?
- Does the UI already have a placeholder for it?

## 2. Use The Correct Prompt

Use prompts from `prompts/`.

Examples:

```text
prompts/agent_sheet_base.md
prompts/station_sheet_base.md
prompts/room_sheet_base.md
prompts/ui_components_base.md
prompts/effects_sheet_base.md
```

## 3. Save Concept Sheets

Put broad generated sheets in `concepts/`.

Example:

```text
concepts/concept_agent_roles_v1.png
```

Concept sheets are not final production files.

## 4. Crop Production Assets

Crop useful pieces from concept sheets into the correct folder.

Examples:

```text
sprites/agents/agent_engineer_idle_01.png
sprites/stations/station_t5810_ai_flagship_idle_01.png
sprites/rooms/room_ai_core_busy_01.png
ui/ui_selection_ring_station_selected_01.png
```

## 5. Name Consistently

Use `ASSET_NAMING.md`.

Do not use vague names like:

```text
coolrobot.png
thing2.png
newpanel-final-final.png
```

Use meaningful names:

```text
agent_engineer_repair_01.png
ui_panel_tactical_dark_idle_01.png
```

## 6. Add Metadata Later

When the asset loader supports it, add entries to:

```text
metadata/assets.manifest.json
```

Until then, folder path and filename are enough.

## 7. Test In The App

Every production asset should be checked in the UI.

Look for:

- readable size
- good contrast
- no baked text
- correct state mapping
- good fallback behavior
- acceptable performance

## 8. Optimize

After assets are accepted:

- keep original PNG/source when useful
- export optimized runtime versions if needed
- avoid giant files for small UI pieces
- consider WebP for final runtime bundles

## 9. Document Changes

If an asset introduces a new category, state, or style rule, update the docs.

Documentation is part of the asset system.
