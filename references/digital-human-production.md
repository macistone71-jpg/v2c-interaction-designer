# Digital-Human Production Mode

Use this reference when the sustained interaction design must become an AI-presenter, personal-avatar, digital-actor, or talking-head video. Keep V2C-level decisions above the rendering stack: character, relationship, objective, evidence, and boundaries determine the performance; voice, face, gaze, motion, and timing render that intent.

## Select the Scope

Distinguish two deliverables:

- **Production plan:** script, interaction brief, audio direction, avatar windows, shot list, prompts, handoffs, and quality gates. Produce this when connected generation or editing tools are unavailable or the user has not authorized paid generation.
- **Executed production:** generate only the approved assets, assemble the timeline, and verify the output. Never claim generation, upload, publishing, or validation that did not occur.

## Lock Identity and Voice

Before generating any avatar footage, record an identity lock and a voice lock.

- Use the user's latest explicitly confirmed avatar or training source. Do not silently substitute an older avatar, stock person, public figure, or a different identity.
- If the confirmed identity is not available in the active environment, pause before avatar generation and ask the user to provide or reconnect it. Continue with reversible planning work when useful.
- Treat avatar look identifiers as runtime values when a provider can rotate them. Resolve the latest valid look from the persistent avatar or group identity instead of treating an old look ID as permanent.
- Generate one canonical narration voice across avatar and non-avatar footage. Do not let the lip-sync provider re-read the text in another voice.
- If the selected voice provider, model, login, API configuration, or quota is unavailable, report the exact blocker. Do not silently fall back to another voice.

### Personal project defaults

Apply these defaults only for Maci Stone's personal digital-human project. A later explicit user choice overrides them.

- Avatar identity: the user's final confirmed personal HeyGen avatar.
- HeyGen persistent group ID: `c442982fc0594875b159a39c3d353755`.
- Voice provider: Fish Audio.
- Fish Audio model: `清晰青年男声` (`5456d33acb7c425fa1d08e54b297493d`).
- Legacy HeyGen voice `2cd9558922334f138dc94816485c9cdc` is disabled and must not be used for new work.
- HeyGen supplies the existing avatar image and lip sync only; feed it the approved Fish Audio output for every avatar segment.

These identifiers are configuration, not authorization. Never expose credentials, upload a private source asset, or start a paid generation merely because the identifiers are present.

## Plan Before Paid Generation

Determine the expected final duration and all visible avatar windows before calling a paid avatar service.

```text
avatar_ratio = sum(all visible avatar segment durations) / final video duration
```

- Hard maximum: `avatar_ratio <= 0.20`.
- Default target: `0.15–0.18`.
- Use motion graphics, screenshots, product footage, charts, captions, B-roll, or other non-avatar visuals for at least 80% of the final duration.
- Generate only the avatar segments that will appear in the edit. Never generate a full-length avatar video merely to trim most of it away.
- Record before generation: final duration, 20% ceiling, planned avatar segment durations, total avatar duration, planned ratio, and the reason each avatar appearance is needed.

## Audio-First Workflow

The approved narration is the timing and identity master for the production.

1. Finalize the spoken script and semantic beat structure before avatar generation.
2. Generate the personal voice in meaningful units. For the personal Fish Audio voice, default to one or two sentences and roughly 15–40 Chinese characters per unit; preserve natural breathing and sentence tails.
3. Use natural, conversational delivery rather than broadcast or advertisement diction. Keep 1.00x as the baseline speed; prefer script phrasing and edit spacing over mechanical time-stretching.
4. Add at most one low-intensity delivery tag only when the model actually needs it. Do not stack emotional labels or sustain exaggerated energy.
5. Assemble the approved units into one canonical master narration, preserving varied natural pauses. A useful personal-project starting range is about 0.10–0.22 seconds for ordinary joins and 0.25–0.38 seconds for meaningful transitions.
6. Derive the exact avatar audio segments from that approved narration. Do not ask HeyGen to synthesize the script again.
7. Preserve natural dynamics. At final mix, target approximately `-16 LUFS` integrated loudness and True Peak no higher than `-1.5 dBTP`, using only light compression unless the user specifies another delivery standard.

## Translate Interaction Intent Into Performance

For each avatar window, specify a semantic performance card:

```markdown
## Avatar Window
- Timeline:
- Narrative function:
- Actor objective:
- Relationship and audience stance:
- Evidence or cue being answered:
- Spoken content / audio asset:
- Prosody intent:
- Gaze and facial intent:
- Allowed gesture intensity:
- Forbidden behavior:
- Entry / exit transition:
- Fallback if rendering drifts:
```

Derive performance from function. A hook may carry restrained interest and direct gaze; a factual explanation should be calm and clear; a transition can pause and reset attention; a conclusion can slow slightly and close with certainty. Do not micromanage arbitrary emotion percentages when the renderer can accept semantic direction.

## Motion Policy

- Allow natural blinking, small nods, mild facial changes, and occasional gestures that support meaning.
- Prefer natural or low-intensity motion controls.
- Avoid repeated waving, continuous sweeping arm movements, a hand held up for long periods, constant hand motion, body rocking, and exaggerated facial acting.
- Preserve the motion style learned from the confirmed avatar source when the provider offers no reliable control.
- Check lip sync, gaze, expression, and gesture against the audio and objective across the entire segment, not only a single frame.

## End-to-End Handoff

Use this order when execution is authorized and the relevant tools are available:

1. Confirm outcome, platform, aspect ratio, duration, and publishing boundary.
2. Produce the interaction brief, script, and beat map.
3. Lock identity, voice, provider configuration, and avatar budget.
4. Generate and approve the canonical narration.
5. Allocate avatar and non-avatar windows on the master timeline.
6. Generate only the planned lip-synced avatar clips from the approved audio segments.
7. Create or collect non-avatar visuals, captions, and transitions.
8. Assemble on one master timeline; keep the canonical narration as the audio reference.
9. Run the quality gates below before export or publication.

Do not publish, share, change permissions, or distribute a private avatar or voice without the user's explicit authorization for that action.

## Quality Gates

Before delivery, verify and report observable results:

- identity matches the latest confirmed avatar across every visible segment;
- the same approved voice is present in avatar and non-avatar sections;
- lip sync starts and ends cleanly without clipped syllables or replaced audio;
- avatar visible duration and ratio are calculated from the final timeline and remain within the 20% limit;
- the avatar is used where relationship, trust, emphasis, or continuity benefits from a visible person;
- non-avatar visuals carry at least 80% of the runtime and are synchronized to the spoken meaning;
- performance supports each window's semantic objective and remains within the motion policy;
- dialogue or narration tails, pauses, captions, and cuts do not collide;
- final loudness, peak, aspect ratio, resolution, and file integrity meet the delivery target;
- generated, simulated, and unverified elements are labeled accurately.

When a gate fails, classify it as script, voice, identity, policy, lip-sync renderer, motion, timeline, mix, or export failure. Repair the smallest responsible layer rather than regenerating unrelated assets.
