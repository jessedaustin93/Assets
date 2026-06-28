# Agent Sprites

This folder holds character, bot, drone, and worker sprites.

Agents are visual representations of real AI helpers, automations, scripts, or task workers.

## Roles

Recommended role folders or filename subjects:

```text
engineer
developer
scientist
signal_officer
security_officer
cargo_bot
maintenance_bot
recon_drone
commander
```

## States

Recommended states:

```text
idle
walk
type
repair
carry
scan
alert
blocked
complete
return
```

## Naming Examples

```text
agent_engineer_idle_01.png
agent_engineer_walk_01.png
agent_developer_type_01.png
agent_signal_officer_scan_01.png
agent_cargo_bot_carry_01.png
agent_recon_drone_alert_01.png
```

## Design Notes

- Make silhouettes readable at small size.
- Use role-based accent colors.
- Keep sprites simple enough for low-end hardware.
- No text or logos.
- Prefer transparent backgrounds.
- Avoid random idle wandering in the app; movement should mean a real task is happening.
