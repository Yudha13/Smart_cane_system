# Deployment Guide

**Status:** Not deployable. This is a future operational checklist, not a production procedure.

## Deployment prerequisites
- Phase 0 architecture and Phase 1 hardware design approved.
- Exact hardware inventory, firmware/software versions, and configuration recorded.
- RF configuration verified for Indonesia.
- Device credentials provisioned securely.
- TLS, firewall, SSH, database access controls, and secret storage reviewed.
- Backup, restore, retention, monitoring, and incident procedures tested.
- Offline synchronization acceptance tests passed.

## Rollout sequence
1. Bench validation of each hardware subsystem.
2. Controlled integration test with one gateway and one soil node.
3. Verify local weather acquisition and durable storage.
4. Disconnect WAN and verify continued acquisition and queueing.
5. Restore WAN and verify idempotent synchronization and acknowledgements.
6. Expand gradually while monitoring packet loss, battery, storage, thermal, and data quality.
7. Record field acceptance evidence before wider deployment.

Do not use this document as authorization to deploy.
