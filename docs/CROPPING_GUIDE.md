# Asset Cropping Guide

Generated concept sheets should be cropped into individual production assets before the app uses them.

## Goal

Turn broad concept images into clean reusable runtime pieces.

## Cropping Rules

- Crop one object per file.
- Leave a small amount of padding around the object.
- Keep transparent backgrounds when possible.
- Do not include sheet labels or guide marks.
- Do not crop baked text into production sprites.
- Keep scale consistent inside each asset family.

## Recommended Output Types

```text
PNG  - preferred for sprites with transparency
WebP - preferred for optimized runtime copies
SVG  - preferred for simple scalable UI shapes when hand-authored
```

## Agent Sprites

For agents:

- keep each role the same approximate size
- keep feet/base aligned when possible
- separate each animation frame
- use consistent frame dimensions for a given animation

Example:

```text
agent_engineer_idle_01.png
agent_engineer_idle_02.png
agent_engineer_walk_01.png
agent_engineer_walk_02.png
```

## Station Sprites

For stations:

- keep icons centered
- leave room for selection rings and labels rendered by the app
- make state variants similar in size

## Room Sprites

For rooms:

- crop whole room as background/interior
- keep room bounds consistent
- leave open space for agent placement
- crop props separately if reusable

## UI Pieces

For UI:

- keep blank space for rendered text
- preserve corner and border consistency
- crop multiple sizes if needed
- avoid including sample text from generated sheets

## Effects

For effects:

- transparent background preferred
- keep the effect centered
- preserve frame size for animation sequences
- avoid heavy glow that overwhelms content

## Quality Check

Before committing cropped assets, verify:

- file name matches `ASSET_NAMING.md`
- no unwanted text
- no weird cut-off edges
- transparent background works
- asset is readable at target size
- file size is reasonable
