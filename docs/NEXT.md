# RTS-Skills Next Actions

The next goal is an inventory pass, not implementation expansion.

## Next Tasks

1. List existing skill definitions and shells.
2. Identify which skills are ready, draft, stale, or duplicate.
3. Confirm naming and manifest key conventions.
4. Document which outputs each skill should produce.
5. Check local documentation links.
6. Decide which skills should remain here and which belong in adjacent repositories.

## Suggested Follow-up Files

```text
docs/inventory/skills_inventory.md
docs/contracts/skill_manifest_contract.md
docs/relations/adjacent_repo_boundaries.md
```

## Inventory Categories

Use these labels during the next pass:

- READY: usable as a reusable skill definition
- DRAFT: useful but incomplete
- STALE: likely outdated or superseded
- DUPLICATE: overlaps another skill
- MOVE: belongs in another repository
- ARCHIVE: preserve for history only

## Do Not Do Yet

Do not:

- add runtime execution code
- add connector internals
- add pack internals
- import adjacent repository internals
- rewrite all manifests at once
- refactor the repository broadly
- promote a skill to canonical status without review

## Next Recommended Task

Create `docs/inventory/skills_inventory.md`.

That file should list each known skill or shell with:

1. name
2. path
3. purpose
4. status label
5. expected output
6. dependencies or adjacent repo relation
7. next smallest safe action
