# Theme System

Agent Mesh should support visual themes without changing the underlying data model.

The first theme is Dark Sci-Fi RTS.

## Theme Goals

- Keep assets consistent.
- Allow future reskins.
- Keep text and live data separate from images.
- Support low-power mode.
- Avoid hardcoding colors everywhere.

## Core Theme Parts

A theme may define:

- background colors
- primary accent colors
- status colors
- panel styles
- station sprite set
- room sprite set
- agent sprite set
- effect sprite set
- UI frame set
- font choices
- motion settings

## Default Theme

```text
name: dark_sci_fi_rts
base: dark navy / charcoal
primary: cyan / blue
ai: purple
healthy: green
warning: yellow
error: red
build_heat: orange
```

## Theme Folder Idea

Later, runtime themes may use:

```text
themes/dark_sci_fi_rts/
themes/industrial_server_bay/
themes/retro_terminal/
themes/clean_ops_board/
```

This repo may store shared source assets before the app packages them into themes.

## Do Not Bake Theme Into Data

The app should not treat `T5810` as permanently tied to one image.

Instead:

```text
station:t5810_ai_flagship:idle
```

can resolve to different files depending on active theme.

## Text Rendering

Text should be controlled by the app theme:

- font
- size
- color
- shadow
- outline
- contrast

Do not bake labels into images.

## Future Theme Ideas

- Dark Sci-Fi RTS
- Imperial command table
- Industrial server room
- Retro green terminal
- Clean enterprise ops board
- Steampunk machine room
- Minimal mobile dashboard

## Theme Safety

Every theme must preserve:

- readable status
- visible alerts
- obvious controls
- accessible contrast
- low-power fallback
