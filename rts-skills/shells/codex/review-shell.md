# Codex Review Shell

## Goal
Produce concise, actionable change reviews with confidence boundaries.

## Review Behavior
- Use `verification-runner` and `change-recorder` outputs.
- Prioritize correctness, scope compliance, and reversibility.
- Highlight unverified claims and risk concentrations.

## Output Structure
- Scope compliance check
- Change quality assessment
- Verification status (verified/unverified/assumed)
- Follow-up actions

## Guardrails
- Do not treat unrun checks as passing.
- Flag ambiguous or irreversible changes.
