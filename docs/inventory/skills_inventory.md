# RTS Skills Inventory

Status: INITIAL INVENTORY / NON-CANONICAL

Purpose: satisfy the repository inventory-first boundary before adding new reusable skill definitions.

## Core skills

| name | path | purpose | status | expected output | adjacent relation | next safe action |
|---|---|---|---|---|---|---|
| change-recorder | `rts-skills/core/change-recorder/` | record material changes | READY | reconstructable change record | RTS records | preserve |
| handoff-writer | `rts-skills/core/handoff-writer/` | prepare operator handoff | READY | handoff artifact | operator/runtime neutral | preserve |
| requirement-clarifier | `rts-skills/core/requirement-clarifier/` | clarify ambiguous requirements | READY | clarified requirement set | upstream of implementation | preserve |
| safe-implementer | `rts-skills/core/safe-implementer/` | bounded implementation workflow | READY | implementation + report | runtime executes elsewhere | preserve |
| scope-locker | `rts-skills/core/scope-locker/` | freeze scope and non-goals | READY | frozen scope | compatible with Ultimate Loop workload freeze | preserve |
| skill-builder | `rts-skills/core/skill-builder/` | define reusable job-shaped skills | READY | skill definition | this repository | preserve |
| systematic-debugger | `rts-skills/core/systematic-debugger/` | structured debugging | READY | root-cause/debug report | runtime evidence elsewhere | preserve |
| task-decomposer | `rts-skills/core/task-decomposer/` | decompose bounded work | READY | task plan | runtime neutral | preserve |
| verification-runner | `rts-skills/core/verification-runner/` | separate verified/unverified/assumed results | READY | verification report | evidence sources external | preserve |

## Bundles

| name | path | purpose | status | next safe action |
|---|---|---|---|---|
| bugfix | `rts-skills/bundles/bugfix.md` | reusable bug-fix sequence | READY | preserve |
| content-pipeline | `rts-skills/bundles/content-pipeline.md` | content workflow sequence | DRAFT | review boundaries |
| feature-build | `rts-skills/bundles/feature-build.md` | scoped feature sequence | READY | preserve |
| refactor | `rts-skills/bundles/refactor.md` | bounded refactor sequence | READY | preserve |

## Shells

| environment | path | purpose | status | next safe action |
|---|---|---|---|---|
| Claude | `rts-skills/shells/claude/` | environment-specific execution wrapper | READY | keep model-specific behavior here |
| Codex | `rts-skills/shells/codex/` | environment-specific execution wrapper | READY | keep model-specific behavior here |

## Manifest shelf

`rts-skills/manifests/` contains job-level manifests for reusable workflows including repository intake, issue-to-fix, build failure analysis, mail triage, revenue reporting, knowledge retrieval, Sentry analysis, content repurposing, signal-to-social ideas, price watching, and skill promotion review.

Classification of every manifest remains a follow-up inventory task. No manifest is promoted to new canonical status by this document.

## New candidate opened by /goal

Candidate: `plain-knowledge-preparer`

Proposed role: produce an author-neutral/client-neutral knowledge template and a removal/gap report from a reusable workflow without adding runtime, connector, credential, or orchestration behavior.

Initial classification: `DRAFT` until separate review.
