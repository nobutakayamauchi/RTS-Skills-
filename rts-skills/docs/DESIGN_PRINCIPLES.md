# Design Principles

## 1) Reconstructability first
Outputs should make it easy for another operator or model to reproduce decisions and steps.

## 2) Minimal reversible change
Prefer the smallest change that solves the defined problem and can be safely rolled back.

## 3) Explicit assumptions
Clearly separate known facts from assumptions and unknowns.

## 4) No silent scope expansion
Work only within stated goals and boundaries unless scope changes are explicitly approved.

## 5) Handoff-ready outputs
Every skill output should support low-friction continuation by another operator.

## 6) Separate logic from model behavior
Core skills capture stable work logic. Shell files capture environment-specific interaction style.

## 7) Domain isolation
Keep engineering, growth, and media skills in separate domains unless bundled intentionally.
