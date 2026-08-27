# Title
Combat Economy Governor

## Purpose
Control how much execution capability, reasoning budget, and external capability is committed to a task so the system can preserve success probability while reducing total cost per verified resolution.

Treat work as a bounded encounter with four economic quantities:

- **Summon Cost**: fixed/step cost of starting or escalating an executor.
- **HP**: executor-local reasoning/context/iteration budget.
- **MP**: external capability budget for skills, tools, search, retrieval, specialist calls, or bounded creation.
- **Enemy HP**: evidence-backed remaining unresolved work, not raw code size.

The governing objective is not minimum HP or minimum MP in isolation. It is the lowest expected total resolution cost that preserves required verification and safety.

## Use When
- A task can be solved through more than one executor strength, skill, tool, or search path.
- A capable executor is becoming over-equipped or context-heavy by default.
- Repeated trial-and-error is consuming more reasoning or tool budget than necessary.
- Past execution records can improve future routing, switching, or stopping decisions.
- A development loop needs a consistent way to choose executor strength, resource allocation, loadout, escalation, and post-battle learning.

## Inputs
- Task / desired outcome
- Repository and scope constraints
- Required verification level
- Failure impact / reversibility
- Available executor tiers or reasoning strengths
- Available skills/tools/search/create surfaces and their approximate costs
- Current context and known evidence
- Relevant prior battle records, when available
- Hard budget or operational limits, when present

## Core Invariants

`STRONGEST EXECUTOR != DEFAULT EXECUTOR`

`MORE TOOLS != MORE CAPABILITY PER COST`

`LOW MP != LOW TOTAL COST`

`LOW HP != LOW TOTAL COST`

`FAST SUCCESS != REPRODUCIBLE SUCCESS`

`HYPOTHESIS != VERIFIED STRUCTURE`

`PROGRESS CLAIM != ENEMY HP REDUCTION WITHOUT EVIDENCE`

`FAILURE TO FIT EXISTING WEAPONS != AUTOMATIC PERMISSION TO CREATE`

`WIN != OPTIMAL WIN`

## Five-Part Runtime

### 1. Encounter Scanner
Estimate the encounter before committing heavy resources.

Record at minimum:
- scope size;
- uncertainty;
- dependency depth;
- novelty;
- failure impact;
- reversibility;
- verification difficulty;
- remaining unresolved work.

Produce:
- `enemy_rating`;
- initial `enemy_hp` with an explicit decomposition;
- top structural hypotheses;
- uncertainty / unknowns;
- minimum acceptable verification level.

Enemy HP represents unresolved evidence-bearing work such as requirements, design, implementation, verification, deployment reality, or unresolved defects. Do not equate Enemy HP with lines changed.

### 2. Summon Planner
Choose the weakest executor profile that has a credible path to the required outcome.

For each candidate executor tier, estimate:
- summon cost;
- expected HP demand;
- expected MP demand;
- expected success probability;
- escalation probability;
- expected verification coverage.

Prefer the minimum expected-cost tier that clears the required confidence and safety threshold.

Do not summon multiple executors by default. Escalate only when the current executor cannot efficiently reduce uncertainty or Enemy HP.

### 3. Resource Governor
Allocate bounded resources after summon.

Track separately:
- `hp_budget`: reasoning/context/iteration allowance;
- `mp_budget`: external skill/tool/search/create allowance;
- `reserve_budget`: budget withheld for escalation, verification, or recovery.

Do not spend the full budget up front.

At each material decision point, compare at least these options:
1. spend more HP to reason locally;
2. spend MP to load a relevant capability;
3. run a low-cost probe that separates hypotheses;
4. switch or discard the current capability;
5. escalate executor tier;
6. search/retrieve externally;
7. create a new capability only when bounded evidence shows the existing arsenal is insufficient.

Choose the option with the best expected reduction in unresolved work per total cost, subject to verification and safety constraints.

### 4. Combat Director
Run the task as a feedback loop rather than a fixed full loadout.

Loop:
1. **Observe** current evidence and Enemy HP.
2. **Classify** likely structure and retrieve the smallest useful prior pattern.
3. **Select** the cheapest plausible weapon/skill/tool or local reasoning move.
4. **Attack / Probe** with a bounded action.
5. **Measure** whether uncertainty or Enemy HP actually decreased.
6. **Continue, Transform, Switch, Discard, Escalate, Search, or Create** based on observed fit.
7. Repeat until verified resolution or a stop condition is reached.

#### Weapon Fit
A candidate capability should be evaluated on:
- structural fit;
- expected information gain;
- execution cost;
- switching cost;
- risk / blast radius;
- prior success on similar structures;
- verification availability.

#### Stagnation Sensor
Detect when cost is being consumed without meaningful progress.

