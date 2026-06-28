# Effect Sprites

This folder holds visual effects for real Agent Mesh activity.

Effects should explain what is happening without hiding the controls.

## Subjects

Recommended effect subjects:

```text
ssh_beam
deploy_beam
packet_flow
radar_sweep
new_contact_pulse
warning_pulse
error_pulse
success_pulse
gpu_core_glow
cpu_heat_glow
storage_fill
construction_update
service_restart
```

## States

Recommended states:

```text
connecting
active
failed
complete
warning
error
critical
normal
busy
loop
start
end
```

## Naming Examples

```text
effect_ssh_beam_connecting_01.png
effect_deploy_beam_active_01.png
effect_packet_flow_normal_01.png
effect_radar_sweep_loop_01.png
effect_warning_pulse_red_01.png
```

## Design Notes

- Keep effects reusable as overlays.
- Prefer transparent backgrounds.
- Keep frame counts modest.
- Make effects optional for low-power mode.
- Effects should map to real events, tasks, alerts, or telemetry.
