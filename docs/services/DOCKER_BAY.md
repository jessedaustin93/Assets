# Docker Bay

The Docker Bay represents container and compose-stack management.

It should make service health and container activity visible without becoming cluttered.

## Purpose

Show containers, compose stacks, updates, restarts, and unhealthy services.

## Visual Theme

- container racks
- deployment crane
- terminal wall
- status lights
- service bays
- blue/green healthy state
- orange activity/build state
- yellow warning
- red failed container

## Useful Telemetry

- running containers
- stopped containers
- restarting containers
- unhealthy containers
- image update status
- compose stack status
- CPU/RAM per container if available
- recent restart count

## Room Objects

Suggested clickable objects:

```text
container_rack
compose_stack_panel
deploy_crane
logs_terminal
image_cache_shelf
service_control_panel
```

## Common Commands

```text
View Containers
View Compose Stack
View Logs
Restart Container
Pull Images
Recreate Stack
Run Health Check
Assign Engineer
```

## Visual States

```text
idle       containers healthy and stable
busy       pulls, restarts, deploys, or logs active
warning    one or more containers degraded or restarting
error      critical container unhealthy or failed
offline    Docker unavailable
updating   image pull or recreate running
```

## Asset Ideas

```text
room_docker_bay_idle_01.png
room_docker_bay_busy_01.png
room_docker_bay_warning_01.png
prop_container_rack_idle_01.png
prop_deploy_crane_active_01.png
effect_service_restart_active_01.png
```

## Agent Usage

- Engineer restarts services and checks containers.
- Developer deploys app changes.
- Maintenance bot checks health and cleanup.

## Safety Notes

Confirm destructive actions before running them.

Examples include volume removal, container removal, large cleanup operations, and network changes.

Logs should be accessible before and after actions.
