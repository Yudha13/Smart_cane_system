# Engineering Roadmap

| Phase | Scope | Exit criteria |
|---|---|---|
| 0 | Requirements and engineering validation | Architecture/requirements reviewed; assumptions, risks, RF compliance path, data flow, candidate BOM, and open questions approved by owner |
| 1 | Hardware design | Exact parts selected; datasheets verified; BOM, wiring, power, enclosure, installation plan approved |
| 2 | Raspberry Pi foundation | OS, storage, network, SSH, runtime, monitoring, boot and recovery tested on actual hardware |
| 3 | Weather station | Each sensor/interface tested; units and calibration checked against reference; fault behavior documented |
| 4 | LoRaWAN gateway | Regional plan verified; concentrator/service tested; gateway registered; reception evidence recorded |
| 5 | ESP32 soil nodes | Firmware, sensors, OTAA, payload, low-power, battery, radio tested on actual hardware |
| 6 | Local data infrastructure | MQTT/ingestion, schema, validation, persistence, device registry tested locally |
| 7 | Offline synchronization | Outbox, batch API, retries, idempotency, prolonged outage, restart and recovery tests pass |
| 8 | Private server | Central API, DB, authentication, ingestion, live updates validated |
| 9 | Dashboard | Overview, weather, soil, paddock, history, devices, alerts, gateway, sync views validated |
| 10 | Integration and field validation | End-to-end, stress, network, offline, power recovery, integrity, security, field tests pass |

## Dependencies
Phase 1 depends on Phase 0 approval. Phases 2–5 depend on verified hardware interfaces. Phase 6 depends on stable event/payload contracts. Phase 7 depends on durable local storage and central ingestion semantics. Phases 8–9 depend on approved API/data contracts. Phase 10 depends on all component gates.

Only Phase 0 review and documentation work are authorized. Production firmware, wiring, and deployment implementation have not started.
