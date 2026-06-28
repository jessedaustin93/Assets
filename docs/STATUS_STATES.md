# Status States

Status states connect real telemetry to visual behavior.

The same general state names should be reused across stations, rooms, agents, effects, and UI.

## Core States

### idle

Online and healthy, with no active visible work.

### busy

Actively doing work.

Examples:
- agent running command
- service scanning library
- model performing inference
- download/import active

### warning

Needs attention but is not fully failed.

Examples:
- disk nearing full
- high CPU
- service restarted recently
- task waiting longer than expected

### error

Something failed.

Examples:
- service down
- task failed
- host command returned failure
- container unhealthy

### offline

Unreachable, powered down, or intentionally disconnected.

### selected

User has selected the object.

Usually this should be an overlay, not a separate full sprite.

### hover

Pointer or focus hover state.

### connecting

A connection is being opened.

Examples:
- SSH session starting
- API connection pending
- agent connecting to host

### updating

A service, room, station, or asset is changing.

### blocked

A task cannot continue without input, permissions, or missing dependency.

### complete

Task completed successfully.

### failed

Task finished unsuccessfully.

## Mapping Real Data To States

### Station

```text
offline   host unreachable
error     host reachable but critical service failed
warning   resource or service warning
busy      high activity or assigned work
idle      healthy and quiet
```

### Room

```text
offline   service stopped/unavailable
error     service health check failed
warning   degraded state
busy      active task/log activity
idle      healthy and quiet
```

### Agent

```text
idle      waiting for assignment
busy      actively working
blocked   needs input
failed    task failed
complete  task succeeded briefly, then returns to idle
```

### Effect

```text
active    effect is running
warning   caution effect
error     error effect
complete  success effect
failed    failure effect
```

## Visual Priority

When multiple states apply, use this priority:

```text
offline > error > warning > blocked > updating > busy > selected > hover > idle
```

Selection and hover should usually be overlays so they can coexist with warning/error states.
