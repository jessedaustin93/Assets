# Low-Power / Potato Mode

Agent Mesh should run on low-end hardware.

The interface can look good, but it must not require a gaming PC just to manage a homelab.

## Goal

Provide a reduced rendering mode that keeps all controls and status visible while disabling expensive visuals.

## Disable Or Reduce

In low-power mode:

- Disable background particles.
- Disable continuous glow animation.
- Disable unnecessary idle animations.
- Use static agent sprites.
- Lower telemetry refresh rate.
- Reduce shadows and blur.
- Reduce animated route effects.
- Use simpler selection outlines.
- Prefer CSS shapes over large image overlays.

## Keep Always Visible

Low-power mode must still show:

- station status
- room status
- active tasks
- alerts
- selected objects
- command menus
- logs/terminal panels
- agent assignment state

## Asset Requirements

Every major asset family should have a static fallback.

Examples:

```text
agent_engineer_idle_01.png
station_t5810_ai_flagship_idle_01.png
room_ai_core_idle_01.png
effect_warning_pulse_static_01.png
```

## Suggested Settings

```json
{
  "lowPowerMode": true,
  "enableParticles": false,
  "enableIdleAnimations": false,
  "enableGlowLoops": false,
  "telemetryRefreshMs": 5000,
  "maxAnimatedAgents": 3,
  "useStaticEffects": true
}
```

## Design Rule

If an asset only works because of animation, it is not readable enough.

The static version should communicate the basic meaning.
