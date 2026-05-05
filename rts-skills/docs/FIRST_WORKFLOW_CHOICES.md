# FIRST_WORKFLOW_CHOICES

Choose the smallest job-shaped workflow that matches intent.

## Confirmed facts
- Existing manifests already cover dev reporting, issue resolution, error analysis, revenue summaries, and communication summaries.
- A skill in this repository should represent a complete job unit, not low-level tool fragments.

## Assumptions
- New skills are needed when a recurring job cannot be expressed by current manifests.

## Unverified
- Current trigger usage frequency by workflow type across downstream runtimes.

## Minimal decision map
- If you need repository problem-to-fix flow, start from `issue_to_fix_pr.skill.yaml`.
- If you need periodic engineering summaries, start from `weekly_dev_report.skill.yaml`.
- If you need incoming-signal condensation, start from thread/mail summary manifests.
- If your task is social/content pipeline intake-to-output, use the additional manifests in this repo and keep scope declarative.

## Guardrail checks before adding a new manifest
1. Job-shaped scope is explicit.
2. No runtime implementation details are embedded.
3. Required packs are declared, not implemented.
4. outputs_to_rts is present.
5. Facts/assumptions/unverified can be reported clearly.
