# Station Mapping

This document maps real homelab machines to Agent Mesh station concepts.

The exact hardware may change. Update this document when the real environment changes.

## Station Naming Rule

A station should have:

- user-friendly name
- real host/machine identity
- role
- rooms/services
- status source
- asset subject ID

## T5810 - AI Flagship

Asset subject:

```text
t5810_ai_flagship
```

Role:

AI compute, local LLM, coding agents, GPU workloads, heavy work.

Suggested station rooms:

```text
Bridge
AI Core
GPU Reactor
Engineering
Build Lab
Model Storage
Agent Barracks
```

Telemetry to show:

- CPU
- RAM
- GPU load
- VRAM
- disk
- running agents
- active models
- current jobs

## T3610 - Media and Infrastructure Station

Asset subject:

```text
t3610_media_station
```

Role:

Docker media stack, Jellyfin, ARR stack, Navidrome, Vaultwarden, downloads, media storage.

Suggested station rooms:

```text
Bridge
Docker Bay
Jellyfin Theater
ARR Cargo Office
Vaultwarden Vault
Media Storage
Download Dock
Communications
```

Telemetry to show:

- CPU
- RAM
- disk/storage
- container status
- media streams
- transcodes
- download/import queue
- service alerts

## Raspberry Pi 5 - Sensor Outpost

Asset subject:

```text
pi5_sensor_outpost
```

Role:

Pi-hole, SDR, sensor support, lightweight services.

Suggested station rooms:

```text
Sensor Array
DNS Control
SDR Listening Post
Telemetry Room
```

Telemetry to show:

- DNS queries
- service health
- SDR status
- CPU/RAM
- temperature if available

## HP Automation Node

Asset subject:

```text
hp_automation_node
```

Role:

Home Assistant or home automation services.

Suggested station rooms:

```text
Automation Control
Device Registry
Alert Panel
Utility Logs
```

## Chromebook Kiosk

Asset subject:

```text
chromebook_kiosk
```

Role:

Display console, media kiosk, browser-based terminal surface.

Suggested rooms:

```text
Kiosk Display
Jellyfin Client
Browser Console
```

## ESP32 Recon Nodes

Asset subject:

```text
esp32_recon_node
```

Role:

Small sensor/recon nodes.

Suggested view:

Use compact device panels instead of full rooms at first.

Telemetry to show:

- last seen
- battery if available
- signal strength
- sensor type
- location if available

## Generic Station

Asset subject:

```text
generic_station
```

Use for new hosts before custom art exists.

## Asset State Mapping

Station art should follow status priority:

```text
offline > error > warning > updating > busy > idle
```

Selection and hover should usually be overlays.
