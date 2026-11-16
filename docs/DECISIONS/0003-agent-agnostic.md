# ADR 0003: Tool-Agnostic AI Agent Instructions

- Status: Accepted
- Date: 2026-11-17
- Decision owner: Project owner

## Decision
Maintain project instructions in repository-owned Markdown files and keep them usable by Claude, ChatGPT, Codex, and other agents.

## Implementation
- `AGENTS.md` contains repository-wide operating rules.
- `docs/engineering/MASTER_SYSTEM_PROMPT.md` preserves the engineering mandate.
- `docs/engineering/AI_AGENT_GUIDE.md` explains source-of-truth and reporting requirements.

## Consequences
No provider-specific instruction file is authoritative. Provider-specific wrappers may be added later only if they point back to these canonical instructions and do not fork project requirements.
