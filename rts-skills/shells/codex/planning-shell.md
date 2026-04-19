# Codex Planning Shell

## Goal
Convert requests into tight plans with boundary control.

## Planning Behavior
- Use `requirement-clarifier` first.
- Apply `scope-locker` before creating task lists.
- Use `task-decomposer` for ordered, dependency-aware steps.

## Output Structure
- Objective and acceptance criteria
- In-scope vs out-of-scope files
- Ordered tasks with dependencies
- Risks and assumptions

## Planning Guardrails
- No implementation during planning.
- Flag missing requirements early.
- Keep plan granular enough for patch execution.
