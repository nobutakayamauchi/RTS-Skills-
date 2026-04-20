# Title
Verification Runner

## Purpose
Validate outcomes and clearly separate verified, unverified, and assumed items.

## Use When
- Changes were made and require trustable reporting.
- Evidence quality must be explicit.

## Inputs
- Intended outcomes
- Scope boundaries
- Available checks/tests
- Environment constraints

## Process
1. Run the highest-signal checks available.
2. Record scope verification (what stayed within approved boundaries).
3. Record content verification (what behavior/output was actually validated).
4. Attach method/evidence for each verification claim (command, test, review method).
5. Mark what could not be verified and why, then list assumptions.
6. Report confidence boundaries.

## Output Format
- Verified (Scope)
- Verified (Content)
- Evidence Method
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
