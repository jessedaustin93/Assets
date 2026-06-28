# Storage Room

The Storage Room represents disks, mounts, media libraries, backups, and storage health.

It should make capacity and risk visible at a glance.

## Purpose

Show storage usage, mount status, disk health, backup state, and media/library capacity.

## Visual Theme

- storage silos
- drive racks
- backup crates
- media shelves
- archive terminals
- green/blue healthy capacity
- yellow near-full or degraded
- red failed/missing disk

## Useful Telemetry

- disk free space
- mount status
- drive health if available
- backup status
- last backup time
- media library size
- failed mounts
- read/write errors

## Room Objects

Suggested clickable objects:

```text
storage_silo
drive_rack
backup_crates
mount_status_panel
archive_terminal
media_library_shelf
```

## Common Commands

```text
View Storage
Check Mounts
View Disk Usage
Check Backups
Open Media Folder
Run Backup Check
Assign Maintenance Bot
```

## Visual States

```text
idle       storage healthy
busy       backup, scan, copy, or import active
warning    disk near full, backup old, mount warning
error      failed disk, missing mount, backup failed
offline    storage unavailable
updating   migration/backup/update active
```

## Asset Ideas

```text
room_storage_room_idle_01.png
room_storage_room_warning_01.png
prop_storage_silo_idle_01.png
prop_drive_rack_warning_01.png
prop_backup_crates_idle_01.png
```

## Agent Usage

- Maintenance bot checks backups and space.
- Engineer fixes mounts and disk issues.
- Cargo bot moves media files.

## Safety Notes

Deletion, formatting, wiping, or backup rotation should require confirmation.
