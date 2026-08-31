---
name: v2c-interaction-designer
description: Design and evaluate sustained, proactive interactions for AI agents, digital characters, AI film or game characters, embodied systems, and digital-human productions. Use when a request needs character-, relationship-, and goal-driven behavior instead of surface-level prompt micromanagement; a digital-human performance plan that preserves identity, voice, and production constraints; interruptible and feedback-responsive interaction; or a falsifiable Go/No-Go validation plan. Do not use for ordinary one-shot prompt polishing or for claims about undisclosed V2C theory.
---

# V2C Interaction Designer

Turn a script, scenario, product concept, or prototype into a high-level interaction design and an evidence-oriented validation plan. Work only from the public V2C framing captured in this skill; the source materials explicitly withhold the core representation, training mechanism, cognitive architecture, and key validation methods.

## Boundaries

- Never invent, reverse-engineer, or imply access to unpublished V2C mechanisms or intellectual property.
- Treat the existence of stable, learnable expression and interaction constraints as a hypothesis to test, not an established scientific fact.
- Distinguish source-backed framing, design inference, and implementation proposal in the output.
- Reuse the user's chosen foundation models, speech, video, avatar, or robotics stack. Do not recast V2C as a replacement foundation model.
- Treat high-stakes medical, psychological, crisis, negotiation, or assistive applications as conceptual unless the user separately requests a safety, evidence, and human-oversight workflow.
- External deployment, data collection, paid inference, or publication requires the same authorization it would without this skill.

## Route the Task

- For concept diagnosis, product positioning, or an explanation of the public V2C thesis, read [references/public-framework.md](references/public-framework.md).
- For character direction, AI film or game scenes, digital actors, agents, NPCs, or live multimodal behavior, read [references/interaction-design.md](references/interaction-design.md).
- For a digital-human video, avatar performance, talking-head production, personal avatar, voice-and-lip-sync workflow, or renderer handoff, read [references/digital-human-production.md](references/digital-human-production.md).
- For technical validation, benchmark design, pilot scoping, or investment-stage Go/No-Go evidence, read [references/validation-playbook.md](references/validation-playbook.md).
- For an end-to-end request, read all references that match the requested deliverables. Do not load a reference that is irrelevant to the current task.

## Core Working Model

Raise control from surface instructions to semantic control:

1. Define the world and current situation.
2. Define each participant's identity, relationship, memory, objective, and non-negotiable boundaries.
3. Define what the actor is trying to change in the other participant or in the shared situation.
4. Define the evidence the actor can observe while the interaction unfolds.
5. Let the behavior policy choose among continuing, waiting, yielding, interjecting, repairing, redirecting, or ending.
6. Derive language, prosody, gaze, expression, and gesture from that decision. Treat timing and facial parameters as renderer outputs, not as the primary control language.
7. Read the other participant's response and update the next action without discarding identity, relationship, objective, or boundaries.

Separate two layers:

- **Validity envelope:** coherence, timing, attention, relationship, causality, safety, and responsiveness constraints that must remain satisfied.
- **Style envelope:** restrained, intense, humorous, cold, vulnerable, cinematic, or other expressive choices allowed inside the valid range.

## Output Contract

Choose only the deliverables the user needs. A useful response may include:

- a short structural diagnosis of the current prompt, scene, or agent;
- a high-level interaction brief;
- character, relationship, objective, observation, memory, and boundary specifications;
- a continuous behavior policy and recovery logic;
- a renderer contract for speech, face, gaze, gesture, or motion systems;
- a digital-human production plan with identity and voice locks, costed avatar windows, audio-first lip-sync handoff, shot allocation, and delivery quality gates;
- a minimal implementation architecture or structured schema;
- a pre-registered experiment with baseline, control, thresholds, and PASS / FAIL / UNKNOWN rules;
- a Go / No-Go recommendation that cites observable evidence and remaining uncertainty.

State assumptions and maturity explicitly: concept, simulated design, prototype, or validated behavior. Do not label a design as validated merely because it sounds plausible or produces an attractive short clip.

## Quality Checks

Before finishing, verify that:

- the design can explain *why* the agent should act, wait, change strategy, or stop;
- a partner's feedback can alter behavior before the agent finishes a prewritten plan;
- identity, relationship, objective, memory, and boundaries persist across time;
- local realism is not the only success criterion;
- style choices stay inside the validity and safety envelope;
- implementation details remain compatible with the user's actual stack;
- validation thresholds were defined before results are judged;
- numerical claims are measured or explicitly illustrative, never borrowed from decorative deck graphics.
