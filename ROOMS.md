# Agent Mesh Rooms

Rooms represent real services, projects, or functional zones inside a station.

A room is not just decoration. It should expose useful controls, live status, logs, agents, and tasks.

## Room Data Model

Each room should eventually support:

- Room name
- Parent station
- Service/project mapping
- Status
- Health checks
- Logs
- Controls
- Active agents
- Active tasks
- Related files/repos
- Telemetry widgets

## Common Room States

- Idle
- Busy
- Warning
- Error
- Offline
- Updating
- Locked
- Selected

## Room Types

### Bridge

Purpose: command overview for a station.

Contains:
- Station summary
- Alerts
- Active agents
- Quick actions
- Resource overview

### AI Core

Purpose: LLM/model activity and AI orchestration.

Contains:
- Model racks
- GPU core/reactor
- Agent consoles
- Task queue display
- Memory/context indicators

Telemetry:
- GPU use
- VRAM use
- Active models
- Token/task activity

### Engineering

Purpose: Linux administration, repair, updates, shell work.

Contains:
- Tool benches
- Terminal panels
- Repair drone dock
- Service restart controls

Telemetry:
- CPU
- RAM
- disk
- services
- package/update status

### Docker Bay

Purpose: container management.

Contains:
- Container racks
- Deployment cranes
- Status lights
- Logs panel

Telemetry:
- Running containers
- Restarting containers
- Failed containers
- Image updates

### Jellyfin Theater

Purpose: Jellyfin/media server control.

Contains:
- Theater screen
- Media shelves
- Transcode console
- Library scanner bot

Telemetry:
- Streams
- Transcodes
- Library scan status
- Storage usage

### ARR Cargo Office

Purpose: Sonarr/Radarr/Lidarr/Prowlarr workflow.

Contains:
- Cargo manifests
- Download dock
- Sorting conveyor
- Queue board

Telemetry:
- Queue
- missing media
- failed downloads
- import status

### Vaultwarden Vault

Purpose: password vault/security room.

Contains:
- Vault door
- Lock console
- Sync status
- Security agent post

Telemetry:
- service health
- backups
- sync status
- alerts

### SnifferOps Radar Room

Purpose: RF/Wi-Fi/BLE/SDR awareness and signal analysis.

Contains:
- Radar scope
- Signal map
- Packet analyzer terminal
- Recon drone dock

Telemetry:
- detections
- new devices
- RSSI changes
- GPS/position data
- alert contacts

### Communications Room

Purpose: network, VPN, Tailscale, SSH, DNS.

Contains:
- Link map
- SSH relay console
- VPN gateway
- DNS board

Telemetry:
- active links
- latency
- DNS queries
- tunnel status

### Storage Room

Purpose: drives, media libraries, backups.

Contains:
- Storage silos
- Crates
- Backup console
- Disk health indicators

Telemetry:
- free space
- SMART status
- mounts
- backup jobs

## Room Asset Rules

- Rooms should have open space for agents.
- Interactive objects should be visually obvious.
- Do not bake room names into the art.
- Room background and UI overlay should be separate.
- Each room should work as a static image first, then gain animation states later.

## Naming Examples

```text
room_ai_core_idle.png
room_ai_core_busy.png
room_docker_bay_warning.png
room_jellyfin_theater_idle.png
room_snifferops_radar_alert.png
```
