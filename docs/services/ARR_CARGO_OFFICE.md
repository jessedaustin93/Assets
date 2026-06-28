# ARR Cargo Office

The ARR Cargo Office represents media request, search, download, and import workflows.

It should visualize queues and sorting like an RTS cargo/logistics room.

## Purpose

Show the state of Sonarr, Radarr, Lidarr, Prowlarr, download clients, and import queues.

## Visual Theme

- cargo manifests
- crates
- conveyor belts
- download dock
- sorting desk
- queue board
- green healthy logistics
- yellow stuck/waiting items
- red failed imports/downloads

## Useful Telemetry

- wanted/missing count
- download queue
- failed downloads
- import queue
- indexer health
- service status
- disk free space
- recent imports

## Room Objects

Suggested clickable objects:

```text
cargo_manifest_board
download_dock
sorting_conveyor
indexer_console
queue_terminal
media_crates
```

## Common Commands

```text
Open Sonarr
Open Radarr
Open Prowlarr
View Queue
View Failed Items
Search Missing
Check Indexers
Open Download Client
Assign Cargo Bot
```

## Visual States

```text
idle       services healthy and queue normal
busy       downloads/imports/searches active
warning    failed items, stuck queue, indexer warning
error      service failed or import path broken
offline    services unavailable
```

## Asset Ideas

```text
room_arr_cargo_office_idle_01.png
room_arr_cargo_office_busy_01.png
room_arr_cargo_office_warning_01.png
prop_media_crate_idle_01.png
prop_sorting_conveyor_active_01.png
agent_cargo_bot_carry_01.png
```

## Agent Usage

- Cargo bot visualizes imports and file movement.
- Engineer fixes service/path issues.
- Maintenance bot checks queues and indexers.

## Safety Notes

Avoid showing sensitive tracker/indexer credentials in the UI.

Confirm destructive deletes or bulk cleanup actions.
