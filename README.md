# RTS-Skills

Public repository for reusable, AI-agnostic, job-shaped operational skills.

## Repository role

This repository is the **public baseline and distribution surface** for intentionally open skill definitions, documentation, inventory, examples, and reviewed exports.

It is **not** the canonical target for new proprietary/paid skill development. New copy-sensitive skills, paid bundles, private evaluation assets, unreleased prompts, and proprietary extensions belong in `nobutakayamauchi/RTS-Skills-Core`.

## Start here

1. Read `AGENTS.md` for the AI/public-private boundary.
2. Read `rts-skills/README.md` for the primary workflow guide.
3. For a guided first run, use `rts-skills/docs/START_HERE.md`.
4. Continue with `rts-skills/docs/NEXT_STEPS.md` after one successful run.

## Repository layout

- `rts-skills/core/` — reusable public execution skills
- `rts-skills/shells/` — environment-specific wrappers
- `rts-skills/bundles/` — public multi-skill sequences
- `rts-skills/growth/`, `rts-skills/media/` — domain extensions

## Hard boundary

```text
PUBLIC BASELINE != PRIVATE CANONICAL DEVELOPMENT
```

Do not mirror the private Core repository into this public repository. Public export must be deliberate and reviewed.