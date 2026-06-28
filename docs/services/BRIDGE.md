# Bridge Room

The Bridge is the command overview for a station.

It should summarize the station without replacing deeper room views.

## Purpose

Show the station's overall state, quick actions, active agents, alerts, and major telemetry.

## Visual Theme

- command table
- station hologram
- alert console
- agent status board
- resource display
- calm blue/green when healthy
- yellow/red for warnings/errors

## Useful Telemetry

- station online/offline state
- CPU/RAM/disk summary
- GPU summary if available
- active room count
- service alerts
- active agents
- task count
- network status
- uptime

## Room Objects

Suggested clickable objects:

```text
station_hologram
resource_console
alert_board
agent_status_panel
quick_actions_console
logs_terminal
```

## Common Commands

```text
Open Station Terminal
Run Health Check
View Alerts
View Active Agents
Open Logs
Open Rooms
Assign Agent
```

## Visual States

```text
idle       station healthy and quiet
busy       station has active tasks
warning    one or more rooms/services need attention
error      station has critical failure
offline    station unreachable
selected   station selected on world map
```

## Asset Ideas

```text
room_bridge_idle_01.png
room_bridge_busy_01.png
room_bridge_warning_01.png
prop_station_hologram_idle_01.png
prop_alert_board_warning_01.png
```

## Agent Usage

Any agent can appear on the Bridge when assigned to station-level work.

Commander role can be represented here later.
