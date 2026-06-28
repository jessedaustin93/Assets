# Security Boundaries

Agent Mesh should make control easier without making the homelab reckless.

Visuals should never imply that an action is safe just because it looks cool.

## Core Rule

Dangerous actions require clear confirmation and obvious logs.

## Sensitive Areas

Treat these as sensitive:

- password vaults
- SSH keys
- API keys
- tokens
- VPN settings
- firewall rules
- DNS infrastructure
- backups
- delete operations
- service credentials
- production containers

## Vaultwarden / Secret Handling

The UI may show vault status, but should not display secret contents by default.

Allowed in normal room view:

- service online/offline
- backup status
- sync status
- alerts
- certificate status

Not allowed in normal room view:

- passwords
- tokens
- recovery keys
- private keys
- raw secret values

## Confirm Before Dangerous Actions

Require confirmation for:

- deleting files
- deleting assets
- deleting containers
- clearing volumes
- changing firewall/VPN rules
- rotating keys
- wiping backups
- exposing services externally
- changing authentication settings

## Permission Levels

Suggested agent permissions:

```text
read_only
can_edit_assets
can_edit_code
can_run_safe_commands
can_restart_services
can_modify_network
can_access_secrets
can_delete_data
```

Agents should start with the lowest permission needed.

## Logs

Important actions should produce logs:

- who/what requested it
- target station/room
- command/action
- result
- timestamp
- error output if failed

## UI Safety

- Dangerous buttons should not be next to common safe buttons without separation.
- Error and warning states should be obvious.
- Confirmation dialogs should state the actual effect.
- Do not hide shell output from destructive commands.

## Asset Repository Safety

This repo should not store:

- passwords
- API keys
- private SSH keys
- `.env` files with real secrets
- private certificates
- tokens

It can store:

- public docs
- prompts
- generated assets
- placeholder metadata
- example manifests with fake values

## Remote Control Rule

If Agent Mesh controls real machines over SSH/API, the UI should make the target clear before running commands.

Example confirmation:

```text
Restart Jellyfin on T3610?
Target: t3610
Service: jellyfin
Action: restart service
```

## Development Rule

When in doubt, make it visible, logged, and confirmable.
