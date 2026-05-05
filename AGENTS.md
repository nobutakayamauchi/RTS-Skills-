# AGENTS.md

## Scope
This file applies to the entire repository.

## Repository intent guardrails
- Keep this repository as the RTS reusable **job-shaped skill definition layer**.
- Do not add runtime implementations, connector implementations, or MCP pack internals here.
- Do not import full MCP pack bodies, Hermes drive internals, Talent Registry internals, or Signal Feed registry internals.
- Prefer minimal, additive edits over broad refactors.

## Editing rules
- Do not overwrite existing canonical docs unless explicitly requested.
- When adding skills, follow existing manifest key style and keep entries concise.
- Keep outputs reconstructable and report facts/assumptions/unverified separately in documentation.

## Validation
- Check for broken local doc links when adding index or onboarding docs.
