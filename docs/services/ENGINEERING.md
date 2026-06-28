# Engineering Room

The Engineering Room represents system administration, repair, service management, and low-level host work.

It should be practical first: quick access to logs, health checks, terminals, and safe repair actions.

## Purpose

Show host health, failed services, update status, and repair tasks.

## Visual Theme

- workbench
- terminal wall
- repair tools
- service panels
- maintenance drone dock
- blue/green healthy state
- orange active repair/build state
- yellow warning
- red failed service state

## Useful Telemetry

- host status
- CPU/RAM/disk
- uptime
- failed services
- package updates available
- disk mount status
- recent restarts
- health check result
- temperature if available

## Room Objects

Suggested clickable objects:

```text
terminal_wall
repair_bench
service_status_panel
update_console
mounts_panel
maintenance_drone_dock
```

## Common Commands

```text
Open Terminal
View System Logs
Run Health Check
View Failed Services
Check Updates
Restart Service
Check Disk Mounts
Assign Engineer
```

## Visual States

```text
idle       host healthy, no repair active
busy       health check, update, or repair running
warning    service warning, updates pending, disk/resource warning
error      critical service or host issue
offline    host unavailable
updating   packages/service updates in progress
```

## Asset Ideas

```text
room_engineering_idle_01.png
room_engineering_busy_01.png
room_engineering_warning_01.png
prop_repair_bench_idle_01.png
prop_terminal_wall_active_01.png
agent_engineer_repair_01.png
```

## Agent Usage

- Engineer is primary.
- Maintenance bot handles routine checks.
- Developer may use Engineering for build environment issues.

## Safety Notes

Confirm high-impact changes such as service removals, network changes, bulk deletes, or permission changes.
