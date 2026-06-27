# Agent Mesh Visual Style Guide

## Style Target

Agent Mesh should feel like a lightweight RTS command interface for a real AI-powered homelab.

The goal is a readable, functional interface first, with a sci-fi tactical layer added on top.

## Core Visual Keywords

- RTS command map
- Space station control room
- Tactical holographic interface
- Modular base interior
- Dark sci-fi UI
- Clear status language
- Functional, not decorative
- Lightweight enough for old hardware

## Perspective

Use consistent perspective within each asset family.

Preferred options:

1. Top-down tactical map for world/station navigation.
2. Isometric or top-down room tiles for service rooms.
3. Simple front-facing or 3/4 sprites for agents.

Do not mix random perspectives inside the same screen unless the app intentionally separates map view from room view.

## Color Direction

Base colors:

- Dark navy
- Charcoal black
- Deep steel gray
- Desaturated blue

Primary glow:

- Cyan
- Blue
- Soft teal

Status colors:

- Green: healthy, complete, available
- Yellow: busy, warning, attention
- Red: error, failed, offline, danger
- Purple: AI/model activity
- Orange: compile/build/heat/load

Use glow sparingly. Readability beats brightness.

## Text Rule

Do not bake labels, titles, percentages, machine names, or button text into image assets.

All text should be rendered by the application using HTML/CSS/canvas/SVG. This keeps assets reusable across machines, themes, and languages.

## Shape Language

Stations:
- Large readable silhouettes
- Circular or hex tactical markers
- Clear status ring space

Rooms:
- Modular rectangles or connected tiles
- Distinct silhouettes by function
- Open center area for agents
- Clear interaction hotspots

Agents:
- Simple recognizable role silhouettes
- Color accents identify role
- Animation states should be readable at small sizes

UI:
- Panels should be clean and low-noise
- Borders can glow but should not overpower content
- Buttons should be obvious and easy to click

## Detail Level

Use more detail in concept art and less detail in production sprites.

Production assets should remain clear when scaled down.

Good:
- Bold silhouette
- Clear icon shape
- Few strong details
- Transparent background

Bad:
- Tiny unreadable details
- Text in the image
- Excessive glow
- Complex textures that blur when scaled

## Performance Rules

Agent Mesh should run on low-end hardware.

- Prefer small sprite sheets.
- Avoid huge full-screen animated images.
- Use CSS/SVG for simple UI shapes when possible.
- Use PNG/WebP for sprites and effects.
- Keep animation frame counts reasonable.
- Reuse assets through tinting and overlays.

## Theme Variants

The first theme should be Dark Sci-Fi RTS.

Future compatible themes may include:

- Imperial tactical command
- Industrial server-bay
- Steampunk factory
- Retro terminal grid
- Clean enterprise ops board

Themes should not require changing the underlying data model.
