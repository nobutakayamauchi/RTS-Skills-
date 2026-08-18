# Plain Knowledge Profile

Status: TEMPLATE / CLIENT-NEUTRAL

## 1. Human-important outcome

- Outcome:
- Success condition:
- Failure condition:

## 2. Reusable invariants

Rules that must survive personalization because they protect correctness, safety, evidence, authority, recovery, or reconstructability.

- Invariant:
- Invariant:

## 3. Neutral operating defaults

Defaults that may be changed by a client overlay without breaking the human-important outcome.

- Default:
- Default:

## 4. Required client inputs

Unknown values that must be supplied before client-specific optimization.

| field | why required | acceptable form | current state |
|---|---|---|---|
| `<client_goal>` | defines optimization target | text / measurable target | UNKNOWN |
| `<decision_thresholds>` | controls trade-offs | explicit thresholds | UNKNOWN |
| `<authority_boundary>` | defines who may approve material actions | role / rule | UNKNOWN |
| `<evidence_requirement>` | defines proof needed before completion | checklist / contract | UNKNOWN |

## 5. Vocabulary placeholders

- `<canonical_term_1>`:
- `<canonical_term_2>`:

## 6. External dependency declarations

Declare required capabilities, not connector implementation.

| capability | preferred provider | required? | adapter state |
|---|---|---:|---|
| `<capability>` | UNSPECIFIED | yes/no | EXISTING / NEEDED / UNKNOWN |

## 7. Prohibited assumptions

- Do not infer missing client facts.
- Do not treat author habits as universal requirements.
- Do not remove safety/evidence/recovery rules merely to simplify the profile.

## 8. Known unknowns / conflicts

- UNKNOWN:
- CONFLICT:

## 9. Verification notes

- Frozen outcome preserved: VERIFIED / UNVERIFIED
- Required invariants preserved: VERIFIED / UNVERIFIED
- Author-specific tuning removed/generalized: VERIFIED / UNVERIFIED
- Client data absent: VERIFIED / UNVERIFIED
- Connector/runtime implementation absent: VERIFIED / UNVERIFIED

## 10. Lineage

- Source workflow:
- Source revision:
- Prepared by:
- Preparation date:
- Related execution record:
