# Placeholder Sprites

This folder holds simple fallback assets used when final art is missing.

Placeholders keep Agent Mesh functional while the asset library grows.

## Required Placeholders

```text
placeholder_station.png
placeholder_room.png
placeholder_agent.png
placeholder_effect.png
placeholder_ui.png
placeholder_icon.png
placeholder_background.png
```

## Rules

- Placeholders should be ugly-simple and obvious.
- They should not pretend to be final art.
- They should clearly show missing category/state.
- They should keep the app from breaking.
- Text labels can be rendered by the app, not baked into the placeholder image.

## App Behavior

When an exact asset is missing, the app should fall back to a placeholder instead of crashing.

Recommended fallback chain:

```text
exact asset
same subject idle state
generic category state
generic category idle
placeholder category
```
