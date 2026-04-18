# rts-skills

A standalone repository for reusable, AI-agnostic operational skills.

## What this repository is

`rts-skills` is a modular skill library for structured work across software delivery, growth, and media workflows. It is designed to be reused in different AI coding environments (such as Codex and Claude) without rewriting core methods each time.

## What problem it solves

Teams often mix execution logic with model-specific prompting, making skills hard to transfer between AI tools. This repository separates:

- reusable work logic (core skills)
- model-specific wrappers (shells)
- domain extensions (growth and media)
- multi-step workflow compositions (bundles)

This separation reduces lock-in, improves consistency, and makes workflows easier to audit and extend.

## Repository layers

- **core/**: AI-independent execution skills for engineering work.
- **shells/**: AI-specific adaptation guides (e.g., Codex, Claude) that describe how to apply the same skills in each environment.
- **growth/**: Domain skills for offer clarity, sales pages, SEO briefs, and repurposing content.
- **media/**: Domain skills for visual and creative briefing.
- **bundles/**: Recommended multi-skill execution sequences for common outcomes.

## Safe extension model

When adding a new skill or bundle:

1. Keep the work logic environment-neutral when it belongs in `core/`.
2. Put model-specific prompting behavior only in `shells/`.
3. Keep growth and media workflows in their own domain folders.
4. Define clear inputs, process, outputs, and stop conditions.
5. Preserve reconstructability and reversible change.
6. Mark facts, assumptions, and unverified items separately.
7. Do not expand scope implicitly.

## Adapting one core skill to many AI environments

Use a two-part pattern:

1. **Core skill (`core/.../SKILL.md`)**: stable method and output expectations.
2. **Shell (`shells/<environment>/...`)**: interaction style and execution constraints for that AI tool.

This keeps behavior portable while still optimizing for each environment's strengths.

## Relationship to RTS

This repository is intentionally separate from the main RTS product codebase in early phases. It can later be referenced or integrated, but remains decoupled now to:

- avoid premature product coupling
- allow reuse across multiple contexts
- iterate on skill quality independently

See `docs/ARCHITECTURE.md` and `docs/ROADMAP.md` for details.
