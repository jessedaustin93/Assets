# Appearance Direction

Agent Mesh should look like a functional RTS command interface for a real homelab.

The appearance should be interesting enough to feel like a game command center, but readable enough to use every day.

## Core Look

```text
Dark sci-fi RTS command map
Industrial server-room station interiors
Holographic tactical UI overlays
Readable low-noise dashboard controls
```

## Main Rule

Looks should support control.

Do not add decoration that hides status, buttons, logs, labels, or warnings.

## Visual Personality

Agent Mesh should feel like:

- a strategy-game command layer
- a homelab control room
- a sci-fi station map
- a network operations board
- an AI agent command surface

It should not feel like:

- a generic business dashboard
- a random cyberpunk wallpaper
- a fake game with no real data
- a cluttered terminal skin
- a copied Star Wars/Command & Conquer/Stellaris UI

## First Theme

Theme name:

```text
dark_sci_fi_rts
```

Style words:

```text
dark
clean
holographic
tactical
industrial
modular
readable
functional
low-noise
```

## Layout Feel

World map:

- tactical star/network map
- station nodes
- status rings
- route/connection lines
- alert markers

Station view:

- top-down or slight-isometric station interior
- rooms arranged like modules
- visible agents only when assigned
- room states obvious from glow/outline/status marker

Room view:

- service-specific control room
- a few readable props
- open space for agents
- logs and controls near edges/panels

Terminal/log view:

- dark clean panel
- readable monospace text
- no heavy background noise behind logs

## Detail Level

Use medium detail.

Too simple looks boring. Too detailed becomes unreadable.

Target:

- readable at a glance
- looks good on desktop
- still usable on phone or low-res screen
- assets crop cleanly
- reduced-motion mode still makes sense

## Motion Feel

Motion should be purposeful.

Good motion:

- agent walks to a task
- connection beam appears when SSH opens
- radar sweeps during scan
- warning pulses during real warning
- success pulse after completed task

Bad motion:

- random flashing
- fake busy loops
- particles everywhere
- idle agents wandering for no reason

## Visual Priority

1. Critical alerts
2. Selected object
3. Active task
4. Health/state
5. Navigation path
6. Decorative atmosphere

Decoration always loses to status and controls.
