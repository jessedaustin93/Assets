# Agent Mesh Asset Manifest Schema

This document defines a simple manifest format for mapping real UI objects to art assets.

The exact implementation can change, but the concepts should remain stable.

## Why Use A Manifest

A manifest lets the app ask for an asset by meaning instead of by hardcoded filename.

Example:

```text
Give me the warning version of the T3610 station.
```

The manifest maps that request to a file path.

## Basic Manifest Example

```json
{
  "version": 1,
  "assets": [
    {
      "id": "station_t5810_ai_flagship_idle_01",
      "category": "station",
      "subject": "t5810_ai_flagship",
      "state": "idle",
      "variant": "01",
      "path": "sprites/stations/station_t5810_ai_flagship_idle_01.png",
      "tags": ["server", "ai", "flagship"],
      "notes": "Default idle state for the T5810 AI station."
    }
  ]
}
```

## Required Fields

### id

Unique asset ID. Should usually match the filename without extension.

### category

One of:

```text
station
room
agent
effect
ui
icon
background
concept
```

### subject

The specific thing represented.

Examples:

```text
t5810_ai_flagship
jellyfin_theater
engineer
ssh_beam
selection_ring
```

### state

The visual state.

Examples:

```text
idle
busy
warning
error
offline
selected
active
complete
failed
```

### variant

A small version marker such as `01`, `02`, or `03`.

### path

Runtime or repo path to the asset file.

## Optional Fields

```json
{
  "width": 128,
  "height": 128,
  "frame_count": 4,
  "frame_rate": 8,
  "loop": true,
  "transparent": true,
  "source_prompt": "prompts/agent_sheet_base.md",
  "source_sheet": "concepts/concept_agent_roles_v1.png",
  "license": "project-owned/generated",
  "created_by": "ChatGPT/Claude/Codex/user",
  "notes": "Any useful implementation notes."
}
```

## Fallbacks

The manifest can include a fallback list.

```json
{
  "id": "station_t5810_ai_flagship_warning_01",
  "fallbacks": [
    "station_t5810_ai_flagship_idle_01",
    "station_generic_warning_01",
    "placeholder_station_01"
  ]
}
```

## Suggested File Location

```text
metadata/assets.manifest.json
```

## App Behavior

When an asset is missing:

1. Try exact match.
2. Try same subject with idle state.
3. Try same category generic state.
4. Try category placeholder.
5. Log the missing asset.

Never crash the UI because an asset is missing.
