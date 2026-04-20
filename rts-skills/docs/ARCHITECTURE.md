# Architecture

## Layered structure

The `rts-skills` architecture uses five layers:

1. **Core** (`core/`)
   - Reusable work logic.
   - AI-agnostic skills that define method, guardrails, and outputs.

2. **Shells** (`shells/`)
   - AI-specific execution wrappers.
   - Translate core skills into model-appropriate operating instructions.

3. **Growth** (`growth/`)
   - Sales, offer, SEO, and content-system skills.
   - Separated from engineering execution logic.

4. **Media** (`media/`)
   - Visual and creative briefing skills.
   - Focused on image/video-oriented workflows.

5. **Bundles** (`bundles/`)
   - Repeatable compositions of multiple skills.
   - Define recommended order and expected outputs for recurring jobs.

## Why this repository is separate from RTS (for now)

`rts-skills` is intentionally split from the RTS application repository at bootstrap stage to ensure:

- skill evolution is independent from product release cycles
- workflows stay reusable across non-RTS projects
- model-specific adaptation can evolve without changing product code
- governance and quality standards can be stabilized before integration

Future integration can happen through references or selective import once the skill patterns have proven stable.
