# RTS Interaction Guide

Agent Mesh should feel like a real-time strategy command interface, but the interactions must control real systems.

## Core Interaction Model

The user selects objects, inspects status, and issues commands.

Objects include:

- stations
- rooms
- agents
- services
- tasks
- alerts
- connections

## Selection

Clicking/tapping an object should select it and show relevant controls.

### Station Selected

Show:

- station status
- resource summary
- active rooms/services
- active agents
- alerts
- quick commands

Possible commands:

```text
Open Station
Open Terminal
View Logs
Run Health Check
Assign Agent
Restart Service
Open Files
```

### Room Selected

Show:

- room/service status
- logs
- telemetry
- assigned agents
- active tasks
- related controls

Possible commands:

```text
Open Room
View Logs
Open Terminal
Restart Service
Assign Agent
Clear Alert
Open Config
```

### Agent Selected

Show:

- role
- current location
- current task
- recent actions
- transcript/logs
- permissions/tool access

Possible commands:

```text
Assign Task
Pause
Resume
Stop
Return To Base
View Transcript
Open Working Directory
```

## Right-Click / Long-Press Commands

Desktop can use right-click.
Mobile can use long-press.

The command menu should be compact, readable, and contextual.

## Drag / Assign

Future behavior:

- drag agent onto room to assign
- drag task onto agent
- drag file/package onto target service

Do not implement fake assignments. If the app shows assignment, the backend should record the task state.

## Routes And Movement

Agent movement should represent task state.

Example:

```text
User assigns Engineer to T3610 > Docker Bay
Agent route appears
Agent travels visually
Task starts when agent arrives
Logs open or become available
```

## Alerts

Alerts should be selectable objects.

Clicking an alert should show:

- what failed
- when it started
- severity
- affected station/room
- suggested action
- logs
- clear/snooze controls

## Mission / Task Cards

Tasks can be shown like RTS objectives.

Fields:

- title
- target
- assigned agent
- status
- progress
- logs
- required input

## Interaction Priority

1. Status must be readable.
2. Commands must be discoverable.
3. Logs must be reachable.
4. Effects must not block controls.
5. Animations must reflect real state.

## Mobile Rules

- Large tap targets.
- Long-press replaces right-click.
- Bottom-sheet command panels are acceptable.
- Avoid tiny RTS controls that only work with a mouse.

## Keyboard Shortcuts Later

Potential shortcuts:

```text
Esc      back / deselect
Enter    open selected
L        logs
T        terminal
H        health check
A        assign agent
Space    pause visual updates
```
