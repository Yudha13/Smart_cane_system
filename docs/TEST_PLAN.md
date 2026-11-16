# Test Plan

**Status:** Acceptance strategy draft. No tests have been executed; no hardware has been validated.

## Phase 0
Architecture and requirements reviewed; assumptions, risks, blockers, and owners recorded; hardware selection criteria and RF compliance path agreed.

## Hardware
Verify exact datasheets and electrical compatibility. Bench-test rails under idle/peak load, RS485, pulse conditioning, ADC accuracy, grounding, thermal behavior, enclosure, and sensor calibration against a reference.

## Firmware and radio
Unit-test drivers, conversions, payloads, and config validation. Verify device identity, sequence, battery, watchdog, sleep/active current, OTAA, regional configuration, packet loss, and link behavior on actual hardware.

## Offline/data integrity
Disconnect WAN; acquisition and local storage continue. Restart services and power-cycle with pending sync. Inject duplicates, delayed/out-of-order events, and timeout after central commit but before acknowledgement. Verify only acknowledged records become SYNCED and no data is silently lost. Test backup restoration and retention.

## Security and field
Test authentication, authorization, TLS, secret handling, firewall, database exposure, and dependency hygiene. Conduct field soak tests across representative conditions.

PASS requires procedure, expected result, observed result, and evidence. Planned, mocked, and simulated tests must be labelled as such.
