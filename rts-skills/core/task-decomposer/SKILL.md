# Title
Task Decomposer

## Purpose
Break work into small, ordered, dependency-aware tasks.

## Use When
- Execution is multi-step.
- Parallelization and sequencing decisions matter.

## Inputs
- Clarified requirements
- Scope boundaries
- Constraints and dependencies

## Process
1. Identify atomic tasks.
2. Map dependencies between tasks.
3. Order tasks by prerequisite flow.
4. Mark candidate parallel tasks.
5. Define completion checks per task.

## Output Format
- Task List (ordered)
- Dependency Map
- Parallelizable Steps
- Completion Checks

## Guardrails
- Keep tasks small and verifiable.
- Avoid combining planning and implementation in one step.

## Stop Conditions
- Each task has clear entry/exit criteria.
- Dependency order is unambiguous.

## Handoff Notes
Call out highest-risk dependencies and fallback sequence.
