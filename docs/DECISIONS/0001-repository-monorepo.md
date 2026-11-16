# ADR 0001: Modular Monorepo

- Status: Accepted
- Date: 2026-11-17
- Decision owner: Project owner

## Context
ESP32 firmware, Raspberry Pi field services, central server, and shared contracts must evolve together. Their data formats and interfaces are tightly coupled.

## Decision
Use one Git repository with clearly separated top-level directories for firmware, hardware, Raspberry Pi software, server software, shared contracts, infrastructure, tests, and documentation.

## Consequences
- Cross-component changes can be reviewed together.
- Shared schemas have one authoritative home.
- Subsystems retain independent boundaries and READMEs.
- Repository size and access boundaries may need reevaluation if the project grows substantially.
