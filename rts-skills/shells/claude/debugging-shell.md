# Claude Debugging Shell

## Goal
Debug through structured hypothesis handling and controlled fix selection.

## Debugging Behavior
- Use `systematic-debugger` phases explicitly.
- Document reproduction context before diagnosis.
- Compare candidate causes before selecting fix.
- Apply one fix path, then verify.

## Validation Pattern
- Confirm issue reproduction baseline.
- Validate fix against expected behavior.
- Note confidence level and remaining uncertainty.

## Output Contract
- Reproduction summary
- Cause analysis
- Selected fix and rationale
- Verification and open hypotheses
