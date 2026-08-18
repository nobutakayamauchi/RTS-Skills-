# Plain Knowledge v0 — Ultimate Loop Decision Record

Status: PROVISIONAL / DRAFT CANDIDATE / HUMAN GATE REQUIRED

## /goal

Create the smallest reusable mechanism that can strip author-specific tuning from a workflow, expose missing client inputs, and prepare the workflow for later client-specific adaptation without creating a fork-per-client architecture.

## Frozen outcome

A future operator must be able to start from the public reusable workflow, obtain a neutral knowledge profile, add client-specific knowledge and adapter declarations, and preserve required correctness, safety, evidence, recovery, and reconstructability.

## Current discovery sweep

Existing RTS-Skills already separates reusable job logic (`core/`) from environment-specific execution (`shells/`) and uses manifests for job-level inputs/outputs.

No existing `plain`, `client_profile`, or overlay-specific skill was found in RTS-Skills during the current repository search.

Material existing constraint: repository AGENTS/STATUS/NEXT require inventory-first, minimal additive edits and prohibit runtime, connector, pack, registry, and orchestration implementations here.

## Loop 1 — Raison d'être Destroy

Candidates considered:

1. **Do nothing / document manually per customer** — rejected because every paid adaptation would repeat the same knowledge-separation work and create hidden operator knowledge.
2. **Fork the whole tool per customer** — rejected as the default because it multiplies maintenance, migration, security, and update burden.
3. **Build a new profile-generation runtime here** — rejected because RTS-Skills is explicitly not a runtime repository and the job can be defined without new machinery.
4. **Add one job-shaped preparation skill plus a profile contract** — survives. It expresses the reusable work while leaving execution and connector implementation elsewhere.

Decision: `COMPOSE / SMALL GLUE CONTRACT`, not a new runtime.

## Loop 2 — METEOR Crucible

The surviving design was attacked against these failure modes:

- deleting author tuning also deletes safety or correctness rules;
- a supposedly neutral profile silently contains author assumptions;
- unknown client facts are invented;
- adapter declarations grow into connector implementations;
- client customization creates permanent source forks;
- the public profile claims universal optimization without evidence.

Mitigations adopted:

- freeze the human-important outcome before stripping tuning;
- classify assumptions before removal;
- keep safety/evidence/recovery/authority rules unless proven optional;
- preserve `UNKNOWN` and conflicts explicitly;
- separate adapter declaration from adapter implementation;
- make client customization overlay-oriented;
- label v0 `DRAFT / NON-CANONICAL` until separate review.

Provisional result: `SURVIVE AS DRAFT`.

## Reality boundary

This change is documentation/skill-definition only. There is no runtime deployment surface in this repository for the new candidate.

Validation boundary is therefore:

- files exist on the feature branch;
- structure respects repository boundaries;
- manifest style is consistent with existing concise manifests;
- no runtime/connector/credential code is introduced;
- links and referenced paths are reviewable before merge.

`REPOSITORY TRANSITION != SEMANTIC PROMOTION`.

## Loop 3 — DARWIN / future challengers

The design intentionally keeps these occupants replaceable:

- the plain profile format;
- the client overlay format;
- adapter declarations;
- the shell/runtime that executes the preparation job.

A future simpler or more reliable profile format may partially or fully replace this v0. Client overlays should not become permanent forks merely because they were created first.

## Open blocker discovered

The repository currently carries an MIT license. MIT explicitly permits distribution, sublicensing, and sale of copies. That does not match the proposed Limit Development Public Use License model discussed for future public distribution.

This branch does **not** change the license. License migration is a separate Human Gate and should be resolved before representing this repository as covered by the new resale/support restrictions.

## Files added

- `docs/inventory/skills_inventory.md`
- `docs/contracts/plain_knowledge_profile_contract.md`
- `rts-skills/core/plain-knowledge-preparer/SKILL.md`
- `rts-skills/manifests/plain_knowledge_preparer.skill.yaml`
- `docs/decisions/PLAIN_KNOWLEDGE_V0.md`

## Human Gate

Before merge, decide:

1. whether `plain-knowledge-preparer` belongs in `core/` or a future dedicated knowledge-adaptation domain;
2. whether the initial contract is sufficient for a first dogfood run;
3. whether license migration should be a separate immediate /goal;
4. whether successful dogfood evidence is required before promotion from DRAFT.