Trigger a reassessment when any bounded threshold is crossed, for example:
- repeated actions produce no new evidence;
- Enemy HP does not materially decrease;
- the same hypothesis is retried without new evidence;
- tool/skill switching becomes random rather than evidence-driven;
- HP or MP burn rate exceeds expected progress;
- the current executor is spending more to recover than an escalation would cost.

A stagnation trigger does not automatically mean "use more tools". Recompute the cheapest discriminating next action.

#### Discard Discipline
Do not preserve a weapon, skill, hypothesis, or implementation path because resources have already been spent on it.

`SUNK COST != CONTINUATION AUTHORITY`

If observed fit falls below the continuation threshold, discard or transform it and move on.

### 5. Battle Recorder / EXP Compiler
After the encounter, record not only whether the task succeeded, but how economically and reproducibly it succeeded.

Record:
- encounter fingerprint and structural class;
- initial Enemy Rating and Enemy HP decomposition;
- executor tier and summon cost;
- initial/final HP, MP, and reserve usage;
- capability/loadout timeline;
- hypotheses attempted;
- probes and information gained;
- switch/discard/escalation decisions;
- final verified structure / root cause when known;
- final verification evidence;
- total elapsed steps/time when measurable;
- avoidable actions discovered in hindsight;
- candidate cheaper path for the next similar encounter.

Learning must extract reusable structure, not memorize surface error text alone.

Promote experience only when it can improve at least one of:
- earlier structural recognition;
- smaller candidate set;
- faster discard decision;
- cheaper probe selection;
- lower HP demand;
- lower MP demand;
- lower summon tier;
- stronger verification at equal or lower cost.

## Economic Model
Use the following conceptual objective when estimates are available:

`Expected Resolution Cost = Summon Cost + HP Cost + MP Cost + Escalation Cost + Failure Probability * Recovery/Rebattle Cost`

Do not optimize a numeric score when its inputs are fabricated. When costs are only ordinal, use `LOW / MEDIUM / HIGH` or bounded relative estimates and preserve uncertainty.

## Performance Metrics
Primary:
- verified success rate;
- `cost_per_verified_resolution`;
- Enemy HP reduction per unit cost;
- median HP used;
- median MP used;
- escalation rate;
- unnecessary weapon/skill calls;
- mean actions before correct structural class;
- mean actions before discarding a bad path.

Learning / maturity:
- Top-1 / Top-3 initial structural hypothesis hit rate;
- reduction in candidate count for repeated structural classes;
- reduction in total resolution cost on comparable encounters;
- verification retention while cost declines;
- percentage of battle records that produce reusable structural learning.

## Output Format
For each governed encounter, produce a compact battle state and final battle record.

### Battle State
- Encounter / objective
- Enemy Rating
- Enemy HP + decomposition
- Executor tier / summon decision
- HP / MP / reserve remaining
- Current structural hypotheses
- Current weapon/skill/tool
- Evidence gained this step
- Enemy HP change
- Next decision: continue / transform / switch / discard / escalate / search / create / stop

### Final Battle Record
- Outcome: verified success / bounded partial / blocked / failed
- Verification evidence
- Total summon + HP + MP + escalation cost
- Final Enemy HP
- Winning path
- Discarded paths and why
- Avoidable cost
- Reusable structural lesson
- Recommended starting loadout/tier for the next comparable encounter

## Guardrails
- Never trade away required safety, authorization, or verification merely to reduce cost.
- Never invent precise cost, probability, Enemy HP, or confidence numbers when evidence is insufficient.
- Keep facts, hypotheses, and estimates explicitly separate.
- Prefer small discriminating probes over broad random trial-and-error.
- Preserve a reserve for verification/recovery on consequential tasks.
- External search/retrieval does not become internal truth without validation.
- Create/new-build is a bounded fallback, not the first response to uncertainty.
- A battle record provides learning evidence, not automatic promotion authority.
- Do not keep full history active when a compact structural fingerprint and source pointer are sufficient.

## Stop Conditions
Stop the combat loop when any of the following is true:
- Enemy HP is reduced to zero with the required verification evidence;
- the authorized scope is exhausted;
- further progress requires unavailable evidence, authority, credentials, or human input;
- expected additional cost exceeds the authorized budget;
- the current plan is unsafe or irreversible beyond allowed bounds;
- repeated stagnation persists after bounded reassessment/escalation.

When stopped before verified resolution, report the remaining Enemy HP/unknowns and the cheapest evidence-bearing next action.

## Handoff Notes
For future operators, preserve:
- what executor tier was sufficient;
- what HP/MP allocation actually worked;
- which weapon/skill was first useful;
- which paths should be skipped next time;
- which structural fingerprint predicts the winning path;
- what evidence would justify a lower-cost summon or loadout in the next comparable encounter.
