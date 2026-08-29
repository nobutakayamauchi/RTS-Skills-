# Title
Plain Knowledge Preparer

## Status
DRAFT / NON-CANONICAL

## Purpose
Prepare a reusable author-neutral and client-neutral knowledge profile from an existing workflow while preserving required correctness, safety, evidence, and recovery obligations.

## Use When
- A workflow works well but contains author-specific habits, terminology, thresholds, or preferences.
- A public tool needs a neutral starting profile before client-specific adaptation.
- A future paid adaptation should be produced as an overlay rather than a full fork.

## Inputs
- Source skill, bundle, or workflow definition
- Frozen human-important outcome
- Known author-specific tuning
- Required correctness and safety constraints
- Known external dependencies
- Known evidence and recovery requirements

## Process
1. Freeze the outcome that must survive personalization changes.
2. Inventory explicit and implicit knowledge assumptions in the source workflow.
3. Classify each assumption as reusable core, author-specific tuning, client-required input, external dependency, or unresolved.
4. Remove or generalize author-specific tuning without deleting required safety, evidence, verification, authority, or recovery behavior.
5. Replace client-specific values with explicit neutral fields or placeholders.
6. Record external systems as adapter requirements rather than embedding connector implementation.
7. Produce a removal/gap report so future operators can see exactly what changed.
8. Run a verification pass against the frozen outcome and report verified, unverified, assumed, and unknown items separately.

## Output Format
- `plain_profile`
- `removed_author_tuning`
- `required_client_inputs`
- `adapter_requirements`
- `unresolved_assumptions`
- `verification_notes`
- `execution_record` when RTS recording is available

## Guardrails
- Do not invent missing client knowledge.
- Do not call a profile neutral merely because names were deleted.
- Do not remove safety, evidence, recovery, or authority boundaries as "author preference" without proof.
- Do not add connector/runtime implementation to this skill.
- Prefer overlay-ready fields over client-specific forks.
- Keep the source workflow reconstructable.

## Stop Conditions
- The frozen outcome remains represented.
- Author-specific tuning is either removed, generalized, or explicitly retained with justification.
- Required client inputs are visible.
- Unknowns and conflicts are explicit.
- No runtime, credential, or connector implementation was introduced.

## Handoff Notes
Provide the source reference, what was generalized, what still needs client input, any adapter requirements, and the verification status. Promotion from DRAFT requires a separate review decision.
