# Asset Fallback Rules

Agent Mesh should never crash or become unusable because art is missing.

Fallbacks are mandatory.

## Fallback Order

When the app requests an asset, try this order:

```text
1. Exact asset
2. Same subject, idle state
3. Generic subject, same state
4. Generic subject, idle state
5. Category placeholder
```

## Example

Request:

```text
station_t5810_ai_flagship_warning_01.png
```

Fallback chain:

```text
station_t5810_ai_flagship_warning_01.png
station_t5810_ai_flagship_idle_01.png
station_generic_warning_01.png
station_generic_idle_01.png
placeholder_station.png
```

## Missing Asset Logging

When fallback occurs, log:

- requested asset id
- fallback asset id
- category
- subject
- state
- caller/screen if available

This makes it easy to generate missing assets later.

## Placeholder Rules

Placeholders should:

- be simple
- be obvious
- not look final
- preserve layout size
- allow app-rendered labels
- keep controls usable

## UI Rule

Do not hide a control because its decorative asset is missing.

The interface should still work with plain boxes and text.

## Development Rule

If adding a new station, room, agent, or state, add either:

- a real asset
- a generic fallback
- or a placeholder

before relying on it in the UI.
