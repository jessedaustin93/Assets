# Metadata

This folder stores machine-readable asset information for Agent Mesh.

Metadata lets the app load assets by meaning instead of hardcoded filenames.

## Recommended Files

```text
assets.manifest.json          Main runtime asset manifest
assets.manifest.example.json  Example manifest format
asset_families.json           List of known categories, subjects, and states
status_states.json            Standard state definitions
fallbacks.json                Optional fallback chains
```

## Goals

- Let the app resolve assets by category, subject, state, and variant.
- Track source prompts and concept sheets.
- Support fallback assets.
- Support future themes.
- Keep the app from breaking when an asset is missing.

## Rule

The UI should still work when metadata is incomplete.

Metadata improves the experience; it should not become a single point of failure.
