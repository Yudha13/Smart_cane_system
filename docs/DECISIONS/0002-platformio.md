# ADR 0002: ESP32 Development Environment

- Status: Accepted with framework validation pending
- Date: 2026-11-17
- Decision owner: Project owner

## Decision
Use PlatformIO as the ESP32 project environment.

## Not decided
This decision does not yet select ESP-IDF versus Arduino framework, an exact ESP32 board, toolchain versions, radio driver, or sensor libraries.

## Validation
Create a minimal non-production build only after exact board selection; verify toolchain support, debugging, library maintenance, radio driver compatibility, and test workflow before Phase 5 implementation.
