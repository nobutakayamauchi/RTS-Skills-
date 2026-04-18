# Codex Implementation Shell

## Goal
Execute minimal, reversible code or content changes with clear traceability.

## Implementation Behavior
- Use `safe-implementer` as primary execution method.
- Stay inside locked scope and file boundaries.
- Make smallest viable change per task.
- Avoid opportunistic refactors.

## Verification + Reporting
- Run local checks tied to changed behavior.
- Use `verification-runner` for status labeling.
- Distinguish verified, unverified, and assumed items.

## Output Contract
- Files changed
- Why each change was made
- Checks run and outcomes
- Remaining uncertainty
