# Start Here

## What this page is for
This page helps first-time users decide what to open first and which minimal workflow to run first.

## Start here if...
- **You want to understand the repository purpose:** start with `README.md`.
- **You want to make a small Codex change:** start with `docs/QUICKSTART_EXAMPLE_CODEX.md`.
- **You want to plan before execution with Claude:** start with `docs/QUICKSTART_EXAMPLE_CLAUDE.md`.
- **You need to fix a bug:** start with `bundles/bugfix.md`.
- **You need to build a small feature:** start with `bundles/feature-build.md`.

If you are unsure which first-run path to choose, compare options in `docs/FIRST_WORKFLOW_CHOICES.md`.

## Recommended first reads
1. `README.md` (what this repository is and how layers fit together)
2. `docs/ARCHITECTURE.md` (core vs shells vs domains vs bundles)
3. One quickstart example for your environment:
   - Codex: `docs/QUICKSTART_EXAMPLE_CODEX.md`
   - Claude: `docs/QUICKSTART_EXAMPLE_CLAUDE.md`

## Recommended first workflow
1. Pick one small task.
2. Run `core/requirement-clarifier` to define objective and constraints.
3. Run `core/scope-locker` to lock allowed files.
4. Choose your shell planning style:
   - Codex: `shells/codex/planning-shell.md`
   - Claude: `shells/claude/planning-shell.md`
5. Execute minimal change with `core/safe-implementer`.
6. Report verified vs unverified using `core/verification-runner`.
7. Write a short continuation note with `core/handoff-writer`.

## What to ignore at first
- Do not read every skill file on day one.
- Do not start with growth/media domains unless that is your immediate task.
- Do not create new bundles before you can run one existing bundle successfully.

## Next step after first success
Repeat the same flow on one more small task, then adopt a bundle (`feature-build` or `bugfix`) as your default starting template.
