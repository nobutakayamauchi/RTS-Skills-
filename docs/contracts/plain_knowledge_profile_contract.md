# Plain Knowledge Profile Contract

Status: DRAFT / NON-CANONICAL

## Purpose

Define a reusable boundary for turning an author-tuned workflow into a neutral starting profile that can later receive a client-specific overlay.

This repository defines the job-shaped contract only. It does not implement a runtime, connector, credential store, or always-on assembler.

## Layer model

```text
REUSABLE CORE
+ PLAIN KNOWLEDGE PROFILE
+ OPTIONAL CLIENT OVERLAY
+ OPTIONAL ADAPTER DECLARATIONS
= DEPLOYABLE CONFIGURATION (assembled elsewhere)
```

The public reusable core must not depend on one author's private habits in order to remain understandable.

## Plain profile requirements

A `plain` profile MUST:

- preserve the workflow's human-important outcome;
- preserve required safety, evidence, verification, recovery, and stop conditions;
- expose assumptions that must be supplied by a future operator or client;
- use neutral placeholders for organization-specific vocabulary, thresholds, destinations, and decision rules;
- contain no credentials, secrets, personal data, or client-confidential material;
- contain no hidden author-only knowledge required for basic reconstruction;
- avoid hard-coding a specific external provider unless the provider itself is part of the frozen requirement;
- distinguish facts, defaults, assumptions, and unresolved items.

A `plain` profile MUST NOT claim to be optimized for every user. It is a neutral starting point, not a universal best configuration.

## Client overlay fields

A client overlay may supply:

- business objective and success conditions;
- domain vocabulary and canonical terms;
- decision thresholds and tolerances;
- speed/quality/cost trade-off preferences;
- prohibited actions and escalation boundaries;
- evidence requirements;
- approval and authority boundaries;
- preferred output style and delivery surface;
- known failure patterns;
- required external systems and adapter declarations;
- maintenance and revalidation expectations.

## Separation rules

1. `CORE != CLIENT KNOWLEDGE`.
2. `PLAIN != AUTHOR CUSTOM`.
3. `CLIENT OVERLAY != CONNECTOR IMPLEMENTATION`.
4. `ADAPTER DECLARATION != ADAPTER CODE`.
5. Removing author-specific tuning MUST NOT remove required safety or evidence obligations.
6. If a supposedly author-specific rule is necessary for correctness, it belongs in the reusable core or must be explicitly marked as a required input.
7. Unknown client facts stay `UNKNOWN`; they are never invented to make a profile look complete.

## Output contract

A plain-profile preparation job should return:

- `plain_profile` — neutral reusable knowledge/configuration template;
- `removed_author_tuning` — what was deliberately removed or generalized;
- `required_client_inputs` — fields needed before client optimization;
- `adapter_requirements` — declarations only, with implementation location left external;
- `unresolved_assumptions` — material unknowns or conflicts;
- `verification_notes` — checks showing required behavior was not accidentally removed;
- `execution_record` — reconstructable summary for RTS when applicable.

## Commercial boundary note

This contract supports the product model "the tool is public; adaptation is a separate service" but does not itself define licensing terms or commercial permissions.

Before commercial distribution, repository licensing must be reviewed separately.
