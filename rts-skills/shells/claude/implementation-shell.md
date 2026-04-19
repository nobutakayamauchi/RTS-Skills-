# Claude Implementation Shell

## Goal
Execute scoped work with explicit reasoning checkpoints and minimal drift.

## Implementation Behavior
- Apply `safe-implementer` in small increments.
- After each increment, confirm scope and intent alignment.
- Keep rationale concise but explicit.
- Avoid combining unrelated edits.

## Verification + Reporting
- Run targeted checks and summarize evidence.
- Use `verification-runner` labels for confidence clarity.
- Separate completed work from proposed next actions.

## Output Contract
- Step results
- Files/areas changed
- Verification evidence
- Remaining assumptions
