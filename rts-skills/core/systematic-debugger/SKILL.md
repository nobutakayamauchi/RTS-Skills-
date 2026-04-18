# Title
Systematic Debugger

## Purpose
Resolve defects through a disciplined reproduce → narrow cause → single fix → verify flow.

## Use When
- Behavior is broken or inconsistent.
- Root cause is uncertain.

## Inputs
- Bug report or failing behavior
- Reproduction context
- Logs, tests, or traces

## Process
1. Reproduce the issue reliably.
2. Narrow the cause via targeted checks.
3. Choose one primary fix.
4. Apply only that fix.
5. Verify the issue is resolved.
6. Check for obvious regressions.

## Output Format
- Reproduction Steps
- Root Cause
- Fix Applied
- Verification Results
- Regression Notes

## Guardrails
- Avoid shotgun debugging.
- Do not bundle multiple unrelated fixes.

## Stop Conditions
- Reproduction no longer fails.
- Verification confirms intended behavior.

## Handoff Notes
Include remaining hypotheses if full resolution is not reached.
