# Room Sprites

This folder holds room/interior sprites for station drill-down views.

Rooms represent real services, projects, or functional zones.

## Subjects

Recommended room subjects:

```text
bridge
ai_core
engineering
docker_bay
jellyfin_theater
arr_cargo_office
vaultwarden_vault
snifferops_radar
communications
storage_room
build_lab
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
locked
unlocked
updating
alert
```

## Naming Examples

```text
room_ai_core_idle_01.png
room_docker_bay_busy_01.png
room_jellyfin_theater_warning_01.png
room_vaultwarden_vault_locked_01.png
room_snifferops_radar_alert_01.png
```

## Design Notes

- Leave open space for agents.
- Keep clickable objects visually obvious.
- Do not bake labels into the room art.
- Keep room background, props, and UI overlay separate where practical.
- Each room should communicate its function from shape and props.
