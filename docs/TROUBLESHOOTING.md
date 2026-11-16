# Troubleshooting

Diagnostic guidance only; no fixes here are claimed as field-tested.

## Missing dashboard data
Check sensor acquisition; gateway/network-server receive path; local persistence/outbox; WAN and sync worker; central API validation/idempotency/commit; event and receive timestamps; schema version.

## Duplicate events
Inspect `event_id`, sequence, retry logs, and central uniqueness constraint. Duplicate delivery must not create duplicate measurements.

## LoRaWAN node not received
Verify activation, credentials, antenna, gateway health, regional configuration, and correlated logs. Do not change RF settings without verifying Indonesian requirements.

## Weather sensor communication failure
Verify supply, exact interface, polarity, bus termination, baud/parity, register map, and isolation. Never guess register addresses or connect unknown signal levels to GPIO.

## Power/reboot problems
Capture rail voltage under load, modem transmit peaks, storage behavior, UPS state, and boot logs before changing hardware.
