# Development Reflection Policy

## Purpose
This document defines how changes should be integrated after a task or test flow is completed.

Its goal is to reduce merge friction, prevent over-processing, and keep reflection-to-integration behavior consistent across projects.

---

## Core Principle

Always complete the workflow first, then choose the integration path.

Do not decide the merge/apply method before the task has been clarified, implemented, verified, and handed off.

---

## Required Precondition

Before choosing an integration path, complete these steps:

1. Workflow selection
2. Clarification / scope lock
3. Implementation
4. Verification
5. Handoff / next action

If these steps are not complete, the change is not integration-ready.

---

## Integration Path Rules

### 1. Manual Apply First
Choose **manual apply** when all of the following are true:

- the change affects only one file
- the change is small
- the change is mainly wording, compression, note insertion, or light documentation refinement
- full-file replacement is safer than line-level editing in the current environment
- the final file content is already available in full

Typical examples:
- README wording fix
- small documentation note
- SKILL.md wording compression
- one short clarification in a bundle file

In this mode:
- return the final updated file content in full
- apply it directly to GitHub main manually
- do not require PR if it adds unnecessary friction

---

### 2. PR First
Choose **PR first** when any of the following are true:

- the change adds a new file
- the change affects multiple files
- the change modifies repository structure or onboarding flow
- the change coordinates updates across docs, bundles, shells, or core skills
- the change should be reviewed as one grouped set

Typical examples:
- adding a new documentation page
- onboarding flow improvements across multiple files
- bundle + core skill alignment changes
- structural refinements

In this mode:
- review the grouped change as a unit
- prefer PR-based inspection before integration
- merge only after the grouped set is understood

---

### 3. PR Failure Fallback
If a PR-first change later conflicts:

- if the effective change is still small and limited to one file, switch to **manual apply**
- if the change is broad, multi-file, or structurally important, keep it in PR flow and resolve later
- do not force a complex merge if manual apply is clearly safer for a small change

---

## Source of Truth Rule

When local checkout and GitHub main diverge:

- treat **GitHub main** as the source of truth
- do not assume local absence means the file does not exist
- if checkout is stale, produce manual-edit-ready output based on the known target file in main

---

## Phone-First Rule

When working from a phone-first environment:

- prefer full-file replacement over fragile line-by-line editing
- prefer manual apply for small single-file changes
- avoid unnecessary merge conflict resolution for tiny documentation changes
- use PR mainly for grouped, multi-file, or new-file changes

---

## Reflection Rule

After each completed change, record:

- what kind of change it was
- which integration path was chosen
- whether that path was correct
- whether conflict occurred
- what should be improved next time

This keeps integration behavior reusable instead of improvised.

---

## Default Decision Summary

### Use Manual Apply when:
- one file
- small change
- wording / note / light docs refinement
- full content available
- phone-first editing is simpler

### Use PR First when:
- new file
- multiple files
- grouped workflow change
- structure or onboarding coordination
- review as one set is valuable

### If PR conflicts:
- small single-file change -> switch to manual apply
- broad multi-file change -> keep PR path

---

## What This Policy Does Not Do

This policy does not decide:

- business approval
- legal approval
- financial approval
- whether a fix is allowed without approval

Those are governed by higher-level delegation and approval rules.

This policy only governs **how completed changes are integrated**.

---

## Short Operational Rule

Finish the workflow first.  
Then classify the change.  
Small one-file changes go manual.  
New or multi-file changes go PR.  
If a small PR conflicts, switch to manual apply.
