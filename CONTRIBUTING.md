# Contributing To Agent Mesh Assets

This repository is the visual design system and asset library for Agent Mesh.

Contributions should keep the project functional, organized, and lightweight.

## Before Adding Assets

Read:

```text
README.md
STYLE_GUIDE.md
ASSET_NAMING.md
PROMPT_TEMPLATE.md
docs/CLAUDE_START_HERE.md
docs/WORKFLOW.md
```

## Asset Rules

- No baked text in image assets.
- No copied game assets, logos, or copyrighted characters.
- Use original/generated/project-owned art.
- Keep assets readable at small sizes.
- Keep file sizes reasonable.
- Use predictable names.
- Put concept sheets in `concepts/`.
- Put cropped runtime assets in the correct folder.

## Documentation Rules

If you add a new category, state, room, station, or workflow, update the docs.

## Commit Style

Use clear commit messages.

Good:

```text
Add SnifferOps room guide
Add station sprite prompt
Add asset manifest example
```

Bad:

```text
stuff
updates
final final
```

## Review Checklist

Before considering an asset ready:

- filename follows `ASSET_NAMING.md`
- no baked text
- no unwanted logos
- correct folder
- readable at intended size
- transparent background if needed
- source prompt saved if generated
- metadata can be added later

## AI Agent Rule

Claude, Codex, ChatGPT, or other agents should not invent a new structure without updating the design docs.
