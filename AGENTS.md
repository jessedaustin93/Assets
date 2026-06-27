# Agent Mesh Agents

Agents are the visual representation of AI helpers, automations, scripts, services, and user-directed workers.

Agents should move and animate because real work is happening.

## Core Rule

Do not fake productivity. If an agent appears to be working, it should correspond to a real task, command, job, log stream, or service action.

## Agent Data Model

Each agent should eventually support:

- Name
- Role
- Current station
- Current room
- Current task
- Status
- Permissions
- Tool access
- Assigned project/repo
- Last action
- Logs/transcript

## Agent Status States

- Idle
- Assigned
- Walking
- Working
- Typing
- Repairing
- Carrying
- Waiting
- Blocked
- Failed
- Complete
- Returning

## Agent Roles

### Commander

Purpose: user-facing command/control role.

Visual:
- Distinct leader silhouette
- Strong selection ring
- Minimal animation needed

### Engineer

Purpose: Linux, Docker, server repair, service restarts.

Visual:
- Mechanic/tech silhouette
- Tool pack or repair drone
- Yellow/orange accents

Animations:
- idle
- walk
- type
- repair
- alert

### Developer

Purpose: coding, Git work, app changes, tests.

Visual:
- Console/operator silhouette
- Blue/cyan accents
- Laptop/terminal prop

Animations:
- idle
- walk
- type
- compile/build
- blocked

### Scientist / LLM Operator

Purpose: model work, research, prompt testing, AI reasoning tasks.

Visual:
- Hologram/model console
- Purple AI accents
- Data orb or neural display

Animations:
- idle
- analyze
- type
- thinking
- complete

### Signal Officer

Purpose: SnifferOps, SDR, BLE/Wi-Fi/LoRa awareness, RF analysis.

Visual:
- Radar headset/operator
- Antenna or scanning device
- Green/cyan signal accents

Animations:
- idle
- scan
- analyze
- alert
- track

### Security Officer

Purpose: Vaultwarden, access, firewall, VPN, auth, secrets.

Visual:
- Guard/lock motif
- Shield icon accent
- Green/red alert states

Animations:
- idle
- patrol
- lock
- unlock
- alert

### Cargo Bot

Purpose: media movement, ARR stack, downloads, file transfers.

Visual:
- Small cargo robot
- Crate carrier
- Conveyor/dock motif

Animations:
- idle
- carry
- move
- sort
- complete

### Maintenance Bot

Purpose: generic service cleanup, health checks, scheduled jobs.

Visual:
- Small utility bot
- Tool arms
- Friendly but practical

Animations:
- idle
- roll/walk
- repair
- clean
- error

### Recon Drone

Purpose: ESP32, sensor nodes, field data, RF contacts.

Visual:
- Small drone/satellite marker
- Battery/signal status
- Map-friendly silhouette

Animations:
- idle hover
- scan pulse
- move
- low battery
- alert

## Visual Rules

- Agents should be readable at small size.
- Role should be obvious from silhouette and accent color.
- Keep sprites simple enough for low-end machines.
- Use transparent backgrounds.
- Avoid text in sprites.

## Behavior Rules

- Agent movement should be tied to assignment state.
- Agent working animation should be tied to task execution.
- Agent error animation should be tied to real failure/blockage.
- Agent complete animation should be brief and then return to idle/available.

## Naming Examples

```text
agent_engineer_idle_01.png
agent_engineer_walk_01.png
agent_engineer_repair_01.png
agent_developer_type_01.png
agent_signal_officer_scan_01.png
agent_cargo_bot_carry_01.png
```
