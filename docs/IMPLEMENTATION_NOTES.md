# Agent Mesh Asset Implementation Notes

These notes describe how the Agent Mesh app should consume the assets in this repository.

## Asset System Goals

The app should not hardcode image paths everywhere.

Instead, it should use a predictable asset registry or manifest that maps functional objects to visual assets.

## Recommended Asset Lookup

Use a lookup model like this:

```json
{
  "category": "station",
  "subject": "t5810_ai_flagship",
  "state": "idle",
  "variant": "01"
}
```

The loader can resolve that into a file path:

```text
sprites/stations/station_t5810_ai_flagship_idle_01.png
```

## Fallback Chain

Every asset lookup should have a fallback chain.

Example:

```text
station_t5810_ai_flagship_warning_01.png
station_t5810_ai_flagship_idle_01.png
station_generic_warning_01.png
station_generic_idle_01.png
placeholder_station.png
```

This lets the UI keep working even when real art is missing.

## State Mapping

Real telemetry should drive visual state.

Example station state mapping:

```text
offline: host unreachable
error: critical service failed
warning: disk/RAM/CPU/service warning
busy: active task or heavy load
idle: healthy and quiet
selected: user selection overlay
```

Example agent state mapping:

```text
idle: no active task
assigned: task accepted but not started
walking: visual travel to target room
working: active command/job running
blocked: needs input or failed precondition
failed: task ended unsuccessfully
complete: task ended successfully
```

## Separate Art From Data

Do not bake names, labels, percentages, logs, or buttons into image assets.

The application should render live data over reusable art.

## Recommended Metadata

Each asset family can have a metadata JSON file later.

Useful fields:

- id
- category
- subject
- state
- variant
- path
- width
- height
- frame_count
- frame_rate
- loop
- tags
- notes
- source_prompt

## Low-Power Mode

Agent Mesh should support a reduced rendering mode.

In low-power mode:

- use static assets
- disable particles
- disable animated glows
- lower update frequency
- simplify shadows
- hide nonessential background movement

## Asset Packaging

For web deployment, production assets may eventually be exported to optimized WebP.

Keep original PNGs or source files if possible.

Recommended generated outputs:

```text
raw/          original generated sheets
cropped/      individual PNG assets
webp/         optimized runtime assets
metadata/     JSON manifests
```

## Do Not Block Development On Final Art

Placeholders are acceptable and expected.

A working clickable placeholder room is better than a polished room that does nothing.
