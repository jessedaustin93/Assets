# Jellyfin Theater Room

The Jellyfin Theater represents the Jellyfin media service inside Agent Mesh.

It should be useful as a real service-control room, not just a movie-themed decoration.

## Purpose

Show media-server health, active playback, library activity, and common controls.

## Parent Station

Usually:

```text
T3610 - Media and Infrastructure Station
```

## Visual Theme

- theater screen
- media shelves
- transcode console
- scanner bot
- storage indicators
- calm blue/green when healthy
- orange/purple glow during transcoding
- yellow/red warning for playback or library errors

## Useful Telemetry

- service status
- active streams
- transcoding sessions
- library scan status
- user count
- storage usage
- recent errors
- container health if running in Docker

## Room Objects

Suggested clickable objects:

```text
media_screen
library_scanner_console
transcode_console
storage_shelves
logs_terminal
service_control_panel
```

## Common Commands

```text
Open Jellyfin
View Logs
Restart Jellyfin
Run Library Scan
Check Transcodes
Open Media Storage
Assign Agent
```

## Visual States

```text
idle       service healthy, no major activity
busy       streams, transcodes, or scan active
warning    playback warning, storage warning, scanner warning
error      service/container failed
offline    unavailable
updating   service restart/update in progress
```

## Asset Ideas

```text
room_jellyfin_theater_idle_01.png
room_jellyfin_theater_busy_01.png
room_jellyfin_theater_warning_01.png
prop_media_screen_idle_01.png
prop_transcode_console_busy_01.png
```

## Agent Usage

- Engineer fixes service/container problems.
- Cargo bot handles media import/sorting visualization.
- Maintenance bot can run scans/cleanup.

## Safety Notes

Do not expose private user watch history broadly unless the app is intentionally local/private.
