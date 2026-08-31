# Interaction Design Playbook

Use this reference to turn a scenario, script, character, agent, NPC, or embodied-system concept into a sustained interaction specification.

## Select the Operating Mode

### Directed performance

Use for AI film, digital actors, games, and authored scenes. Preserve the writer's events and the director's artistic intent, while moving low-level performance choices into an actor policy.

### Live interaction

Use for conversational agents, companions, NPCs, virtual employees, robots, or other systems responding to an active partner. Design an event-driven loop rather than a sequence of completed turns.

Hybrid systems may use authored scene boundaries with live behavior inside each boundary.

## Intake

Collect or infer only what materially changes behavior:

- participants, modalities, environment, and expected duration;
- character identity, role, history, knowledge, and current condition;
- relationship state, trust, power, obligations, and unresolved tension;
- scene objective and the specific change sought in the partner or world;
- available observations and their uncertainty;
- hard boundaries, safety rules, story invariants, and escalation paths;
- style envelope and forbidden tonal choices;
- the rendering stack for language, voice, face, gaze, gesture, and motion.

If a missing value would materially change the design, mark an assumption instead of silently inventing certainty.

## Interaction Brief

Use this structure when a full specification is useful:

```markdown
# Interaction Brief

## Situation
- World / location / time:
- Triggering event:
- Participants and modalities:
- Expected duration and continuity:

## Actor
- Identity and role:
- Stable traits and commitments:
- Current physical / cognitive / emotional condition:
- Relevant memory:

## Relationship
- Relationship type and history:
- Current trust / power / distance:
- Obligations and unresolved tension:

## Objective
- Immediate objective:
- Desired change in partner or situation:
- Evidence of progress:
- Conditions for abandoning or revising the strategy:

## Boundaries
- Must preserve:
- Must never do:
- Safety / escalation / termination conditions:

## Style Envelope
- Allowed expressive range:
- Forbidden style choices:
- Artistic or brand direction:

## Observation Model
- Observable signals:
- Confidence / ambiguity handling:
- Signals that require immediate reevaluation:

## Behavior Policy
- Continue when:
- Wait when:
- Yield when:
- Interject when:
- Ask / clarify when:
- Repair when:
- Redirect when:
- End / escalate when:

## Memory Update
- Persist:
- Decay:
- Never infer without evidence:

## Renderer Contract
- Semantic action:
- Language constraints:
- Prosody intent:
- Gaze / face / gesture intent:
- Timing constraints:
- Synchronization and fallback behavior:
```

Do not fill every field when a smaller artifact is enough.

## Continuous Decision Loop

Design the behavior around events and evidence:

```text
observe signals and system state
update situation, relationship, and progress estimates
check safety, boundaries, and termination conditions
select a semantic action: continue | wait | yield | interject |
                          clarify | repair | redirect | end/escalate
render that action through language, voice, face, gaze, and motion
monitor partner feedback during rendering
interrupt or revise the current action when new evidence crosses a threshold
persist justified memory and repeat
```

The policy must allow an unfinished utterance or action to be revised. A system that only evaluates after completing its planned output is still turn-based at the behavioral level.

## Directed-Performance Translation

Translate authored material in this order:

1. Preserve plot facts, mandatory lines, scene boundaries, and forbidden deviations.
2. Identify each beat's objective, obstacle, relationship change, and evidence of success or failure.
3. Give the AI actor the character, relationship, objective, memory, boundary, and style envelopes.
4. Let the actor policy choose an expression strategy for each beat.
5. Let the renderer derive words where improvisation is allowed, plus prosody, gaze, facial expression, gesture, and timing.
6. Review the complete scene for longitudinal coherence, not only attractive frames or isolated lines.

Use low-level values only when a renderer requires them. Record their semantic source so they can be regenerated rather than hand-tuned blindly.

## Implementation Layers

Map a design to the user's stack without assuming a proprietary V2C implementation:

```text
perception/events
    -> situation and partner-state estimator
    -> character/relationship/objective memory
    -> constraint and safety gate
    -> semantic behavior policy
    -> multimodal renderer adapters
    -> interruption monitor and feedback loop
    -> structured logs for validation
```

Keep the interfaces explicit. A renderer should receive semantic intent and constraints; it should not silently change the actor's objective or relationship state.

## Failure and Recovery Cases

Design at least the failures relevant to the scenario:

- partner interrupts or begins to disengage;
- evidence contradicts the actor's assumption;
- two goals conflict;
- rendering fails or drifts from semantic intent;
- the actor repeats itself or over-pursues the objective;
- a boundary or safety condition activates;
- memory is missing, stale, or uncertain;
- another agent acts unexpectedly;
- the interaction must end before the objective is reached.

For each case, specify detection evidence, the immediate safe action, the repair strategy, and what memory should be updated.

## Review Checklist

- Can every meaningful behavior be traced to character, relationship, objective, evidence, or boundary?
- Can feedback change behavior during an unfinished action?
- Are wait, yield, repair, and end valid choices rather than failures?
- Is the character stable without becoming rigid?
- Is style subordinate to validity and safety?
- Are renderer parameters derived rather than manually used as the primary direction?
- Are uncertainty and missing evidence visible in the state?
- Can the interaction be logged and tested without access to hidden internal reasoning?
