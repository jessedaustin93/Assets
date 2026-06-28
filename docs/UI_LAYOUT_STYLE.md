# UI Layout Style

Agent Mesh should look like a command interface, not a pile of panels.

The layout should make it obvious what layer the user is in and what can be controlled.

## Screen Layers

```text
World Map
Station View
Room View
Object / Tool View
Terminal / Logs View
```

Each layer should have a different visual density.

## World Map Layout

Purpose:

Show all stations and current health.

Visual rules:

- large open map
- station nodes spaced clearly
- status rings visible
- selected station has strong outline
- route/connection lines are thin and subtle
- alerts are obvious but not giant

Suggested screen areas:

```text
top: global status / title / breadcrumbs
center: world map
left: station list or filters
right: selected station detail
bottom: command/task bar
```

## Station View Layout

Purpose:

Show one host with its rooms/services.

Visual rules:

- station interior or module map fills center
- rooms arranged in clean grid or station-shape layout
- each room has status marker
- active agents appear near assigned rooms
- selected room details appear in side panel

Suggested screen areas:

```text
top: breadcrumbs and station health
center: room/module map
left: rooms/services list
right: selected room/agent details
bottom: active tasks and quick commands
```

## Room View Layout

Purpose:

Show service-specific controls and telemetry.

Visual rules:

- room art should not cover controls
- most important 3-5 metrics visible
- logs are one click away
- props should act like interactive shortcuts
- agents should not overlap buttons

Suggested screen areas:

```text
top: room title, state, breadcrumbs
center: room scene / service props
left: telemetry
right: controls / selected object
bottom: logs preview / active task bar
```

## Terminal / Logs Layout

Purpose:

Show text output clearly.

Visual rules:

- dark plain panel
- readable monospace font
- high contrast
- minimal background art
- error/warning highlighting
- copy/select text allowed

## Panel Style

Panels should be:

- dark translucent or solid
- thin cyan/blue borders
- subtle corner cuts
- readable without glow
- not overly glassy

## Button Style

Buttons should be obvious and compact.

States:

```text
idle
hover
active
selected
disabled
warning
danger
```

Danger buttons should look different and require confirmation.

## Breadcrumb Style

Always show path.

Example:

```text
World > T3610 > Docker Bay > Jellyfin Logs
```

Breadcrumbs should be clickable later.

## Mobile Layout

For phone/tablet:

- center map remains primary
- side panels become bottom sheets
- long-press opens context menu
- controls need large tap targets
- logs should open full-screen

## Clutter Rule

If everything is glowing, nothing is important.

Use visual emphasis only for selected, active, warning, or error states.
