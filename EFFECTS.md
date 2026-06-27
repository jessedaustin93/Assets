# Agent Mesh Effects

Effects communicate live activity, alerts, movement, and task progress.

Effects should support real state. They should not create fake activity.

## Core Effect Rules

- Effects should be lightweight.
- Effects should be readable at a glance.
- Effects should correspond to actual events or states.
- Effects should be reusable across stations, rooms, and agents.
- Effects should not obscure controls or text.

## Primary Effect Categories

### SSH Beam

Used when an agent or user opens an SSH/session connection.

Visual:
- Thin blue/cyan beam or dotted route
- Connection pulse from source to target
- Optional terminal icon pulse

States:
- connecting
- active
- failed
- closed

### Deploy Beam

Used when code/config is deployed or files are pushed.

Visual:
- Brighter beam than SSH
- Packet bursts or crate icons moving along path
- Completion flash at target

States:
- pending
- transferring
- applying
- complete
- failed

### Packet Flow

Used for network activity, SnifferOps, Tailscale, DNS, media streaming.

Visual:
- Small dots moving along connection lines
- Directional arrows
- Rate can control density/speed

States:
- low traffic
- normal traffic
- high traffic
- blocked
- suspicious

### Radar Sweep

Used by SnifferOps and sensor rooms.

Visual:
- Rotating sweep arc
- Fading contact dots
- New contact pulse

States:
- scanning
- contact found
- tracking
- alert

### Build / Compile Sparks

Used by developer agents and build rooms.

Visual:
- Small orange sparks
- Code block shimmer
- Progress pulse

States:
- building
- testing
- failed
- passed

### CPU Heat Glow

Used when a host or room is under load.

Visual:
- Orange glow overlay
- Heat shimmer if supported

States:
- normal
- warm
- hot
- critical

### GPU Core Glow

Used by AI/model workloads.

Visual:
- Purple/blue reactor glow
- Pulsing VRAM indicator

States:
- idle
- loaded
- inference
- overloaded

### Storage Fill

Used for disks/media/backups.

Visual:
- Storage silos or crates filling
- Progress overlay

States:
- safe
- filling
- near full
- full/error

### Warning Pulse

Used for warnings and failed services.

Visual:
- Yellow or red pulse around object
- Optional alert triangle overlay

States:
- warning
- error
- critical
- resolved

### Construction / Update

Used when creating new rooms, updating services, or installing assets.

Visual:
- Scaffolding outline
- Small drones/bots
- Progress frame

States:
- queued
- building
- applying
- complete
- failed

## Effect Asset Requirements

Each major effect should eventually have:

- static preview
- short loop
- start frame
- active loop
- end frame
- fail state if applicable

## Naming Examples

```text
effect_ssh_beam_active_01.png
effect_deploy_beam_transfer_01.png
effect_packet_flow_normal_01.png
effect_radar_sweep_loop_01.png
effect_warning_pulse_red_01.png
effect_gpu_core_glow_busy_01.png
```
