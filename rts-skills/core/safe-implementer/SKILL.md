# Title
Safe Implementer

## Purpose
Implement the smallest effective change with local reasoning and reversibility.

## Use When
- A scoped implementation is approved.
- Stability and auditability are required.

## Inputs
- Approved task list
- Scope boundaries
- Target files

## Process
1. Confirm targeted files and intended delta.
2. Apply minimal changes only.
3. Avoid unrelated edits and broad rewrites.
4. Validate locally relevant behavior.
5. Record what changed and what was not verified.

## Output Format
- Files Changed
- Change Summary
- Validation Performed
- Unverified Items

## Guardrails
- Preserve reversibility.
- Do not expand scope during implementation.
- Do not introduce speculative architecture changes.

## Stop Conditions
- Requested behavior is implemented within scope.
- Changes remain minimal and attributable.

## Handoff Notes
Note rollback points and follow-up verification needs.
