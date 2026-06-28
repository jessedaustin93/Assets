# Drill-Down Navigation

Agent Mesh navigation should feel like zooming through an RTS command interface.

Each layer should reveal more detail without losing the path back out.

## Primary Hierarchy

```text
World Map
  -> Station / Host
    -> Room / Service
      -> Object / Tool
        -> Agent / Task
          -> Terminal / Logs / Controls
```

## World Map

Purpose:

Show all major machines, nodes, and environments.

Objects:

- T5810 AI Flagship
- T3610 Media and Infrastructure Station
- Pi 5 Sensor Outpost
- HP Automation Node
- Chromebook Kiosk
- ESP32 Recon Nodes
- Future cloud/VPS nodes

World map should answer:

- What is online?
- What needs attention?
- Where are agents working?
- What stations have active tasks?

## Station View

Purpose:

Show one machine and its rooms/services.

Station view should answer:

- What services are running here?
- What resources are under load?
- What agents are present?
- What rooms need attention?

## Room View

Purpose:

Show one service/project/control zone.

Room view should answer:

- Is the service healthy?
- What is it doing?
- What controls are available?
- What logs matter?
- Which agents are assigned?

## Object / Tool View

Purpose:

Inspect a specific terminal, server rack, radar screen, vault door, task board, or other room object.

Examples:

- Docker container rack
- Jellyfin transcode screen
- SnifferOps radar panel
- Vaultwarden lock console
- Terminal wall panel

## Agent / Task View

Purpose:

Inspect one worker or one task.

Show:

- current instruction
- progress
- output/logs
- blockers
- controls

## Terminal / Logs View

Purpose:

Deepest practical layer.

Show:

- SSH session
- service logs
- container logs
- command queue
- build output
- agent transcript

## Breadcrumbs

Always show the current path.

Example:

```text
World > T3610 > Docker Bay > Container Rack > Jellyfin Logs
```

## Back Behavior

Back should move up one layer.

Do not dump the user back to the world map unless they choose home.

## Visual Transition Rules

- Transitions can zoom or slide, but must stay fast.
- Reduced-motion mode should use instant transitions.
- Never delay controls for decorative animation.

## Deep Link Idea

Eventually, every object should have a route-like identity.

Example:

```text
/world/t3610/docker_bay/jellyfin/logs
```

This makes it easier for agents and users to open exact screens.
