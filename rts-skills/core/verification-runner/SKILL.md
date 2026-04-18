# Title
Verification Runner

## Purpose
Validate outcomes and clearly separate verified, unverified, and assumed items.

## Use When
- Changes were made and require trustable reporting.
- Evidence quality must be explicit.

## Inputs
- Intended outcomes
- Available checks/tests
- Environment constraints

## Process
1. Run the highest-signal checks available.
2. Record what was actually verified.
3. Mark what could not be verified and why.
4. List assumptions still in play.
5. Report confidence boundaries.

## Output Format
- Verified
- Unverified
- Assumed
- Verification Gaps

## Guardrails
- Never present assumptions as facts.
- Include command or method used for each verification claim.

## Stop Conditions
- Verification status is explicit for all critical claims.
- Remaining risk is visible.

## Handoff Notes
Document next checks needed to raise confidence.
