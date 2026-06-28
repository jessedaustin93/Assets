# Build Lab

The Build Lab represents code builds, tests, local development, Git work, and deployment preparation.

It should make software work visible without hiding logs and command output.

## Purpose

Show current build/test jobs, repo state, agent work, and deployment readiness.

## Visual Theme

- code workbench
- build terminal
- test chamber
- artifact shelf
- Git branch display
- blue/cyan normal state
- orange build activity
- green success
- yellow blocked/warning
- red failed build/test

## Useful Telemetry

- current repo
- branch
- dirty working tree status
- current build/test job
- last build result
- test failures
- artifact output
- assigned developer agent
- recent commit or task summary

## Room Objects

Suggested clickable objects:

```text
build_terminal
test_console
git_panel
artifact_shelf
agent_workbench
logs_terminal
```

## Common Commands

```text
Open Repo
View Build Logs
Run Tests
Check Git Status
Open Terminal
View Artifacts
Assign Developer
Assign Scientist
```

## Visual States

```text
idle       no active build/test job
busy       build/test/code task running
warning    dirty tree, skipped tests, warnings
error      build or test failed
offline    repo/build service unavailable
complete   recent success pulse
blocked    waiting for input or dependency
```

## Asset Ideas

```text
room_build_lab_idle_01.png
room_build_lab_busy_01.png
room_build_lab_error_01.png
prop_build_terminal_active_01.png
prop_artifact_shelf_idle_01.png
agent_developer_type_01.png
```

## Agent Usage

- Developer builds, tests, and edits code.
- Scientist helps with reasoning, prompts, and analysis.
- Engineer fixes environment problems.

## Safety Notes

Do not auto-deploy destructive or system-changing code without a clear confirmation step.
