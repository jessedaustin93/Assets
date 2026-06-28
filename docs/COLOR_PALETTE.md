# Color Palette

Agent Mesh uses a dark tactical base with bright functional accents.

Colors should communicate state first and style second.

## Base Colors

Use dark neutral colors for backgrounds and large panels.

```text
near_black        #05080D
deep_navy         #07111F
charcoal          #111821
steel_dark        #1B2633
panel_dark        #0D1624
panel_border      #26384A
```

## Primary Accent Colors

```text
cyan_primary      #35D6FF
blue_glow         #2B7CFF
teal_secondary    #20F0C0
soft_blue         #7FB8FF
```

Use these for:

- selection outlines
- active links
- station rings
- normal holographic UI
- command highlights

## AI / Model Accent

```text
ai_purple         #A855FF
ai_magenta        #D946EF
model_violet      #7C3AED
```

Use for:

- AI Core
- models
- LLM jobs
- inference activity
- scientist role accents

## Status Colors

```text
healthy_green     #38E078
busy_cyan         #35D6FF
warning_yellow    #FFD447
error_red         #FF4D5E
critical_red      #FF1F3D
offline_gray      #6B7280
blocked_amber     #F59E0B
complete_green    #4ADE80
```

Status colors must be consistent across the whole app.

## Heat / Build Colors

```text
build_orange      #FF9F1C
heat_orange       #FF6B1A
compile_gold      #FBBF24
```

Use for:

- builds
- compiles
- GPU/CPU heat
- Docker deploys
- active repair work

## Background Glow Rules

Glow should be subtle.

Use glow to communicate state, not to make everything shiny.

Bad:

```text
everything glowing all the time
```

Good:

```text
selected station has cyan ring
warning room has yellow pulse
AI core has subtle purple idle glow
```

## Contrast Rules

- Text must be readable on panels.
- Warning and error must stand out immediately.
- Avoid using only color for critical meaning; combine color with icon/shape/pulse.
- Reduced-motion mode still needs clear color and shape states.

## Role Accent Ideas

```text
engineer          orange/cyan
developer         blue/cyan
scientist         purple
signal_officer    green/cyan
security_officer  red/blue
cargo_bot         yellow/orange
maintenance_bot   green/blue
recon_drone       teal/green
```

## Do Not Use

Avoid:

- white backgrounds as the main theme
- neon rainbow everywhere
- unreadable dark-on-dark panels
- red for normal activity
- yellow for healthy state
- random colors per screen
