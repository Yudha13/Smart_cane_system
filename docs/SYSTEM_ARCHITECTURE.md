# System Architecture

**Status:** Phase 0 draft; not a deployment specification.

## Components
### ESP32 soil nodes
Independent, uniquely identified nodes with configurable soil moisture, temperature, pH, and EC sensors. Include farm/paddock identity, measurement timestamp, sequence, battery and communication diagnostics where applicable, configurable interval, and low-power behavior. LoRaWAN Class A is default. Wi-Fi is for commissioning where justified.

### Raspberry Pi field node
Directly acquires weather measurements. Candidate interfaces: isolated RS485/Modbus RTU, protected pulse inputs, I2C, and external ADC/signal conditioning. Hosts field gateway integration, local messaging, durable storage, health monitoring, and synchronization. Pi has no native ADC. A simple LoRa radio is not an SX1302-class multi-channel gateway.

### Private server
Hosts central API, authentication/authorization, PostgreSQL candidate, history, dashboard, device management, and live updates. Actual server capacity and topology are unknown.

## Data flow
1. ESP32 samples configured soil sensors and creates a unique event.
2. LoRaWAN network infrastructure receives uplink and delivers decoded application data to field ingestion, subject to final topology.
3. Raspberry Pi directly acquires weather data.
4. Validate and commit measurement plus outbox event in one local transaction.
5. Sync worker sends batches over 4G LTE/Wi-Fi.
6. Central API validates and idempotently ingests by `event_id`.
7. Only acknowledged events become `SYNCED`; retention is a separate policy.

## Offline behavior
WAN loss must not stop local weather acquisition, local durable storage, or field data handling. Outbox survives service/device restarts. Retry uses bounded exponential backoff with jitter. Duplicate, delayed, and out-of-order delivery must be handled.

## Unresolved topology
ChirpStack placement is undecided. Hosting on Pi may improve local autonomy but adds resource/operational load. Central hosting may simplify field compute but risks local application processing during WAN loss unless a local buffering/forwarding design is proven. Decide through offline acceptance testing.

## Trust boundaries
Radio/network server; local services/database; WAN field-to-server transport; central API/database; administration/deployment. Local database must not be publicly exposed.
