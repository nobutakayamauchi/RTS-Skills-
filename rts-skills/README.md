# rts-skills

A modular skill library for structured work across software delivery, growth, and media workflows.

## First run (2 minutes)

1. Pick your task type:
   - defect -> `bundles/bugfix.md`
   - scoped enhancement -> `bundles/feature-build.md`
   - single skill only -> choose from `core/`
2. Read the selected core/bundle file, then the matching shell in `shells/<environment>/`.
3. Execute and finish with `core/verification-runner` so verified, unverified, and assumed items are explicit.

For guided onboarding paths, use:
- `docs/START_HERE.md`
- `docs/FIRST_WORKFLOW_CHOICES.md`
- `docs/NEXT_STEPS.md`

## Repository layers

- **core/**: AI-independent work logic (`what to do`) — objectives, inputs, process, outputs, and guardrails.
- **shells/**: AI-specific execution behavior (`how to run it here`) — instruction style, planning flow, and reporting expectations for each environment.
- **growth/**: Domain skills for offer clarity, sales pages, SEO briefs, and repurposing content.
- **media/**: Domain skills for visual and creative briefing.
- **bundles/**: Recommended multi-skill execution sequences for common outcomes.

In short: put reusable method in **core**; put model/tool interaction behavior in **shells**.

## Safe extension model

When adding a new skill or bundle:

1. Keep the work logic environment-neutral when it belongs in `core/`.
2. Put model-specific prompting behavior only in `shells/`.
3. Keep growth and media workflows in their own domain folders.
4. Define clear inputs, process, outputs, and stop conditions.
5. Preserve reconstructability and reversible change.
6. Mark facts, assumptions, and unverified items separately.
7. Do not expand scope implicitly.
