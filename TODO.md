# Agent Mesh Assets TODO

This list tracks near-term asset and documentation work.

## Live in app (2026-06-27)

Functional UI shipped ahead of polished art (per "make it work first"):

- [x] World map with real machine stations (keyed by agent-id suffix)
- [x] Station drill-down → rooms; nested rooms (Arr Stack, Downloads → programs)
- [x] Real service liveness telemetry (collector + `/api/telemetry`); rooms lit up/down
- [x] Host metrics on stations (GPU/RAM/load for T5810)
- [x] Service web-UI links open in a new tab
- [x] Agent terminal drill level (read + send on the real thread)
- [x] Program operations layer: health, logs, assignment, and guarded restart
  routed to a real agent on the owning machine (local checkout; deploy pending)

Still placeholder/none: real sprite art, room interiors, effects.

## Immediate

- [x] Create repo structure
- [x] Add initial concept asset sheet
- [x] Add README
- [x] Add ROADMAP
- [x] Add STYLE_GUIDE
- [x] Add WORLD_LAYOUT
- [x] Add STATIONS
- [x] Add ROOMS
- [x] Add AGENTS
- [x] Add UI_COMPONENTS
- [x] Add EFFECTS
- [x] Add ANIMATION_GUIDE
- [x] Add PROMPT_TEMPLATE
- [x] Add ASSET_NAMING

## Next Asset Sheets

- [ ] Agent role sprite sheet
- [ ] Station icon sheet
- [ ] Room interior sheet
- [ ] UI component sheet
- [ ] Effects sheet
- [ ] Status icon sheet
- [ ] Background/grid sheet

## Production Prep

- [ ] Crop concept sheets into individual assets
- [ ] Create transparent PNG versions
- [ ] Create WebP optimized versions
- [ ] Add source prompts beside generated images
- [ ] Add metadata JSON for asset families
- [ ] Decide sprite sizes
- [ ] Decide room tile sizes
- [ ] Decide station icon sizes

## Claude/Codex Tasks

- [ ] Read all design docs before generating or using assets
- [ ] Build asset loader that supports categories and states
- [ ] Add fallback placeholder system
- [ ] Add theme support
- [ ] Add reduced-motion mode
- [ ] Add low-power/potato mode
- [ ] Add asset manifest support

## Visual Priorities

1. Readability
2. Functionality
3. Consistency
4. Performance
5. Style polish

## Do Not Do Yet

- [ ] Do not spend days polishing animations before the UI works.
- [ ] Do not bake labels into images.
- [ ] Do not copy copyrighted game assets.
- [ ] Do not make huge images that slow down old machines.
- [ ] Do not let asset style drift without updating the style guide.
