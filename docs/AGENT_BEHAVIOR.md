# Agent Behavior Guide

Agents are visual workers tied to real AI helpers, automations, scripts, and tasks.

They should not just wander around to look alive. Their behavior should represent real state.

## Core Principle

If an agent appears busy, it should be doing real work or waiting on a real task state.

## Agent Lifecycle

```text
idle
  -> assigned
    -> traveling
      -> working
        -> complete / failed / blocked
          -> returning / idle
```

## Idle

Agent is available.

Visual:

- standing still
- very subtle idle loop
- no fake work

## Assigned

A task has been accepted but not started.

Visual:

- selection or assignment marker
- optional route preview

## Traveling

Agent is moving to the target station or room.

Visual:

- route line
- walk/shuttle movement
- destination marker

The backend should know the assignment exists before showing travel.

## Working

Agent is executing a real task.

Examples:

- running a command
- editing files
- reading logs
- restarting a service
- generating assets
- analyzing packets
- building code

Visual:

- typing
- repairing
- scanning
- carrying
- build animation

## Blocked

Agent cannot continue.

Reasons:

- needs user input
- missing permission
- command failed
- ambiguous instruction
- dependency missing
- rate limit or usage limit

Visual:

- yellow blocked state
- paused animation
- clear task card showing what is needed

## Complete

Task succeeded.

Visual:

- brief success pulse
- update room/station state
- agent returns to idle or next queued task

## Failed

Task failed.

Visual:

- red error state
- logs visible
- retry or inspect command available

## Permissions

Agents should have explicit permissions.

Examples:

```text
read_only
can_edit_files
can_run_commands
can_restart_services
can_access_secrets
can_modify_network
```

Visuals should not imply access that does not exist.

## Agent Roles

### Engineer

Works on Linux, Docker, system repair, services.

### Developer

Works on code, Git, tests, builds.

### Scientist

Works on models, prompts, research, analysis.

### Signal Officer

Works on SnifferOps, SDR, BLE/Wi-Fi, RF awareness.

### Security Officer

Works on vaults, auth, VPN, secrets, firewall status.

### Cargo Bot

Works on ARR stack, media imports, file movement.

### Maintenance Bot

Works on health checks, cleanup, scheduled jobs.

### Recon Drone

Works on sensors, ESP32 nodes, mobile/field telemetry.

## Do Not Fake It

Bad:

```text
Agent randomly repairs a healthy room for visual interest.
```

Good:

```text
Agent repairs Docker Bay because a container restart task is running.
```

## User Controls

Every active agent should support:

- inspect task
- view logs/transcript
- pause if possible
- stop if safe
- retry failed task
- reassign task

## Multi-Agent Behavior

Multiple agents can work at once, but the UI should avoid chaos.

Rules:

- group agents by station/room
- limit visible animation in low-power mode
- show queues clearly
- do not overlap important controls
