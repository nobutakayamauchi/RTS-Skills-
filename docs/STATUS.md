# RTS-Skills Status

Status: PARTS / SKILLS / INVENTORY NEEDED

RTS-Skills is the reusable job-shaped skill definition layer for the RTS ecosystem.

It is a component shelf, not RTS core.

It is not RTS-AGE.

It is not an MCP pack implementation repository.

It is not a runtime execution engine.

## Current Position

This repository should hold reusable operational skill definitions, skill shells, wrappers, bundles, and related documentation that can be used by operators or future agent environments.

Allowed by default:

- document skill definitions
- add concise skill manifests
- improve skill indexing
- clarify wrapper boundaries
- organize bundles and examples
- preserve reconstructable output expectations
- separate facts, assumptions, unverified material, and risks in documentation

Prohibited by default:

- adding full runtime implementations
- adding connector internals
- adding MCP pack internals
- importing Hermes Drive internals
- importing Talent Registry internals
- importing Signal Feed registry internals
- turning this repository into RTS core
- turning this repository into RTS-AGE
- broad refactors without an inventory decision

## Boundary

RTS defines the protocol.

RTS-AGE may execute or prepare implementation artifacts.

RTS-MCP-Packs may hold connector pack definitions.

RTS-Hermes-Drive may hold orchestration bridge material.

RTS-Skills should remain the reusable skill definition layer.

## Minimum Alive Definition

This repository is considered Minimum Alive when:

1. Its role as a skill definition shelf is explicit.
2. Its boundaries from runtime, connector, and orchestration repositories are clear.
3. Its next inventory pass is documented.
4. Existing AGENTS.md guardrails are preserved.
5. No runtime behavior is changed by the rescue documentation itself.

## Current Decision

Keep this repository.

Treat it as a parts shelf for reusable RTS operational skills.

Do not expand it into runtime, connector, registry, or orchestration implementation without a separate decision record.
