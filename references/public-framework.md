# Public V2C Framework

Use this reference for diagnosis, positioning, and conceptual explanation. It summarizes only the non-secret framing in the supplied V2C overview and pitch deck.

## Status and Scope

V2C is described as a pre-product, pre-commercial research effort in core technical validation. Its public thesis is not proof of the hidden mechanisms. Phrase conclusions as hypotheses, design principles, or experiment proposals unless reproducible evidence is supplied.

## The Structural Gap

Modern language, speech, video, avatar, and motion models can generate locally convincing outputs. The unresolved question is whether a system can maintain coherent expression and purposeful participation while circumstances and partner feedback change over time.

Two objectives must not be conflated:

- **Looks human:** an observer judges a clip, voice, face, or gesture as realistic or natural.
- **Acts as a sustained participant:** the system has a reliable basis for deciding whether to continue, wait, yield, interrupt, repair, redirect, or stop.

A short, attractive sample can satisfy the first objective while failing the second. Diagnose the latter over sequences, interruptions, conflicting signals, and long-running interaction.

## From Search to Directed Behavior

Prompt micromanagement plus repeated sampling makes a human search a large output space. It can be effective for one-off content but pushes the human into specifying surface results such as exact pauses, facial movements, or emotional percentages.

The proposed shift is:

| Surface-control workflow | Higher-level workflow |
| --- | --- |
| Prompt-driven | Situation- and interaction-rule-driven |
| Repeated sampling | Deliberation inside explicit constraints |
| Facial or timing micromanagement | Character, relationship, and objective direction |
| Fixed script playback | Bounded, adaptive scene evolution |
| Discrete question and answer | Sustained behavior and mutual influence |
| Locally human-like output | A stable participant over time |

This does not eliminate generative models. It places a control, evaluation, and adaptation layer above them.

## Continuous Interaction

Do not model live interaction only as `ASR -> LLM -> TTS`. That pipeline can be useful infrastructure, but it encourages completed-turn processing. A sustained interaction policy must be able to:

- monitor while speaking or acting;
- wait when evidence is incomplete;
- accept or anticipate interruption;
- yield or interject when context warrants it;
- repair a misunderstanding or failed action;
- redirect when the original strategy no longer serves the objective;
- attract and maintain attention without ignoring the partner;
- end or escalate when boundaries require it.

The key criterion is mutual influence during the unfolding event, not merely low-latency alternating messages.

## Stable Constraints and Style

The materials propose that varied human expression may share stable, learnable constraints. This remains an experimental hypothesis. In design work, operationalize it as two layers:

1. A validity envelope containing coherence, relationship, timing, attention, causal, safety, and response constraints.
2. A style envelope containing creative variation that is allowed only while the first layer remains satisfied.

Do not reduce style to arbitrary weighted emotion labels. Prefer a reasoned strategy tied to character, relationship, objective, and evidence.

## Position Relative to Foundation Models

Treat language, speech, video, perception, avatar, and motion models as reusable infrastructure. The proposed V2C layer focuses on narrower, higher-leverage decisions: semantic control, constraints, validation, memory reuse, and adaptive strategy. Stronger foundation models may improve rendering without resolving the control problem by themselves.

## Diagnostic Questions

Use these questions to locate the structural gap:

1. Who is the acting subject, and what persists about them across time?
2. What relationship is active, and how does it constrain acceptable behavior?
3. What is the actor trying to change in the partner or situation?
4. What live evidence can change the actor's next action?
5. Can the system wait, yield, interrupt, repair, redirect, and end?
6. Does it preserve context and intention across interruptions?
7. Are expression parameters derived from a reasoned action, or manually supplied as the action itself?
8. Is success judged only by local realism, or also by longitudinal coherence and outcome?
9. Can the claim be falsified in a short, controlled experiment?

## Appropriate Claim Language

Prefer:

- “The public materials hypothesize…”
- “This design operationalizes the hypothesis as…”
- “The proposed experiment would test whether…”
- “Evidence is currently insufficient to conclude…”

Avoid:

- “V2C has proven…” without supplied evidence;
- invented details about proprietary representations, training, or cognition;
- market-size claims presented as current realized demand;
- decorative percentages from presentation graphics presented as measurements.
