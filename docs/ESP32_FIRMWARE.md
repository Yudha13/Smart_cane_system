# ESP32 Firmware

**Status:** Development plan only; no production firmware exists.

## Tooling decision
PlatformIO selected by project owner. Framework choice (ESP-IDF or Arduino framework), exact board, toolchain versions, and radio/sensor drivers remain to be validated.

## Planned firmware modules
- Device identity and provisioning
- Sensor configuration and acquisition
- Sensor-specific calibration and quality checks
- Timestamp and sequence management
- Payload encoding with schema version
- LoRaWAN OTAA and Class A uplink scheduling
- Battery measurement and power management
- Diagnostics, watchdog, and fault recovery
- Optional local commissioning interface

## Required tests
Host/unit tests for payload and conversion logic; hardware-in-loop tests for sensor interfaces; radio/OTAA tests on the legal regional configuration; measured sleep/active current; brownout/restart behavior; and field link validation.

No GPIO allocation or driver implementation should be guessed before exact board and sensor models are selected.
