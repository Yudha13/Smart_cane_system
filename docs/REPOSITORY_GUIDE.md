# Repository Guide

- `firmware/esp32-soil-node/`: ESP32 soil-node firmware. PlatformIO selected; framework validation pending.
- `hardware/raspberry-pi/`: field-node BOM, wiring, interfaces, power, enclosure.
- `hardware/esp32/`: node electronics, PCB, connectors, power, enclosure.
- `raspberry-pi/`: direct weather acquisition, gateway integration, local services, device health, synchronization.
- `server/`: central API, authentication, database, dashboard, deployment.
- `shared/`: versioned payload schemas, API contracts, units, identifiers, protocol definitions.
- `infrastructure/`: deployment, reverse proxy, monitoring, backups, operations.
- `tests/`: cross-component and system validation.
- `docs/`: engineering documentation and decision records.

Keep physical designs under `hardware/`, ESP32 source under `firmware/`, field software under `raspberry-pi/`, and central services under `server/`. Cross-component contracts belong in `shared/`. Avoid empty abstractions before requirements exist; `.gitkeep` preserves a planned directory but does not imply implementation.
