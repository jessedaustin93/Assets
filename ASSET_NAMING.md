# Agent Mesh Asset Naming Guide

Consistent names make assets easier for Claude, Codex, scripts, and the app to find.

Use lowercase names with underscores.

## General Pattern

```text
category_subject_variant_state_index.extension
```

Examples:

```text
station_t5810_flagship_idle_01.png
room_ai_core_busy_01.png
agent_engineer_walk_01.png
effect_ssh_beam_active_01.png
ui_panel_tactical_dark_01.png
```

## Categories

Use these category prefixes:

```text
station_
room_
agent_
effect_
ui_
icon_
background_
concept_
prompt_
```

## States

Common state names:

```text
idle
busy
warning
error
offline
selected
hover
active
inactive
complete
failed
connecting
updating
locked
unlocked
```

## Agent Actions

Use these for animated/posed agent assets:

```text
idle
walk
type
repair
carry
scan
alert
complete
blocked
return
```

## Station Naming

```text
station_[host_or_type]_[role]_[state]_[index].png
```

Examples:

```text
station_t5810_ai_flagship_idle_01.png
station_t3610_media_station_warning_01.png
station_pi5_sensor_outpost_busy_01.png
station_esp32_recon_node_idle_01.png
```

## Room Naming

```text
room_[room_name]_[state]_[index].png
```

Examples:

```text
room_ai_core_idle_01.png
room_docker_bay_busy_01.png
room_jellyfin_theater_warning_01.png
room_snifferops_radar_alert_01.png
room_vaultwarden_vault_locked_01.png
```

## Agent Naming

```text
agent_[role]_[action]_[index].png
```

Examples:

```text
agent_engineer_idle_01.png
agent_engineer_repair_01.png
agent_developer_type_01.png
agent_signal_officer_scan_01.png
agent_cargo_bot_carry_01.png
```

## UI Naming

```text
ui_[component]_[variant]_[state]_[index].png
```

Examples:

```text
ui_panel_tactical_dark_idle_01.png
ui_button_primary_hover_01.png
ui_selection_ring_station_selected_01.png
ui_progress_bar_frame_cyan_01.png
```

## Effects Naming

```text
effect_[effect_name]_[state]_[index].png
```

Examples:

```text
effect_ssh_beam_connecting_01.png
effect_deploy_beam_active_01.png
effect_packet_flow_normal_01.png
effect_radar_sweep_alert_01.png
effect_warning_pulse_red_01.png
```

## Concept Naming

Concepts can be broader because they are exploratory.

```text
concept_[asset_family]_[short_description]_v[number].png
```

Examples:

```text
concept_ui_asset_sheet_v1.png
concept_station_icons_v1.png
concept_agent_roles_v1.png
concept_room_interiors_v1.png
```

## Prompt Naming

```text
prompt_[asset_family]_[purpose].md
```

Examples:

```text
prompt_agent_sheet_base.md
prompt_station_sheet_base.md
prompt_room_sheet_base.md
prompt_ui_components_base.md
```

## Versioning

Use `_v1`, `_v2`, `_v3` for concept generations.

Use `_01`, `_02`, `_03` for individual production variants or frames.

Do not overwrite good assets unless intentionally replacing them.
