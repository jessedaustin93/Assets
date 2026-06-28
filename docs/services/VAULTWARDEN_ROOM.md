# Vaultwarden Vault Room

The Vaultwarden Vault represents password-vault service health and security status.

This room should be security-focused without exposing secrets.

## Purpose

Show vault service status, backups, sync health, and security alerts.

## Visual Theme

- vault door
- lock console
- security officer post
- backup archive shelves
- green/blue healthy state
- yellow warning state
- red critical state

## Useful Telemetry

- service status
- container health if applicable
- backup status
- last backup time
- certificate status if used
- sync status
- alert count
- disk/storage status

## Do Not Show By Default

```text
passwords
tokens
private keys
recovery codes
secret values
real .env contents
```

## Room Objects

Suggested clickable objects:

```text
vault_door
lock_console
backup_shelf
security_terminal
logs_terminal
service_control_panel
```

## Common Commands

```text
Open Vaultwarden
View Service Logs
Check Backup Status
Run Backup
Restart Service
Check Certificate
Assign Security Officer
```

## Visual States

```text
idle       service healthy
busy       backup/sync/check active
warning    backup old, cert warning, degraded status
error      service failed or backup failed
offline    service unreachable
locked     secure/normal locked visual
unlocked   only for intentionally opened/admin context
```

## Asset Ideas

```text
room_vaultwarden_vault_locked_01.png
room_vaultwarden_vault_warning_01.png
room_vaultwarden_vault_error_01.png
prop_vault_door_locked_01.png
prop_security_terminal_idle_01.png
```

## Agent Usage

- Security officer checks status and policies.
- Engineer fixes service/container issues.
- Maintenance bot can run backup checks.

## Security Notes

The room is allowed to show that secrets exist, but not the secrets themselves.

Dangerous actions require confirmation.
