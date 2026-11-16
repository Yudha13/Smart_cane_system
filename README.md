# SMART CANE SYSTEM

Modular, distributed, offline-first agricultural monitoring infrastructure for sugarcane plantations and other agricultural environments.

> **Status:** Phase 0 — requirements and engineering validation. Production firmware, wiring, and deployment implementation have not started.

## Objective
Collect soil and meteorological measurements across farms and paddocks, process and retain data locally, and synchronize reliably with a privately owned central server. Priorities: measurement integrity, offline operation, modularity, maintainability, electrical safety, and scalability.

## Baseline architecture
- **ESP32 soil nodes:** modular, independently identified devices; LoRaWAN Class A is the default telemetry mode.
- **Raspberry Pi 4B field node:** directly acquires weather measurements and hosts field-side services, local persistence, and synchronization. A separate ESP32 weather controller is not in the baseline.
- **Private server:** central API, database, authentication, dashboard, historical data, and monitoring.
- **Shared contracts:** versioned payload schemas and API contracts keep components consistent.

```text
ESP32 soil nodes -- LoRaWAN --> Raspberry Pi field node -- 4G/Wi-Fi --> Private server
                                      |                                |
                              Weather acquisition                Central API
                              LoRaWAN gateway                    PostgreSQL
                              Local MQTT                          Dashboard
                              Local persistence                   Auth & history
                              Transactional outbox
```

## Repository map
| Path | Responsibility |
|---|---|
| `firmware/` | ESP32 soil-node firmware (PlatformIO selected; framework to validate) |
| `hardware/` | Schematics, PCB, wiring, enclosure, power, BOM |
| `raspberry-pi/` | Weather acquisition, gateway host integration, local services, sync |
| `server/` | Private-server API, database, authentication, dashboard |
| `shared/` | Payload schemas, API contracts, protocol definitions |
| `infrastructure/` | Deployment templates, reverse proxy, monitoring, backups |
| `docs/` | Architecture, engineering decisions, risks, requirements, test plans |
| `tests/` | Unit, integration, offline, security, and field-validation tests |

See [Repository Guide](docs/REPOSITORY_GUIDE.md), [Project Status](docs/PROJECT_STATUS.md), and [Roadmap](docs/ROADMAP.md).

## Non-negotiable principles
1. Internet loss must not stop field acquisition or destroy accepted measurements.
2. Measurement persistence and creation of its sync record must be atomic (transactional outbox).
3. Every event has a unique `event_id`; central ingestion is idempotent.
4. Only acknowledged events become `SYNCED`; successful upload does not mean local data is deleted.
5. Internal timestamps use UTC; measurement units are explicit.
6. Hardware instructions require verified documentation for the exact part number.
7. Code completion is not evidence of hardware or field readiness.
8. Architecture changes require a recorded owner decision.

## Decisions recorded
- Repository model: modular monorepo.
- ESP32 tooling: PlatformIO selected; exact framework and board remain to be validated.
- AI-agent compatibility: tool-agnostic; instructions are in `AGENTS.md`.
- License: undecided. No public reuse or redistribution grant is made; see [License Status](docs/LICENSE-STATUS.md).

## Current status
- [x] Repository foundation and engineering guidance.
- [x] Initial architecture review and open-question register.
- [ ] Phase 0 approved by project owner.
- [ ] Exact hardware models and datasheets verified.
- [ ] Indonesian LoRaWAN regional parameters verified.
- [ ] Data contracts and database design approved.
- [ ] Phase 1 hardware design authorized.
- Production implementation: **not started**.

## Safety and security
Never commit credentials, private keys, production environment files, or sensitive deployment data. Do not expose the Raspberry Pi local database directly to the public internet. See [SECURITY.md](SECURITY.md).

## License
No license has been selected. Until an explicit license is added, do not assume that code or hardware designs may be reused, modified, or redistributed. See `docs/LICENSE-STATUS.md`.
