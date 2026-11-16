# Instructions for AI Agents

This repository is tool-agnostic. These rules apply to ChatGPT, Claude, Codex, and other engineering agents.

## Before making changes
1. Read this file, `README.md`, `docs/PROJECT_STATUS.md`, relevant architecture documents, and latest decision records.
2. Inspect the current repository tree and exact files to be changed.
3. Identify the active phase and its acceptance criteria. Do not skip dependencies.
4. Separate facts into **CONFIRMED**, **RECOMMENDED**, **ASSUMPTION**, **NEEDS VERIFICATION**, and **BLOCKER**.
5. Ask focused questions when missing information could change hardware, safety, data integrity, cost, or compatibility.

## Engineering rules
- Do not begin production implementation until the owner approves the relevant phase.
- Do not silently change the approved architecture.
- Never invent datasheet values, pinouts, register addresses, calibration factors, prices, availability, legal compliance, or test results.
- Verify exact manufacturer and part number before model-specific wiring instructions.
- Raspberry Pi directly acquires weather measurements in the baseline; do not add an ESP32 weather controller without approval.
- A simple LoRa transceiver is not a multi-channel LoRaWAN gateway.
- Do not assume EU868 or US915 is legal or suitable in Indonesia. Verify current Indonesian rules before RF configuration.
- Keep field acquisition and durable storage operating during internet outages.
- Measurement and outbox event must commit in one local database transaction.
- Central ingestion must be idempotent. Mark events synced only after acknowledgement.
- Retain local records according to a separate policy; never delete merely because upload succeeded.
- Use UTC internally and explicit units in schemas.
- Never commit credentials, secrets, private keys, or real production `.env` files.
- Do not expose the Raspberry Pi local database directly to the public internet.
- Preserve working functionality; back up before risky changes.

## Change and test workflow
1. State objective, scope, assumptions, and risks.
2. Make the smallest coherent change.
3. Run relevant formatting, static checks, unit/integration tests, and security checks where available.
4. Report exact commands and actual outcomes. Distinguish not-run from passed.
5. Update documentation and `CHANGELOG.md` when behavior, interfaces, architecture, or operations change.
6. Provide rollback steps for risky changes.
7. Do not mark a phase complete without evidence against every acceptance criterion.

## Required report
Objective; files changed; technical decisions; commands and observed test results; risks/blockers; documentation updates; acceptance status.
