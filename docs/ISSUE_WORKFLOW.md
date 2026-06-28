# Issue Workflow

GitHub issues can be used to track asset requests, prompt requests, cropping tasks, and documentation work.

## Issue Types

### Asset Request

Use for a new sprite, room, station, UI piece, effect, prop, icon, or background.

Template:

```text
.github/ISSUE_TEMPLATE/asset_request.md
```

### Prompt Request

Use for creating or improving a generation prompt.

Template:

```text
.github/ISSUE_TEMPLATE/prompt_request.md
```

### Crop Task

Use when a concept sheet needs to be cropped into runtime assets.

Template:

```text
.github/ISSUE_TEMPLATE/crop_task.md
```

### Documentation Task

Use when docs need to be added or updated.

Template:

```text
.github/ISSUE_TEMPLATE/documentation_task.md
```

## Suggested Labels

```text
asset-request
prompt-request
crop-task
documentation
metadata
station
room
agent
effect
ui
background
needs-review
ready
blocked
```

## Workflow

1. Create an issue.
2. Link relevant docs/prompts.
3. Generate or edit the asset/doc.
4. Commit files.
5. Update metadata if needed.
6. Close the issue when usable.

## Agent Usage

Claude, Codex, ChatGPT, or other agents should use issues to avoid losing task context.

Each issue should be specific enough that an agent can complete it without inventing structure.
