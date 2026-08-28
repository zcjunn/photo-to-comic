# Source Story Card

Read whenever a source or output image is supplied. The goal is not pixel identity. It is credible continuity: the sequence should clearly grow from this photograph even when adjacent moments, framing, and emphasis change.

## Source Handling

- A supplied photo plus a request to transform it is consent to use the active image-generation service; do not ask again.
- Inspect locally first. Send only the final production prompt and the required photo to the generation service.
- Do not browse with, reverse-search, publish, or save the user's photo into unrelated project files.
- Public comic references found during trend research are a separate role: analysis-only, never generation inputs.

## Separate Observation from Inference

Use the following compact card. Omit irrelevant fields; never fill uncertainty with confident fiction.

```yaml
file_facts:
  dimensions: observed if available
  ratio_orientation: observed
  quality_limits: blur / crop / compression / glare / occlusion / low light
observed:
  subjects: count, visible identity cues, age band only if evident, pose, gaze, action
  relationships: touch, facing, distance, left-right order, shared task, separation
  signature_anchors: hair, clothing, accessory, pet markings, product silhouette, vehicle, landmark
  setting_topology: ground/support, horizon, room/road/shore/building layout, depth order
  dominant_gesture: gaze, lean, curve, path, diagonal, repetition, convergence, motion
  native_palette: dominant family, supporting family, focal accent, value range
  weather_material_light: only visible facts
  small_story_cues: hand position, displaced object, open door, footprint, shadow, reflection, edge action
  salient_prop_candidates: handheld object / wearable or contact detail / landmark / reflection, shadow, or surface echo
scene_world_model:
  support_surfaces: what holds each subject or object
  depth_bands: near, middle, far relationships
  adjacency_graph: what touches, borders, overlaps, leads to, or sits behind what
  routes_and_openings: visible paths, channels, thresholds, sight lines, and movement corridors
  camera_corridors: source-supported low, high, side, reverse, object-POV, or overhead positions
  uncertain_zones: hidden or ambiguous areas that must remain simple, occluded, or out of frame
inference:
  emotional_residue: what remains after factual description
  plausible_adjacent_moments: source-consistent possibilities, clearly labeled inference
  plausible_action_variants: small pose, gaze, hand, prop, or environmental states supported by evidence
  camera_opportunities: optional new camera positions scored for narrative gain, aesthetic gain, and scene confidence
  unresolved_question: one useful ambiguity
  ambiguous_prop_readings: visible form versus possible identities; never collapse uncertainty into fact
protected_continuity:
  identities_and_count: what must not drift
  appearance_bible: facial proportions, relative feature spacing, age cues, hair mass, clothes, markings, object geometry
  relationship_order: left-right, touch, gaze, possession, relative scale
  place_bible: landmark adjacency, horizon/support, depth bands, recurring color cues
  prop_motif_bibles: selected count, silhouette, visible component stack, material, pattern, contact, topology, and unknowns
transformable:
  framing: camera position, scale, angle, foreground, panel geometry; not limited to source crops
  adjacent_action: only within selected narrative permission
  emphasis: value, color, silhouette, edge, texture, weather/light envelope
  simplification: repeated details that may merge into comic rhythm
hard_avoids:
  invented facts: location/date/name/hidden content/dialogue
  continuity risks: extra/missing subjects, face/clothing drift, prop or topology mutation
```

## Salient Prop and Motif Inventory

Objects are not automatically motifs. Score source-visible candidates by whether they can materially shape the page:

- **Graphic salience:** distinctive silhouette, color, repetition, diagonal, scale, or contrast.
- **Narrative leverage:** carries action, attention, relationship, pressure, or state change.
- **Material/contact value:** hands, feet, fabric, water, metal, glass, wear, reflection, or another tactile relation can be shown.
- **Recurrence value:** remains recognizable from at least two source-supported viewpoints or through a reflection/shadow/detail.
- **Source confidence:** enough visible structure exists to keep it coherent without inventing hidden facts.

Select one primary motif and zero to two secondary motifs. A strong primary may be a held umbrella, sword-like embedded object, camera, vehicle, doorway, or recurring color shape. A useful secondary may be a shoe/contact point, landmark, reflection, shadow, strap, or repeated environmental line. Leave the rest as context.

Build this compact card for every selected item:

```yaml
motif_id: short stable label
category: handheld_or_movable / wearable_or_contact / landmark_or_scale / optical_or_surface_echo
role: primary / secondary
observed_form: only visible facts
source_certainty: confirmed identity / user-identified / ambiguous form
possible_readings: list only when ambiguous
selected_rendering: one source-consistent visual reading used throughout the page
visible_count: exact when countable; otherwise bounded and intentional
recognition_silhouette: outline and dominant proportions that survive at thumbnail size
visible_component_stack: ordered parts such as canopy-ribs-shaft-handle or grip-collar-shaft-rock insertion
material_and_finish: visible material, wetness, wear, reflection, edge quality
color_or_pattern: stable roles, markings, accents
contact_and_ownership: hand, foot, body, ground, wall, water, reflection, or none
topology_and_orientation: location, angle, spacing, overlap, attachment, repeated order
occluded_unknowns: parts that must stay hidden, cropped, silhouetted, or simple
permitted_states: source-supported tilt, grip, movement, reflection, lighting, or scale changes
panel_roles: establish / reveal construction / show contact or material / transform through echo / stabilize scale
detail_hierarchy: recognition in wide view / structure in medium view / material evidence in close view
```

