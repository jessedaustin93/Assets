# Prompts

This folder stores reusable prompts for generating Agent Mesh assets.

Prompts should follow the project style guide and should avoid copyrighted characters, direct game copies, logos, or baked text.

## Rules

- Keep prompts specific to one asset family.
- State `no baked text` clearly.
- Ask for separated assets that can be cropped.
- Mention low-end hardware readability.
- Use the same style language across prompts.
- Save the prompt beside the generated asset sheet when possible.

## Prompt Families

- `agent_sheet_base.md`
- `station_sheet_base.md`
- `room_sheet_base.md`
- `ui_components_base.md`
- `effects_sheet_base.md`
- `backgrounds_base.md`
- `icons_base.md`

## Workflow

1. Pick the correct prompt family.
2. Generate a concept sheet.
3. Save the sheet into `concepts/` or the correct asset folder.
4. Crop useful assets into production folders.
5. Name the cropped assets using `ASSET_NAMING.md`.
6. Add manifest entries when metadata support exists.
