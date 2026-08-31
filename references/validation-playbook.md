# Validation Playbook

Use this reference to design a short, low-cost, falsifiable technical validation or Go / No-Go pilot.

## Principle

Test one structural claim per round. Define the claim, comparison, measurements, and decision rule before observing results. The goal is to expose a wrong path early, not to produce a persuasive demo at any cost.

## Experiment Card

```markdown
# Experiment Card

## Claim
- Operational hypothesis:
- Why it matters:
- Known alternative explanations:

## Scope
- Target scenario and participants:
- Modalities and duration:
- In-scope behavior:
- Out-of-scope behavior:

## Systems
- Baseline:
- Candidate:
- Control variables:
- Randomization / counterbalancing:

## Measurements
- Primary metric and rationale:
- Critical thresholds:
- Secondary metrics:
- Boundary and safety checks:
- Structured logs and artifacts:

## Evaluation
- Rater instructions and blinding:
- Trial count / sample-size rationale:
- Statistical or deterministic analysis:
- Confound checks:

## Decision
- PASS rule:
- FAIL rule:
- UNKNOWN rule:
- Stop conditions:
- Next action for each outcome:
```

## Choose a Baseline That Tests the Claim

Useful comparisons include:

- surface-level micro-prompts plus repeated sampling versus a high-level character/relationship/objective specification;
- completed-turn `ASR -> LLM -> TTS` behavior versus an event-driven policy that can revise an unfinished action;
- a system judged only on short local realism versus the same system judged across long sequences and interruptions;
- no persistent relationship/objective state versus explicit persistent state;
- free generation versus generation constrained by a validity and safety envelope.

Keep foundation models, content, voices, avatars, hardware, and rendering settings constant when they are not the variable under test.

## Measurement Families

Choose measurements that expose the structural claim. Do not use all of them automatically.

### Longitudinal coherence

- identity and role consistency;
- relationship-state consistency and justified change;
- objective persistence or evidence-based revision;
- causal continuity across interruptions;
- memory accuracy and uncertainty handling.

### Mutual responsiveness

- whether partner feedback changes the current or next action;
- response timing relative to the signal, not only end-to-end latency;
- interruption acceptance and recovery quality;
- correct use of waiting, yielding, clarification, repair, redirection, and ending;
- attention maintenance without over-speaking or ignoring resistance.

### Direction and control

- number of low-level corrective prompts required from a human;
- number of discarded generations or retries;
- time to a usable scene or interaction;
- semantic-intent adherence across language, prosody, face, gaze, and motion;
- consistency when the same high-level brief is rerun.

### Outcome and safety

- progress toward the stated interaction objective;
- adherence to hard boundaries and story invariants;
- rate and severity of unsafe or unrecoverable failures;
- quality of escalation or graceful termination.

Local naturalness can remain a secondary metric. It should not substitute for these structural measures.

## Evaluation Design

- Pre-register primary metrics and critical thresholds.
- Use blind or double-blind human evaluation when subjective judgment is unavoidable.
- Give raters concrete observable questions instead of asking only whether a result “feels natural.”
- Record sample size, rater count, exclusions, variance, and agreement.
- Add deterministic checks for boundaries, required events, latency, interruptions, and state transitions where possible.
- Preserve structured event logs so a result can be traced to observable input, selected semantic action, renderer output, feedback, and state update.
- Separate rendering failures from policy failures.

Never copy percentages or confidence numbers from a presentation graphic into an experiment. Derive thresholds from the scenario's risks, baseline distribution, measurement precision, and decision cost.

## PASS / FAIL / UNKNOWN

Use decision rules consistently:

- **PASS:** every predeclared critical threshold is met, no disqualifying boundary violation occurs, and the result survives confound checks.
- **FAIL:** a critical threshold is missed by a meaningful margin, a disqualifying failure occurs, or the hypothesized effect is absent under an adequately powered test.
- **UNKNOWN:** evidence is insufficient, contradictory, contaminated by confounds, or too imprecise for the predeclared decision rule.

UNKNOWN is not a soft PASS. It may justify one targeted follow-up that fixes the identified evidence gap. Do not repeatedly redesign metrics after seeing unfavorable results.

## Minimal Go / No-Go Pilot

Prefer a small pilot that answers the highest-leverage question:

1. Select one scenario where surface realism is already adequate but sustained behavior visibly matters.
2. Implement a baseline and one candidate change.
3. Include at least one interruption, ambiguous signal, goal conflict, and boundary-trigger case when relevant.
4. Run repeated, logged trials with controlled inputs.
5. Apply the predeclared evaluation and decision rule.
6. Produce a decision memo: evidence, uncertainty, failure taxonomy, and the cheapest next test.

Recommend continued investment only when the result passes the stage gate. If it fails, stop or change the hypothesis. If it is unknown, address only the specific measurement or confound gap before expanding scope.

## Decision Memo

The final memo should state:

- the tested claim and why it matters;
- what differed between baseline and candidate;
- what was observed, with uncertainty;
- whether the result is PASS, FAIL, or UNKNOWN under the predeclared rule;
- which failures were policy, perception, memory, renderer, integration, or evaluation failures;
- the smallest justified next step;
- what remains unproven, especially any claim about undisclosed V2C mechanisms.
