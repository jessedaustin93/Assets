# Room Telemetry Guide

Rooms should show meaningful live data for the service or project they represent.

Do not fill rooms with fake gauges. Every telemetry item should either connect to real data now or be marked as planned.

## General Room Telemetry

Most rooms can show:

- service status
- last check time
- active tasks
- assigned agents
- log shortcut
- restart/open/config controls
- warnings/errors

## Bridge

Shows station overview.

Useful telemetry:

- station status
- CPU/RAM/disk
- service count
- active agents
- alert count
- uptime
- network link status

## AI Core

Useful telemetry:

- active model
- GPU use
- VRAM use
- CPU use
- RAM use
- queue length
- active agent jobs
- model load/unload state

## GPU Reactor

Useful telemetry:

- GPU temperature
- GPU utilization
- VRAM use
- power draw if available
- active workloads

## Engineering

Useful telemetry:

- system updates available
- failed services
- recent restarts
- disk mounts
- package manager status
- health-check results

## Docker Bay

Useful telemetry:

- running containers
- stopped containers
- unhealthy containers
- restarting containers
- image update status
- compose stack status

## Jellyfin Theater

Useful telemetry:

- active streams
- transcodes
- library scan status
- users watching
- media storage usage
- recent errors

## ARR Cargo Office

Useful telemetry:

- wanted/missing count
- download queue
- failed downloads
- import queue
- indexer status
- disk free space

## Vaultwarden Vault

Useful telemetry:

- service status
- backup status
- login/security alerts
- sync status
- certificate status if used

Do not expose secret contents in the room UI.

## SnifferOps Radar Room

Useful telemetry:

- active capture state
- new contacts
- known contacts
- signal strength trends
- GPS availability
- packet/device counts
- alert contacts

## Communications Room

Useful telemetry:

- SSH sessions
- VPN/Tailscale status
- DNS status
- link latency
- network errors
- reachable hosts

## Storage Room

Useful telemetry:

- disk free space
- mount status
- SMART status if available
- backup status
- media library size
- warnings for near-full disks

## Build Lab

Useful telemetry:

- current build/test job
- last build result
- Git branch
- dirty working tree status
- test failures
- artifact output path

## Display Rule

Show the most important 3-5 metrics in the room view.

Put detailed logs and full metrics behind a click.
