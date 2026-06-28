# SnifferOps Radar Room

The SnifferOps Radar Room represents RF, Wi-Fi, BLE, SDR, sensor, and situational-awareness work.

This should feel like a tactical radar room, but the visuals should map to real detections and analysis.

## Purpose

Show signal-awareness status, new contacts, known contacts, scans, and analysis tasks.

## Visual Theme

- radar scope
- signal map
- antenna consoles
- packet analyzer terminal
- recon drone dock
- green/cyan scanning effects
- yellow for unknown/new contacts
- red for alert contacts

## Useful Telemetry

- capture status
- number of contacts
- new contacts
- known contacts
- signal strength/RSSI trends
- GPS availability
- packet/device counts
- sensor node status
- last scan time

## Room Objects

Suggested clickable objects:

```text
radar_screen
signal_map
packet_terminal
recon_drone_dock
contact_list_panel
sensor_status_console
```

## Common Commands

```text
Open SnifferOps
Start Scan
Stop Scan
View Contacts
Analyze New Contact
View Map
Export Capture
Assign Signal Officer
```

## Visual States

```text
idle       service ready but not actively scanning
busy       active capture or analysis
warning    sensor missing, GPS unavailable, unusual trend
alert      important new contact or watched contact
offline    service/sensor unavailable
error      scan failed or parser failed
```

## Asset Ideas

```text
room_snifferops_radar_idle_01.png
room_snifferops_radar_busy_01.png
room_snifferops_radar_alert_01.png
prop_radar_screen_active_01.png
effect_radar_sweep_loop_01.png
effect_new_contact_pulse_01.png
```

## Agent Usage

- Signal officer analyzes captures and contacts.
- Recon drone represents field sensors or ESP32 nodes.
- Scientist can help classify patterns.
- Engineer repairs broken capture services.

## Safety Notes

Agent Mesh should display metadata and awareness data responsibly.

Avoid presenting speculative identity claims as fact. Mark unknown contacts as unknown unless confirmed by data.
