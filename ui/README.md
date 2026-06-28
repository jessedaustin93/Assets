# UI

This folder holds reusable interface pieces for the Agent Mesh command surface.

UI assets should support a clean RTS-style control experience without hardcoding text into images.

## Suggested Subfolders

```text
panels/
buttons/
icons/
status/
selection/
menus/
tooltips/
terminals/
```

## UI Asset Rules

- No baked labels or percentages.
- Keep centers blank for app-rendered text.
- Use consistent border thickness.
- Keep hover and selected states readable.
- Prefer CSS/SVG for simple shapes when practical.
- Use PNG/WebP assets for complex frames and effects.

## Naming Examples

```text
ui_panel_tactical_dark_idle_01.png
ui_button_primary_hover_01.png
ui_selection_ring_station_selected_01.png
ui_status_dot_warning_01.png
ui_terminal_frame_dark_idle_01.png
```
