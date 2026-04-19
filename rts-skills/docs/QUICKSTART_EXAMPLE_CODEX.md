# Quickstart Example (Codex)

## When to use this example
Use this when you are using Codex for the first time and want a minimal, safe workflow with strict scope and clear verification reporting.

## Example task
Improve `README.md` so first-time users can understand the difference between core skills and shells.

## Example Codex prompt
```text
Use the rts-skills framework for this task.

Task:
Improve README.md so first-time users can understand the difference between core skills and shells.

Use:
- core/requirement-clarifier
- core/task-decomposer
- core/scope-locker
- core/safe-implementer
- core/verification-runner
- core/handoff-writer
- shells/codex/planning-shell.md
- shells/codex/implementation-shell.md
- bundles/feature-build.md

Scope:
- Edit README.md only.
- Do not modify any other file.

Constraints:
- Keep changes minimal.
- Keep the README concise.
- Do not add broad new sections.
- Report verified vs unverified clearly.

Output:
1. Objective
2. Scope Lock
3. Task Breakdown
4. Planned Change
5. Change Summary
6. Verification
7. Unverified
8. Handoff Notes
```

## Expected response shape
- **Objective:** one-sentence target.
- **Scope Lock:** in-scope file(s), protected file(s), and out-of-scope statement.
- **Task Breakdown:** short ordered steps.
- **Planned Change:** minimal edit plan before implementation.
- **Change Summary:** what changed and why.
- **Verification:** commands run and results, with explicit evidence.
- **Unverified:** items not checked and why.
- **Handoff Notes:** what the next operator should do first.

## Why this works
- Core skills define **what** work method to follow.
- Codex shell files define **how** to execute and report in Codex.
- Scope lock prevents accidental expansion.
- Verified vs unverified reporting preserves trust boundaries.

## What not to do
- Do not edit files outside the scope lock.
- Do not merge planning and implementation into one vague step.
- Do not present assumptions as verified facts.
- Do not skip command-level verification evidence.
