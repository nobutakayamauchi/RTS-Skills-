# AGENTS.md

## Scope
This file applies to the entire repository.

## Required reading
Before editing, read:

1. `README.md`
2. `docs/STATUS.md`
3. `docs/NEXT.md`

## Repository intent guardrails
- Keep this repository as the RTS reusable **job-shaped skill definition layer**.
- Do not add runtime implementations, connector implementations, or MCP pack internals here.
- Do not import full MCP pack bodies, Hermes drive internals, Talent Registry internals, or Signal Feed registry internals.
- Prefer minimal, additive edits over broad refactors.

## Inventory pass boundary
- Treat the next pass as inventory and classification, not implementation expansion.
- Prefer adding or improving index, inventory, and boundary documentation before changing skill definitions.
- Do not promote a skill to canonical status without a separate review decision.
- If a skill appears to belong in another repository, mark it as `MOVE` in inventory documentation instead of moving it immediately.

## Editing rules
- Do not overwrite existing canonical docs unless explicitly requested.
- When adding skills, follow existing manifest key style and keep entries concise.
- Keep outputs reconstructable and report facts/assumptions/unverified separately in documentation.

## Validation
- Check for broken local doc links when adding index or onboarding docs.
- For documentation-only changes, report changed files and confirm that no runtime, connector, registry, or orchestration implementation was added.
