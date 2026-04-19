# Bugfix Bundle

## Goal
Resolve a defect with controlled diagnosis, minimal fix surface, and explicit verification.

## Included Skills
- requirement-clarifier
- scope-locker
- systematic-debugger
- safe-implementer
- verification-runner
- change-recorder

## Recommended Execution Order
1. requirement-clarifier
2. scope-locker
3. systematic-debugger
4. safe-implementer
5. verification-runner
6. change-recorder

## Expected Outputs
- Bug objective and constraints
- Scoped debug boundary
- Escalation trigger and owner (when scope, risk, or confidence exceeds limits)
- Reproduction and root-cause notes
- Minimal fix summary
- Verified/unverified/assumed report with commands or checks used
- Change and risk record

## When Not to Use
- Net-new feature development.
- Broad refactors without a reproducible defect.