### Ambiguous but salient forms

- Separate the observed geometry from its identity. `Several wet dark grip-like metal forms embedded diagonally in rock` is evidence; `ancient swords` may be only one reading unless the user identifies them.
- Choose one stable rendering category before prompting. A useful neutral choice may preserve sword-like grips, collars, metal shafts, spacing, and rock insertion while leaving blades or hidden ends occluded.
- Do not sanitize the form into generic rods if its distinctive handle-like construction drives the visual tension. Do not amplify it into a fantasy artifact unless the source or user authorizes that reading.
- Across panels, preserve the same count logic, recognition silhouette, component stack, material family, insertion/contact, and orientation family. Intentional off-panel omissions must be recorded.

## Scene World Model, Not Camera Lock

The source camera is one observation point inside a larger scene. Preserve the world relationships it proves, not its exact composition unless the user requests camera fidelity.

- Infer only coarse spatial structure: support, adjacency, depth order, routes, repeated landmarks, and where a camera could plausibly stand or look.
- Build a Camera Opportunity Map. Mark each candidate as `source-aligned` or `relocated-source-consistent`; score `narrative_gain`, `aesthetic_gain`, and `scene_confidence`; then choose `use`, `reject`, or `keep source-aligned` with one reason.
- New camera positions may include low water/ground level, grass/object POV, high or overhead, behind/over-shoulder, reverse angle, or a side view when the scene provides space for them.
- These are candidates, not quotas. Keep the source-aligned direction whenever it tells the story more beautifully or clearly. If no relocation earns a place, create panel difference through shot scale, action/state, focal owner, relationship/detail reveal, motif meaning, foreground, time beat, value ownership, or panel geometry.
- Do not reveal precise hidden faces, rooms, text, architecture, object backs, or geography. Crop, silhouette, simplify, or occlude uncertain zones.
- Never accept a crop ladder: source-aligned panels must still be newly staged comic beats with independent information roles rather than repeated crops or zooms.

## Action Affordance Map

Treat the photographed pose as one state, not the only permitted state.

- Record what can plausibly change within seconds: gaze, head turn, hand position, grip, prop tilt, weight shift, seated/standing posture, hair/clothing response, reflection, shadow, or nearby environmental motion.
- Tie every proposed action to a visible cue or physical affordance. A held umbrella may tilt or lower; a seated subject may turn or shift; a visible path may support one step. Do not invent an unrelated task or destination.
- Under Held Moment, keep the action state fixed and use scale, relation, detail, foreground, environmental response, or an earned camera change to create difference. Under Adjacent Moment, use at least one meaningful source-supported action change when the page has four or more panels and the source affords it.

## Narrative Permission

Choose one before writing beats.

### Held Moment

Use for documentary, memorial, product, architecture, or a request to preserve the actual moment. Decompose one moment through scale, detail, relation, reaction, environmental echo, or an earned camera relocation. Do not invent a before/after event. Keeping one camera direction is allowed when it is strongest, but repeated crops are not.

### Adjacent Moment — default

Invent a short plausible neighborhood around the visible moment: a preparation, continuation, reaction, or residue. Every invented beat must be supported by a visible gesture, object, relationship, weather condition, or spatial possibility. Keep the action small enough that the same people, clothing, place, and short time window remain credible.

### Poetic Expansion

Use only when the user asks for surreal, metaphorical, dreamlike, memory, or highly expressive storytelling. Preserve the semantic nucleus and identity anchors, but allow one visual metaphor or nonliteral transition. Do not pile up unrelated symbols.

## Theme Engine

Build through:

```text
source fact → relationship or pressure → emotional residue → theme proposition → state change → unresolved residue
```

Write two internal sentences:

1. **Theme proposition:** `[specific subject/relationship] meets [specific pressure or contradiction], revealing [what matters].`
2. **State change:** `The sequence moves from [visible or plausible state A] to [state B], leaving [one unresolved trace].`

Good themes are concrete and relational: waiting despite departure, shelter that also isolates, play becoming trust, a small figure measuring a large place, routine interrupted by a tiny signal.

Reject themes that are only `healing`, `nostalgia`, `cinematic`, `romantic`, `adventure`, `youth`, or `mysterious` without a visible structure that produces the feeling.

## Continuity Bible

Write a short cross-panel bible before prompting:

- **Character identity model:** facial proportions, relative feature spacing, age cues, hair silhouette/mass, clothing layers/colors, accessories, body scale, pet markings. Do not freeze head axis, eye-line, gaze, expression, mouth state, pose, or hand state; those are panel-specific performance variables.
- **Prop/Motif model:** use the selected cards above; protect recognition silhouette, visible component stack, count logic, material, pattern, contact, topology, permitted states, and occluded unknowns.
- **Place model:** support surfaces, adjacency graph, landmark order, near/mid/far bands, important openings/routes, camera corridors, uncertain zones, and recurring weather/light.
- **Style model:** line family, value grouping, palette roles, texture, anatomy exaggeration, panel border/gutter language.
- **Intentional omissions:** when a subject is deliberately off-panel or reduced to a detail, say so; absence must not look accidental.

When an important fact is obscured in the source, preserve the occlusion. Do not reconstruct hidden faces, bodies, text, structures, or objects as factual detail.
