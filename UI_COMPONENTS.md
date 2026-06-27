# Agent Mesh UI Components

UI components are the tactical command interface pieces that make Agent Mesh useful.

The UI should feel like an RTS control surface, but it must stay readable and practical.

## Core UI Principles

- Function first.
- All controls must be obvious.
- Text is rendered by the app, not baked into images.
- UI should work with placeholder art.
- Fancy panels should not hide status or controls.
- Mobile and low-resolution screens should remain usable.

## Primary Components

### World Map Node

Represents a station, host, or node.

Needs:
- idle state
- selected state
- hover state
- warning state
- offline state
- status ring

### Station Card

Summary card for a machine.

Fields:
- station name
- role
- status
- CPU
- RAM
- disk
- GPU if available
- active agents
- alert count

### Room Tile

Clickable room/service representation.

Fields:
- room name rendered by app
- service status
- agent count
- task count
- warning/error indicator

### Agent Badge

Small representation of an agent.

Fields:
- name
- role
- status
- current task
- current location

### Selection Ring

RTS-style selected object indicator.

States:
- station selected
- room selected
- agent selected
- hostile/alert contact selected
- disabled/unavailable

### Command Menu

Right-click or action menu for selected object.

Station commands:
- open station
- SSH
- view logs
- assign agent
- restart service
- run health check

Room commands:
- open room
- view logs
- restart service
- open terminal
- assign agent
- clear alert

Agent commands:
- assign task
- pause
- resume
- stop
- view transcript
- return to base

### Terminal Panel

Embedded terminal/log window.

Needs:
- readable monospace area
- command output
- status header
- copy button
- clear button
- close/minimize

### Mission Panel

Task/job panel styled like an RTS objective card.

Fields:
- mission title
- description
- target station
- target room
- assigned agent
- progress
- logs
- success/failure state

### Resource Bars

Used for CPU, RAM, disk, GPU, VRAM, battery, network.

Rules:
- Never rely on color alone.
- Include text/number overlay rendered by app.
- Keep sizes consistent.

### Alert Banner

Visible warning system.

States:
- info
- warning
- error
- critical
- resolved

### Tooltip

Quick details on hover/tap.

Should support:
- station summary
- room summary
- agent status
- service status
- last seen / first seen for sensors

## Visual Asset Needs

- panel backgrounds
- panel corners
- button frames
- progress bar frames
- selection rings
- warning icons
- status dots
- connection lines
- minimap frame
- command cursor markers

## Naming Examples

```text
ui_panel_tactical_dark.png
ui_button_primary_idle.png
ui_button_primary_hover.png
ui_selection_ring_station.png
ui_status_dot_warning.png
ui_progress_bar_frame.png
ui_context_menu_frame.png
```
