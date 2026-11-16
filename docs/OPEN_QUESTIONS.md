# Open Questions and Blockers

## Site and scale
1. Number of farms, paddocks, gateways, weather stations, and soil nodes initially and at scale?
2. Field distances, terrain, vegetation, and gateway mounting heights?
3. Available internet and expected outage duration?
4. Environmental exposure, enclosure, and maintenance access requirements?

## Measurements
5. Which weather parameters are mandatory for the first station?
6. Accuracy, sampling/reporting interval, and calibration approach per sensor?
7. Which soil measurements and existing probe models are available?
8. Required units, quality flags, and acceptable ranges?

## Hardware and power
9. Confirm exact Raspberry Pi board/RAM and power supply.
10. Is an SX1302 concentrator already owned? Provide manufacturer and exact SKU.
11. Which weather sensors, RS485 adapters, LTE modem, RTC, UPS, or enclosure are already owned?
12. Preferred ESP32 board/module or SX1262 radio?
13. Battery/solar autonomy target for remote nodes?

## Network/compliance
14. Expected node count and radio reporting frequency?
15. What process/source will be used to verify current Indonesian RF requirements?
16. Must LoRaWAN network/application services continue locally without WAN for days, or is gateway buffering sufficient?

## Server/operations
17. Private server OS, CPU/RAM/storage, network reachability, and backup capability?
18. Domain name and TLS termination available?
19. Required user roles and authentication?
20. Data retention, backup RPO, recovery RTO, and dashboard latency?

## Design blockers
- RF regional configuration.
- Exact sensor models and electrical interfaces.
- Network-server placement and offline operation model.
- Expected scale and measurement intervals.
- Power/autonomy requirements.
- Private-server deployment constraints.
