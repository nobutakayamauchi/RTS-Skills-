# Title
Verification Runner

## Purpose
Validate outcomes and clearly separate verified, unverified, and assumed items.

## Use When
- Changes were made and require trustable reporting.
- Evidence quality must be explicit before handoff.

## Inputs
- Intended outcomes
- Available checks/tests
- Environment constraints

## Process
1. Run the highest-signal checks available.
2. Record only what was actually verified.
3. Mark what could not be verified and why.
4. List assumptions still in play.
5. State confidence boundaries and the next highest-signal check.

## Output Format
- Verified
- Unverified
- Assumed
- Verification Gaps
- Verification Log (required):
  - Workflow
  - Commands/Checks Run
  - Actual Outcome
  - Improvement Decision (`wording fix` | `sequence fix` | `output format fix` | `no change needed`)
  - Next Action

## Guardrails
- Never present assumptions as facts.
- Include command or method used for each verification claim.

## Stop Conditions
- Verification status is explicit for all critical claims.
- Remaining risk and next check are visible.

## Handoff Notes
Document next checks needed to raise confidence and who should run them.
