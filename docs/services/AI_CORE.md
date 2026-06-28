# AI Core Room

The AI Core represents local LLMs, model management, agent orchestration, and heavy AI workloads.

This room should feel like the brain/reactor of Agent Mesh, but it must show real model and resource status.

## Purpose

Show AI workload status, model activity, GPU/VRAM use, agent jobs, and model storage.

## Parent Station

Usually:

```text
T5810 - AI Flagship
```

## Visual Theme

- AI reactor core
- model racks
- holographic brain/data display
- GPU consoles
- agent terminals
- purple/blue AI glow
- orange heat/load glow when busy
- yellow warning when resource constrained
- red error when model/job fails

## Useful Telemetry

- active model
- loaded model size
- GPU utilization
- VRAM usage
- CPU/RAM usage
- inference/job queue
- active agents
- model load/unload state
- recent errors

## Room Objects

Suggested clickable objects:

```text
model_rack
gpu_core_console
agent_terminal_bank
job_queue_panel
memory_context_display
logs_terminal
```

## Common Commands

```text
Open AI Core
View Active Models
View GPU Status
View Agent Jobs
Open Logs
Load Model
Unload Model
Assign Scientist
Assign Developer
```

## Visual States

```text
idle       AI services healthy, no heavy workload
busy       model inference, coding task, or agent job active
warning    VRAM high, queue stuck, model slow, heat/resource warning
error      model failed, agent job failed, service crashed
offline    AI service unavailable
updating   model download/update or service restart active
```

## Asset Ideas

```text
room_ai_core_idle_01.png
room_ai_core_busy_01.png
room_ai_core_warning_01.png
prop_gpu_core_console_busy_01.png
prop_model_rack_idle_01.png
effect_gpu_core_glow_busy_01.png
```

## Agent Usage

- Scientist works on model/research/prompt tasks.
- Developer works on code and tests.
- Engineer fixes services and GPU/driver issues.

## Safety Notes

Do not expose API keys, tokens, or private model credentials in room overlays.
