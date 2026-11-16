# Raspberry Pi Setup

**Status:** Planning template only. No installation commands have been validated on project hardware.

## Target
Raspberry Pi 4B field node. Exact board/RAM and OS image must be confirmed.

## Planned work
- Verify board revision, RAM, power supply, SSD, cooling, and UPS.
- Select and verify Raspberry Pi OS Lite 64-bit image and release.
- Configure storage, filesystem, hostname, network, time synchronization, SSH keys, firewall, and unattended recovery.
- Install only approved runtime dependencies after service placement is decided.
- Configure monitoring, persistent logs, backups, and watchdog/recovery behavior.

## Acceptance evidence
Record OS image checksum/version, hardware inventory, boot/reboot results, storage health, network failover behavior, temperature under load, power interruption recovery, and restore test.

No production setup should be performed from this draft.
