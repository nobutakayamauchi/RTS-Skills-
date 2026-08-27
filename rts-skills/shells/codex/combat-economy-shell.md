# Codex Combat Economy Shell

## Goal
Apply `core/combat-economy-governor` to Codex execution so model strength, reasoning/context use, skills/tools/search/create calls, and iteration depth are treated as a single bounded combat economy.

## Mental Model
- **Summon Cost** = cost of invoking or escalating Codex capability.
- **HP** = Codex-local reasoning, context, iteration, and debugging budget.
- **MP** = cost of loading skills, tools, search/retrieval, specialist help, or Create/new capability work.
- **Enemy HP** = remaining evidence-backed development work.
- **Weapons** = skills/tools/techniques that may be transformed, switched, or discarded rapidly when fit is poor.

Do not literalize the RPG vocabulary in user-facing output unless useful. The runtime semantics matter more than the metaphor.

## Ultimate Loop Integration
This shell is a cross-cutting execution governor for an Ultimate Loop run. It does not add a new canonical lifecycle stage and does not bypass repository-local governance, Human Gates, freeze state, verification gates, or authority boundaries.

Use it around the active development sequence to decide:
- how strong a Codex executor to use;
- how much reasoning/context budget to commit;
- which skills/tools to load and when;
- when a weapon/path is no longer worth continuing;
- when to escalate, search, retrieve, or Create;
- what battle record should be retained as reusable structural learning.

## Invocation Pattern
1. Read repository-local instructions and freeze/authority state first.
2. Define the encounter: objective, scope, verification target, failure impact, reversibility, and known evidence.
3. Estimate Enemy Rating and decompose Enemy HP into unresolved work classes.
4. Select the weakest credible Codex profile/reasoning strength.
5. Allocate bounded HP, MP, and reserve; do not front-load the full allowance.
6. Start with the smallest plausible weapon/skill or local reasoning move.
7. After each material action, measure evidence gained and Enemy HP reduced.
8. If fit is weak, transform/switch/discard quickly instead of defending sunk cost.
9. If progress stalls, choose the cheapest discriminating probe before adding more armor/tools.
10. Escalate Codex strength or invoke Search/Create only when expected resolution cost is lower than continued local struggle and authority permits it.
11. Finish with repository-required verification.
12. Write the battle record and extract reusable structural learning.

## Codex-Specific Sensor Stack
Keep these signals logically distinct even when evaluated in one pass:

### Intuition Sensor
Generate a small ranked set of likely structural classes from current symptoms and prior experience.

Purpose: reduce search space quickly.

Do not treat intuition as proof.

### Structure Sensor
Trace evidence, dependencies, runtime state, invariants, and causality to determine what is actually happening.

Purpose: correct or confirm the fast intuition path.

### Similarity Sensor
Recall the smallest relevant prior structural fingerprint rather than loading full history.

Purpose: reuse experience without context bloat.

### Weapon Fit Sensor
Estimate which current skill/tool/reasoning move has the best expected information or progress gain per cost.

Purpose: choose what to use now and when to abandon it.

### Novelty Sensor
Detect when no existing weapon has adequate fit.

Purpose: decide whether bounded search/retrieval or Create is justified instead of repeatedly forcing known skills onto an unknown structure.

## Switching Discipline
Codex should behave like a fast multi-weapon operator, not a permanent full-armor loadout.

Preferred order:
1. **Transform** the current general weapon when a cheap mode change is enough.
2. **Switch** to another existing skill/tool when structural fit changes.
3. **Discard** a low-fit path early when new evidence contradicts it.
4. **Retrieve/Search** when the arsenal lacks current knowledge.
5. **Create** only when a real capability gap remains after bounded reuse/search.

`SUNK COST != REASON TO KEEP A LOADOUT`

## Escalation Heuristic
Escalate Codex strength when one or more are true and a stronger summon is expected to be cheaper than continued struggle:
- the task remains structurally ambiguous after bounded probes;
- context integration exceeds the current executor's reliable capacity;
- repeated low-quality attempts are burning HP without Enemy HP reduction;
- verification or risk analysis requires stronger reasoning;
- multiple candidate structures remain coupled and cannot be separated cheaply;
- a smaller executor would require enough specialist/tool calls that a stronger executor is cheaper overall.

Do not escalate merely because the task feels difficult.

## HP Rules
Treat the following as HP-consuming:
- deep repository reading;
- long-context integration;
- multi-step causal reasoning;
- repeated patch/debug loops;
- maintaining many live hypotheses;
- reconstructing forgotten state that should have been compactly recalled.

When HP burn is high, first ask whether a smaller recall, discriminating probe, or relevant skill can reduce the reasoning burden.

## MP Rules
Treat the following as MP-consuming:
- skill loads;
- tool/MCP/connector calls;
- web/search/retrieval;
- specialist sub-executors;
- heavy automated analysis;
- Create/new skill/new helper construction.

Do not minimize MP by forcing Codex to rediscover known methods through expensive reasoning. Spend MP when it lowers expected total cost.

## Battle Record Contract
At completion or bounded stop, capture:

```text
encounter:
enemy_rating:
enemy_hp_initial:
enemy_hp_final:
enemy_hp_breakdown:
executor_profile:
summon_cost:
hp_budget / hp_used:
mp_budget / mp_used:
reserve_budget / reserve_used:
initial_top_hypotheses:
weapon_timeline:
key_probes:
switch_discard_events:
escalations:
search_create_events:
winning_structure:
verification:
outcome:
avoidable_cost:
reusable_fingerprint:
next_starting_tier:
next_starting_weapon:
```

Exact numeric cost is optional. Use ordinal or relative values when precise accounting is unavailable. Never fabricate precision.

## Learning Rule
A completed run should make the next comparable run cheaper or more reliable.

Extract:
- what clue should have been recognized earlier;
- which candidate weapon should move up/down in rank;
- how early a losing path could have been discarded;
- whether the executor was over- or under-summoned;
- whether HP should have been exchanged for MP or vice versa;
- the smallest structural fingerprint that predicts the winning path;
- the minimum verification set that still proves success.

Do not encode a surface mapping such as `error text -> action` when a deeper causal structure is available.

## Reporting Contract
Report compactly:
- encounter state and remaining Enemy HP;
- Codex tier and resource posture;
- current winning structural hypothesis;
- weapons/skills used and discarded;
- verification status;
- final cost summary;
- reusable lesson for the next run.

## Guardrails
- Repository-local governance always outranks this shell.
- Human authorization boundaries remain unchanged.
- Cost reduction cannot justify weaker required verification.
- Search findings remain external evidence until validated.
- Create does not grant automatic promotion or reuse authority.
- Never load every available skill/tool "just in case".
- Keep reserve for verification and recovery on consequential work.
- If confidence is low, prefer an information-rich probe over random weapon cycling.
