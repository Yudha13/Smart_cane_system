# Database Schema

**Status:** Conceptual entity inventory only; no migrations or production schema exist.

Candidate entities: `farms`, `paddocks`, `gateways`, `devices`, `sensor_configs`, `weather_readings`, `soil_readings`, `device_health`, `sync_queue`, `sync_logs`.

Each measurement preserves `event_id`, `device_id`, `farm_id`, optional `paddock_id`, event and receive timestamps, values, explicit units, quality/status, sequence where applicable, and schema version.

The measurement and outbox record commit in the same local transaction. Required sync states: `PENDING`, `SENDING`, `RETRY`, `SYNCED`. Central ingestion enforces uniqueness on `event_id`; duplicate delivery receives deterministic acknowledgement. Preserve event time separately from receive time.

Pending: local DB engine, central PostgreSQL version, TimescaleDB justification, partitioning/indexes, retention, backup, migrations, tenant isolation, access control.
