# Agent Mesh Stations

Stations are the RTS-style representation of real machines, hosts, or major environments.

> **Live status:** the working implementation, real per-machine services, and the
> `stations.json` schema are documented in [IMPLEMENTATION_STATUS.md](IMPLEMENTATION_STATUS.md).
> Stations are keyed by agent-id suffix (`t5810`/`t3610`/`hp`/`x1`) and lit by real
> telemetry. There are 4 machines on the network today.

Each station should be visually distinct, clickable, and tied to live status.

## Station Data Model

Each station should eventually support:

- Display name
- Hostname
- IP / Tailscale IP
- Role
- Status
- CPU load
- RAM use
- Disk use
- GPU use if available
- Services/rooms
- Agents currently present
- Active tasks
- Alerts

## Station Status States

- Healthy
- Busy
- Warning
- Error
- Offline
- Updating
- Unknown

## T5810 - AI Flagship

Role: AI compute, local LLM, agent execution, heavy workloads.

Suggested visual:

- Large flagship/server-station silhouette
- Purple/blue AI core glow
- GPU/reactor visual motif
- Strong command ship identity

Suggested rooms:

- Bridge
- AI Core
- Engineering
- GPU Reactor
- Build Lab
- Agent Barracks
- Model Storage

## T3610 - Media and Infrastructure Station

Role: Docker services, Jellyfin, ARR stack, Navidrome, Vaultwarden, downloads, media storage.

Suggested visual:

- Industrial cargo/media station
- Storage bays and server racks
- Green/blue healthy infrastructure lighting

Suggested rooms:

- Docker Bay
- Jellyfin Theater
- ARR Cargo Office
- Vaultwarden Vault
- Media Storage
- Download Dock
- Network Room

## Raspberry Pi 5 - Sensor Outpost

Role: Pi-hole, SDR, sensors, lightweight services.

Suggested visual:

- Small outpost/satellite node
- Radar dish or antenna mast
- Compact but important

Suggested rooms:

- Sensor Array
- DNS Control
- SDR Listening Post
- Telemetry Room

## HP Node - Home Automation / Utility Node

Role: Home Assistant or future local automation services.

Suggested visual:

- Utility station
- House/system control iconography
- Calm blue/green status language

Suggested rooms:

- Automation Control
- Device Registry
- Alert Panel
- Utility Logs

## Chromebook Kiosk

Role: lightweight display console or kids/media kiosk.

Suggested visual:

- Small terminal outpost
- Simple console station
- Low-power status badge

Suggested rooms:

- Kiosk Display
- Jellyfin Client
- Browser Console

## ESP32 Recon Nodes

Role: small sensors, mesh nodes, recon points, BLE/Wi-Fi/LoRa experiments.

Suggested visual:

- Tiny drones or satellite pings
- Battery and signal indicators
- Swarm-style map markers

Suggested rooms:

ESP32 nodes may not need full rooms at first. They can drill down into a compact device panel.

## Future Station Types

- Laptop field console
- Phone mobile command console
- VPS/cloud relay
- Backup server
- Camera/security node
- SDR vehicle node

## Station Asset Requirements

Each station family should eventually have:

- idle
- busy
- warning
- error
- offline
- selected
- hover

Naming examples:

```text
station_t5810_idle.png
station_t5810_busy.png
station_t5810_warning.png
station_t3610_idle.png
station_pi5_sensor_outpost_idle.png
```
