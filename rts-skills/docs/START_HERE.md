# START_HERE

A minimal first-run path for RTS-Skills.

## Confirmed facts
- This repository is the job-shaped skill definition layer, not a runtime or raw tool-call layer.
- Existing manifests in `rts-skills/manifests/` define reusable units with inputs/outputs and required packs.

## Assumptions
- The operator already has an execution environment capable of running skill workflows.
- The operator can map required packs to their runtime environment outside this repository.

## Unverified
- Whether every environment-specific shell currently available downstream supports every manifest in this repo.

## First run
1. Read `docs/overview/POSITION.md` to confirm boundary and non-responsibility.
2. Read `rts-skills/README.md` for layer model and safe extension rules.
3. Pick one existing manifest from `rts-skills/manifests/` and validate it as a job-shaped unit:
   - clear purpose
   - required packs declared
   - inputs/outputs explicit
   - outputs_to_rts explicit
4. If adding a new skill, follow existing manifest structure and keep scope minimal.
5. Record outcomes as confirmed facts, assumptions, and unverified items.
