# LoRaWAN Configuration

**Status:** No regional parameters or radio configuration approved.

## Candidate architecture
- ESP32 soil nodes use LoRaWAN Class A and OTAA.
- SX1262-based module is a candidate node radio.
- SX1302-based multi-channel concentrator is a candidate gateway radio.
- ChirpStack is the candidate network server; placement is unresolved.

## Regulatory blocker
Do not configure frequency plan, channels, transmit power, duty cycle, bandwidth, data rate, antenna gain, or EIRP until current Indonesian requirements and applicable equipment rules are verified from authoritative sources.

Do not assume EU868 or US915.

## Required validation
1. Confirm applicable Indonesian frequency allocation and technical limits.
2. Select an exact concentrator/module SKU and verify supported bands.
3. Confirm antenna, feeder, connector, mounting, and installation constraints.
4. Verify gateway packet forwarder / Basic Station support and software compatibility.
5. Test OTAA, uplink reception, payload decode, diagnostics, airtime, link budget, and node battery behavior.
6. Test operation during WAN outage according to the approved network-server topology.

Record exact software versions, region plan, channel settings, test location, and evidence before declaring this phase complete.
