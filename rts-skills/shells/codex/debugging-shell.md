# Codex Debugging Shell

## Goal
Debug with disciplined, narrow, and test-backed iterations.

## Debugging Behavior
- Start with `systematic-debugger`.
- Reproduce first; do not patch blindly.
- Narrow cause with targeted diagnostics.
- Apply one primary fix at a time.

## Validation Pattern
- Re-run reproduction steps.
- Run nearby regression checks.
- Record unresolved hypotheses separately.

## Output Contract
- Reproduction evidence
- Root cause statement
- Fix diff summary
- Verification + residual risk
