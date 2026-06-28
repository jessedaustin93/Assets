# Lighting Guide

Lighting in Agent Mesh should communicate status and focus.

Glow is useful, but only when it means something.

## Lighting Goals

- Make selected objects obvious.
- Make warnings/errors impossible to miss.
- Give AI/model areas a distinct feel.
- Keep logs and controls readable.
- Support low-power mode.

## Base Lighting

Default scene lighting should be dark, calm, and low-contrast.

Use:

```text
soft panel edge light
subtle grid glow
small status lights
low-intensity room ambience
```

Avoid:

```text
bright full-screen bloom
rainbow glows everywhere
constant flashing
busy animated backgrounds
```

## Status Lighting

Status lighting must match the standard palette.

```text
healthy   green or calm cyan
busy      cyan/blue pulse
warning   yellow/amber pulse
error     red pulse/ring
critical  stronger red, limited use
offline   dim gray / darkened object
AI        purple/violet glow
build     orange/gold activity glow
```

## Room Lighting

Each room can have a signature accent, but the state color wins.

Examples:

```text
AI Core: purple idle glow, orange heat when busy
Docker Bay: blue/cyan idle, orange deploy activity
Jellyfin Theater: blue/green idle, purple/orange transcode activity
Vaultwarden Vault: blue/green locked idle, yellow warning, red security error
SnifferOps Radar: green/cyan sweep, yellow unknown contact, red alert contact
```

## Selection Lighting

Selection should usually be an overlay:

```text
cyan ring
blue outline
small corner brackets
subtle pulse
```

Selection should not hide warning or error states.

Priority:

```text
critical/error > warning > selected > busy > idle
```

## Agent Lighting

Agents should have small role accents, not huge glows.

Examples:

```text
engineer: orange/cyan tool light
developer: blue/cyan terminal glow
scientist: purple model glow
signal officer: green/cyan radar glow
security officer: blue/red lock light
cargo bot: yellow/orange cargo light
```

## Effect Lighting

Effects should be overlays and short-lived unless tied to an active state.

Good:

- SSH beam while connection is active
- radar sweep while scanning
- warning pulse while warning exists
- success pulse after completion

Bad:

- permanent random sparks
- effects with no data/state source
- lighting that covers controls

## Low-Power Mode

Low-power mode should:

- disable animated glow loops
- replace pulses with static outlines
- reduce bloom/shadow effects
- keep status colors visible
- keep alert icons visible

## Design Rule

If the app is unreadable without glow, the design is too dependent on glow.

Every important state needs shape, icon, or layout support in addition to color and lighting.
