# Agent Mesh World Layout

Agent Mesh should feel like zooming through a real-time strategy command map, but every layer represents real infrastructure.

## Drill-Down Hierarchy

```text
World Map
  ↓
Station / Host
  ↓
Room / Service
  ↓
Object / Tool
  ↓
Agent / Task
  ↓
Terminal / Logs / Controls
```

The interface should support adding more layers later without changing the basic navigation model.

## World Map

The world map is the top-level command view.

It displays every major machine, node, or environment as a station.

Examples:

- T5810 AI Flagship
- T3610 Media and Infrastructure Station
- Raspberry Pi 5 Sensor Outpost
- HP Home Assistant Node
- Chromebook Kiosk
- ESP32 Recon Nodes
- Phone/Mobile Console
- Cloud/VPS nodes if added later

## Station View

A station represents one host machine or major environment.

Station view should show:

- Host identity
- Rooms/services running on that host
- Current system status
- Resource bars
- Agent presence
- Active routes/connections
- Alerts

## Room View

A room represents a real service, project, or function.

Examples:

- AI Core
- Engineering
- SnifferOps Radar
- Jellyfin Theater
- Vaultwarden Vault
- Docker Bay
- Communications
- Storage
- Build Lab

Room view should show:

- Service status
- Controls
- Logs
- Current tasks
- Assigned agents
- Related files/repos
- Telemetry panels

## Agent View

Agent view focuses on one AI/helper/automation.

It should show:

- Current task
- Target machine
- Working directory
- Tool access
- Recent actions
- Logs or conversation
- Pause/stop/resume controls

## Terminal View

Terminal view is the deepest layer.

It can expose:

- SSH session
- Container logs
- Git output
- Service logs
- Command queue
- Agent transcript

## Navigation Rules

- Clicking a station drills into station view.
- Clicking a room drills into room view.
- Clicking an agent opens task/agent view.
- Clicking a terminal object opens logs or shell.
- Back navigation should always be obvious.
- Breadcrumbs should show the current path.

Example breadcrumb:

```text
World > T3610 > Jellyfin Theater > Media Scanner > Logs
```

## Visual Rules

- Top-level view should be sparse and readable.
- Deeper views can show more detail.
- Never hide real status behind decorative animation.
- Status should be visible even when assets are still placeholders.
