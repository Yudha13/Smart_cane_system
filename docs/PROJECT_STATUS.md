# Project Status

**Status date:** 2026-11-17  
**Current phase:** Phase 0 — requirements and engineering validation  
**Production implementation:** Not started  
**Phase 0 approval:** Pending owner review

## CONFIRMED
- Agricultural monitoring across farms and paddocks.
- Raspberry Pi 4B field node directly acquires weather measurements.
- ESP32 devices are distributed soil sensor nodes.
- LoRaWAN is primary soil-node telemetry; Class A is default.
- A privately owned server is the central infrastructure.
- Field acquisition and storage must continue without internet.
- Transactional outbox, idempotent ingestion, unique event identity, UTC timestamps, and explicit units are mandatory.

## Owner decisions
- Modular monorepo.
- PlatformIO selected for ESP32 development; framework and board support require validation.
- AI-agent compatibility is tool-agnostic.
- License undecided; no LICENSE file is issued.

## NEEDS VERIFICATION
- Exact Raspberry Pi revision/RAM, OS image, SSD, power, cooling, UPS.
- Exact SX1302 concentrator and Pi interface.
- Weather sensor models, output interfaces, and mounting.
- ESP32 board, SX1262 module, probes, battery, charger, enclosure.
- Indonesian LoRaWAN regional plan and regulatory compliance.
- ChirpStack placement and offline topology.
- Local database/MQTT sizing.
- Private server OS, capacity, network, backups, and exposure model.
- Node count, sampling intervals, retention, and latency objectives.

## Gate
Phase 1 hardware design must not begin until Phase 0 requirements, component criteria, RF constraints, and architecture decisions are reviewed and approved.
