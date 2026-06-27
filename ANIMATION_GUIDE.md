# Agent Mesh Animation Guide

Animations make Agent Mesh feel alive, but they must stay tied to real system state.

## Animation Philosophy

Animation should explain what is happening.

Bad:
- Agents wandering randomly with no task.
- Rooms flashing constantly for no reason.
- Heavy effects that slow down old machines.

Good:
- Agent walks to a room when assigned.
- Room pulses when a service is busy.
- Warning effect appears only when a real alert exists.
- Packet flow appears when network activity is happening.

## Performance Targets

- Keep loops short.
- Keep frame counts modest.
- Prefer CSS/SVG/canvas effects for simple UI motion.
- Use sprites for characters and complex effects.
- Make every animation optional or reducible.
- Support a low-power mode.

## Agent Animation States

### Idle

Used when the agent is available.

Visual:
- Small breathing/standing loop
- Minimal movement

### Walk / Move

Used when the agent is traveling to a station or room.

Visual:
- Basic walk cycle
- Directional or side-facing variants if needed

### Type

Used when writing code, commands, messages, or config.

Visual:
- Agent at console
- Subtle hand/terminal movement

### Repair

Used when restarting services, fixing errors, or running health checks.

Visual:
- Tool movement
- Sparks or wrench animation

### Carry

Used for file transfers, media movement, downloads/imports.

Visual:
- Agent/bot holding crate or data block

### Scan

Used by signal/recon agents.

Visual:
- Handheld scanner/radar pulse

### Alert

Used when blocked, failed, or responding to a warning.

Visual:
- Exclamation marker rendered by UI
- Red/yellow accent pulse

### Complete

Used briefly when a job finishes.

Visual:
- Short success pulse
- Then return to idle or next task

## Room Animation States

### Idle

Room is online and stable.

### Busy

Service is doing work.

Examples:
- Jellyfin scanning/transcoding
- Docker updating
- AI model running
- SnifferOps capturing

### Warning

Service needs attention but is not fully failed.

### Error

Service or task failed.

### Offline

Service or station unavailable.

### Updating

Service is being changed or restarted.

## Station Animation States

- Idle
- Busy
- Warning
- Error
- Offline
- Connecting
- Selected

Station animation should usually be subtle because many stations may appear at once.

## Timing Guidelines

- Idle loops: slow and subtle.
- Busy loops: noticeable but not distracting.
- Warning loops: visible but not painful.
- Error loops: stronger but still readable.
- Success effects: brief.

## Reduced Motion Mode

Agent Mesh should support a reduced-motion or potato mode.

In reduced motion:

- Replace loops with static state icons.
- Disable background particles.
- Disable large glow animations.
- Keep status indicators visible.

## Sprite Sheet Guidance

Start with simple sheets:

```text
idle: 2-4 frames
walk: 4-8 frames
work/type/repair: 4-8 frames
alert: 2-4 frames
complete: 2-4 frames
```

Do not overbuild animation before the functional UI is stable.
