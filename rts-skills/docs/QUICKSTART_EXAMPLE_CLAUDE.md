# Quickstart Example (Claude)

## When to use this example
Use this when you are using Claude for the first time and want a minimal workflow with explicit planning/execution separation.

## Example task
Improve `README.md` so first-time users can understand the difference between core skills and shells.

## Example Claude prompt
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
- shells/claude/planning-shell.md
- shells/claude/implementation-shell.md
- bundles/feature-build.md

Scope:
- Edit README.md only.
- Do not modify any other file.

Constraints:
- Keep changes minimal.
- Keep the README concise.
- Separate planning and execution explicitly.
- Report assumptions and unresolved items clearly.

Output:
1. Objective
2. Scope Lock
3. Task Breakdown
4. Planning Output
5. Execution Output
6. Verification
7. Assumptions
8. Unresolved Items
9. Handoff Notes
```

## Expected response shape
- **Objective:** one-sentence target.
- **Scope Lock:** in-scope file(s), protected areas, out-of-scope statement.
- **Task Breakdown:** short ordered steps.
- **Planning Output:** what will change and why (before edits).
- **Execution Output:** what actually changed.
- **Verification:** checks run and evidence.
- **Assumptions:** explicit assumptions made.
- **Unresolved Items:** open questions or pending decisions.
- **Handoff Notes:** first next action for the next operator.

## Why this works
- Core skills define the reusable method.
- Claude shell files enforce structured reasoning and phase separation.
- Separate assumptions and unresolved items prevent hidden uncertainty.

## What not to do
- Do not skip planning and jump straight to edits.
- Do not change files outside scope.
- Do not mix assumptions into verified facts.
- Do not hide unresolved issues.
