# Station Sprites

This folder holds world-map sprites for machines, hosts, nodes, and stations.

Stations are the top-level RTS map objects in Agent Mesh.

## Subjects

Recommended subjects:

```text
t5810_ai_flagship
t3610_media_station
pi5_sensor_outpost
hp_automation_node
chromebook_kiosk
esp32_recon_node
cloud_relay
backup_station
generic_station
```

## States

Recommended states:

```text
idle
busy
warning
error
offline
selected
hover
connecting
updating
```

## Naming Examples

```text
station_t5810_ai_flagship_idle_01.png
station_t3610_media_station_warning_01.png
station_pi5_sensor_outpost_busy_01.png
station_esp32_recon_node_idle_01.png
station_generic_offline_01.png
```

## Design Notes

- Make each machine type visually distinct.
- Keep icons readable on the world map.
- Leave room for app-rendered status rings and labels.
- No baked names or labels.
- Use selected/hover overlays when possible instead of separate full sprites.
