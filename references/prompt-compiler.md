# Prompt Compiler

Compile cards into visible production instructions. The prompt should be shorter than the analysis but explicit enough to control a multi-panel page.

## Compiler Order

1. Output: exactly one outer-borderless image containing one finished comic page with at least three visibly divided internal panels, default exact portrait width:height `2:3`, reading direction, and exact adaptive panel count. It must never collapse into one hero frame. Name any explicit user ratio override.
2. Style-dominance header: when the painterly default is active, state within the first three prompt blocks that this is a visibly hand-painted animation comic page, not clean digital cel anime. Name interlocking opaque paint masses, unequal internal turns, connected directional strokes, shared boundary light, lost-and-found edges, and explicit bans on uniform complete outlines, smooth cel bands, vector-clean surfaces, and airbrushed commercial-anime polish.
3. Material Paint Proof Map: select at least four source-present materials when available and assign each a visible construction, stroke direction, edge behavior, reflectance, and panel/detail-scale proof. Do not hide this behind a generic `painterly` label or global texture.
4. Scene World Model and Action Affordance Map: source camera, support/depth, adjacency/routes, camera corridors, uncertain zones, and plausible action states.
5. Visual Concept Brief: central force, source-specific tension, turning point, ending image, and recurring motif.
6. Source role and narrative permission: the user's photo is semantic scene/story evidence, never a single-frame Edit Target; Held Moment, Adjacent Moment, or Poetic Expansion.
7. Theme and state change: one concrete proposition and the sequence movement.
8. Continuity Bible: identities, count, appearance, relationships, object geometry, place topology, recurring palette cues.
9. Prop/Motif Bible and Presence Matrix: selected primary/secondary roles, semantic locks, construction and material keys, recurrence, magnification/reveal, detail hierarchy, and intentional absence.
10. Page architecture: page zones, columns, each panel's aspect/span, dominant and supporting panels, prop screen-space budget, lateral-plus-downward reading path, gutter rhythm, and opening/ending contrast.
11. Camera Opportunity Map and Panel Map: score level, low, high/overhead, side, reverse, over-shoulder, and object-level candidates by narrative gain, aesthetic gain, and scene confidence; then write one sentence per selected panel covering beat, visible action, camera decision, shot scale, focal owner, prop/motif job and visible components, evidence, value/color job, and transition. Keeping a source-aligned camera is valid when it is strongest.
12. Style continuity reinforcement: freeze the six axes, at least four visible comic transformations, area-adaptive `5-9` major colour masses for dominant panels and `3-6` for small support panels, three-value logic, one time/weather/palette family with panel-specific exposure emphasis, scene-owned colour roles, faceted planes, connected brush fields, shared illumination, the Material Paint Proof Map, face identity geometry, broken/lost-and-found edge treatment, background completion, and no artist or franchise names. Do not introduce the medium here for the first time; this block confirms the early style identity across every panel.
13. Cross-panel differentiation and continuity: name the important changes and constants, including at least three shot scales, independent information roles, non-crop visual deltas, three focal owners when supported, frozen prop construction/material keys, and one frozen rendering-completion family. Do not impose an angle quota.
14. Text and exclusions: wordless default; no invented people/objects/facts, repeated crops, crop-only source-template lock, forced camera novelty, duplicate bookends, prop semantic or construction drift, clean-cel drift, lineart-dominant or mixed-finish output, photo-filter treatment, illegible lettering, franchise residue, or watermark.

## Create Template

```text
Transform Image 1 into exactly one outer-borderless image containing one finished compact portrait comic page with width:height exactly 2:3 and [N, never fewer than 3] visibly divided internal panels, read [direction]. Never return a single hero image. This is a compact print-page composition, not landscape 3:2, not 4:5, not 9:16, not an extra-tall canvas, and not a top-to-bottom webtoon strip. Use Image 1 only as the semantic truth anchor for character identity, clothing, objects, relationships, and place. It is not a painterly Edit Target: do not inherit its pixel ratio, exact composition, crop, headroom, subject placement/scale, horizon/quiet-space distribution, pose, head axis, gaze, expression, or camera. Preserve proven scene-world topology while authoring the best comic sequence. Do not paste or repeat the original photo as panel underpainting.

STYLE DOMINANCE — HAND-PAINTED ANIMATION COMIC PAGE, not clean digital cel anime. Build every panel from interlocking opaque paint shapes, unequal internal colour turns, connected directional strokes, shared boundary illumination, and lost-and-found edges. Use sparse broken painted contour fragments only at important overlaps, expressions, contacts, and silhouette turns. No uniform complete outlines, no smooth two-band cel shading, no vector-clean surfaces, no airbrushed commercial-anime finish, and no polished cel character layer over a separate background.

Material Paint Proof Map: [source-present material A → broad base, unequal turns, stroke direction, edge behavior, reflectance, visible proof]; [B → visibly different behavior]; [C → visibly different behavior]; [D → visibly different behavior when available]. At thumbnail scale, irregular interlocking masses and edge rhythm must organize the page. At panel scale, faceted turns, connected stroke currents, and shared light must be visible. At detail scale, at least three important materials must show different mark scale, direction, edge, and reflectance, with no important form enclosed by one perfect vector-like perimeter.

Scene World Model: source camera [side/height/distance]; support/depth [relationships]; adjacency/routes [relationships]; camera corridors [plausible new positions]; uncertain zones [keep simplified, occluded, or out of frame]. Action Affordance Map: [source-supported gaze, hand, prop, posture, reflection, weather, or route changes].

Camera Opportunity Map: consider source-aligned level, relocated level, low-angle, high/overhead, side, reverse, over-shoulder, and object-level cameras. For each useful candidate record [narrative gain], [aesthetic gain], [scene confidence], and [use/reject/keep source-aligned + reason]. Change camera position only when it strengthens story, emotion, scale, spatial clarity, or beauty with enough scene evidence. It is valid to keep the source camera direction when it is strongest; never force angle variety as a quota. Even then, every panel must gain information through shot scale, action/state, focal owner, relation/detail reveal, motif change, foreground, time beat, value ownership, or panel geometry—not crop alone.

Visual Concept Brief: central force [person/object/relationship/place]; tension [source-specific conflict]; turning point [what changes]; ending image [what remains]; recurring motif [source-derived visual carrier].

Narrative permission: [Held Moment / Adjacent Moment / explicitly authorized Poetic Expansion]. Theme: [one concrete proposition]. The sequence moves from [state A] to [state B], leaving [unresolved residue]. Keep all invented adjacent action plausible within the same short moment and place.

Continuity Bible: preserve [subject identities/count], [facial proportions, relative feature spacing, age cues, hair mass, clothing/accessories or pet markings], [relationship and left-right/touch/possession cues], [signature object geometry], and [landmark/support/depth topology]. Treat head axis, eye-line, gaze, expression, mouth state, pose, and hand state as panel-specific performance variables. [Name any intentional off-panel omission.] Do not add, merge, swap, or accidentally remove people, limbs, animals, props, buildings, or landmarks.

Prop/Motif Bible: primary motif [one selected source-visible object, landmark, contact detail, or optical echo]; secondary motifs [zero to two, each with a separate role]. For each, preserve [semantic lock or stable fact-neutral reading], [visible count logic], [recognition silhouette and proportions], [visible component stack], [material/finish], [color/pattern], [contact/ownership], [topology/orientation], and [occluded unknowns]. Primary motif arc: [establish] → [construction/contact/material/scale reveal] → [optional altered echo]. Its close or dominant appearance must reveal more coherent source-supported information than its distant appearances. Do not redesign the motif when magnifying it.

Page architecture: use a genuinely two-dimensional [two- or three-column] mosaic on the fixed 2:3 page. [Name page zones, dominant panel, supporting splits/insets, each panel's shape/span, and the primary motif's screen-space/detail budget.] The eye enters at [entry], moves laterally to [next zone], descends to [middle zone], crosses laterally again, and exits through [final residue]. Use [small/medium/large] gutters according to [beat/action/time transition]. For four or more panels, never stack every panel in one column; for five or more, use at least three panel-aspect families when content permits and no more than two full-width panels. Opening/ending contrast: [at least four visible differences if they share a scale, plus changed motif meaning].

Panel map:
P1 — [beat + narrative delta]; [source-aligned or reconstructed-source-consistent]; [camera corridor + evidence]; [shot scale + camera height/angle]; [visible action + evidence]; [focal owner]; [prop/motif presence, job, screen scale, visible components, state/contact/reflection, detail level, and continuity note]; [value/color role]; [transition].
P2 — [...]
[continue exactly through PN]

Style continuity reinforcement: [line], [value], [color], [shape/anatomy], [texture], [layout rhythm], [primary motif edge/material/detail hierarchy versus context]. Comic transformation operations: [at least four concrete redraw decisions]. This layer controls rendering only and may not restore the source camera, composition, pose, gaze, or ratio. Unless the user explicitly requests another medium, keep the early hand-painted Painterly Comic Animation identity across every panel: approximately 5-9 interlocking major colour masses in a dominant panel and 3-6 in a small support panel; three broad light/middle/dark value groups with unequal local turns; dominant field, structural counter, focal accent, and neutral bridge roles; reconstructed graphic silhouettes and faceted planes; connected neighbouring brush fields with shared boundary illumination; the same source-specific Material Paint Proof Map; focal-sharp-fragment/support-broken/context-lost edge hierarchy; simplified identity-faithful painted-animation face geometry preserving facial proportions, relative feature spacing, age cues, and hair mass while allowing panel-specific head turns, gaze, expression, and pose; fully authored backgrounds in the same painted completion family; medium-dark borders and clean light gutters. Use one consistent character model, environment model, time/weather and palette family, plane language, brush continuity, broken-contour logic, border language, and material finish across all panels; allow each shot to recompose mass count, value ownership, local exposure emphasis, focal accent position, and image-space light pattern. Let the source-derived [primary motif] recur with changed meaning while secondary motifs perform separate jobs. If flat cel or opaque hard-edge rendering is explicitly requested, substitute the alternate Finished Luminous Cel Comic lock; otherwise a clean cel-anime page is a failed output, not a stylistic variant.

Make adjacent panels differ visibly on at least three axes: beat/time, selected camera corridor, shot scale, subject scale, action, foreground, value shape, color role, edge density, focal owner, or panel geometry. Use at least three shot scales and three focal owners when the source permits. New camera positions are optional and must be earned by the Camera Opportunity Map; do not force a minimum number. A page with no camera relocation can pass only when its panels are genuinely re-staged with independent narrative roles and non-crop information gain. Do not solve variation by changing the character design or art style.

Default wordless visual storytelling: no dialogue, captions, title, legible signage, letters, numbers, logos, watermark, or signature. Avoid repeated crops of one pose, preserving the exact source composition/pose/gaze in every panel, forced low/high/reverse novelty, opening/ending duplication, unsupported reverse-view detail, screenshot/contact-sheet composition, equal-grid monotony unless thematically justified, a one-column vertical stack, every panel spanning full width, five horizontal bands, a long strip or scroll canvas, accidental extra/missing subjects, face/clothing drift, invented source facts, a prop switching semantic category, count, silhouette, component stack, material, pattern, contact, or attachment across panels, a close prop panel with less information than a distant view, copied franchise characters/costumes/props/locations/layouts, generic anime wallpaper, photographic rendering, photo filter, flat pasted colour blocks, global brush/noise texture, uniform blur, unbound sticker-like subjects, lineart-dominant or mixed-finish output, translucent wash as the only finish, airbrushed or pore-detailed skin, photographic depth-of-field finish, dozens of equal hair strands, global hatching, mismatched character/background rendering, one sketch panel beside a fully painted panel, plastic skin, excessive effects, and unreadable tiny panels.
```

Replace every bracket and delete irrelevant clauses.

## Panel Sentence Rules

- Name one primary action and one information delta.
- Use visible nouns and verbs. Replace `cinematic`, `epic`, `emotional`, or `dynamic` with camera, pose, value, color, and spatial decisions.
- Avoid micromanaging tiny texture before the page hierarchy is clear.
- If a panel intentionally omits the main subject, name the remaining clue so the absence reads as purposeful.
- For a three-panel minimum, make all three roles necessary: establishment, meaningful change or reveal, and residue/echo. Do not use a three-panel wide/medium/close crop ladder as a substitute for progression.
- Never describe the page as “four versions,” “different crops,” or “same scene from several angles.” Describe the concept and the information delta instead.
- Require at least one environment-led or object-led panel when the source permits; a page made entirely of centered character shots is not a storyboard.
- For every selected camera relocation, state the supporting source evidence and the narrative or aesthetic gain. When a source-aligned camera is retained, state why it is the strongest option and how that panel still differs beyond cropping.
- Treat the opening and ending as a pair. If they share a scale, list at least four visible differences and the changed meaning of the recurring motif.
- If a primary motif is selected, name its construction key and material key once, then state only the panel-specific visible components, state/contact/reflection, screen scale, and detail level. Do not rewrite its design separately in every panel.
- A prop-led or relationship-led panel must reveal at least one new source-supported layer: component construction, material behavior, hand/foot contact, support or insertion, reflection/shadow, motion state, or scale relation. A closer crop alone is not a reveal.
- For ambiguous objects, prompt the observed form and stable selected rendering, not an unsupported factual backstory. List hidden components that must remain occluded.

## Tool Execution

- Inspect the actual source before compiling.
- Attach only the user's photo through the active image tool's real reference-image mechanism.
- Default to one output and one generation call.
- If the user explicitly requests separate frames, generate at least three and hold the same Continuity Bible and Style Bible across them.
- Do not attach trend-reference art, covers, or sampled comic pages.
- Inspect the result beside the source before declaring success. Never claim visual verification of a prompt or unviewed result.
- Make no more than one automatic targeted correction.

## Preflight Veto

Do not send the prompt to image generation if any answer is “no”:

- Can the story be summarized as a source-specific turning point rather than a mood?
- Does every panel have an independent beat, information role, focal owner or relation, and visible delta rather than a crop-only change?
- Are there at least three shot scales across the page?
- Is the Camera Opportunity Map complete, with every relocation supported by narrative/aesthetic gain and scene confidence, and with no forced angle quota?
- If the source supports action, does at least one panel change gaze, pose, grip, prop state, or environmental response?
- Are the opening and ending visibly different at thumbnail scale, with at least four differences when they share a shot scale?
- Does the Style Bible name at least four visible redraw operations that make the result non-photographic?
- Unless another medium is explicit, does the prompt freeze the Painterly Comic Animation fingerprint and fully authored colour coverage across both character and environment?
- Does the first style clause appear before the detailed Panel Map and explicitly establish a hand-painted animation comic while rejecting clean digital cel anime, complete uniform outlines, smooth cel bands, vector-clean surfaces, and airbrushed gradients?
- Does a source-specific Material Paint Proof Map name at least four present materials when available, with observable construction, direction, edge, reflectance, and visible proof rather than a global texture label?
- Are area-adaptive interlocking colour masses (`5-9` dominant, `3-6` small support), three-value logic, scene-owned colour roles, faceted planes, connected brush fields, shared illumination, material-local marks, focal/support/context edge hierarchy, face identity geometry, and atmosphere-only softness explicitly locked without freezing panel-specific pose, gaze, exposure emphasis, or camera?
- Would the page still read first as authored colour/value shapes and a comic page at thumbnail size, rather than as a line drawing, pasted blocks, or a photo with a brush filter?
- Is painterly authorship provable at all three scales: irregular interlocking masses/edge rhythm at thumbnail, faceted connected turns/shared light at panel scale, and divergent material marks/no perfect vector perimeter at detail scale?
- Does the page architecture have a dominant beat, readable entry/path/exit, and non-redundant gutters?
- Is the default canvas stated as exact portrait width:height `2:3`, with no silent `4:5`, `9:16`, landscape, or scroll substitution?
- For four or more panels, does the page use at least two columns or an equally clear inset/mosaic topology rather than a single vertical stack?
- For five or more panels, are there at least two lateral reading moves, no more than two full-width panels, and multiple panel-aspect families?
- Did the source inventory select no more than one primary and two secondary motifs, each with a distinct role rather than decorative clutter?
- When a primary motif is selected, does it appear at least twice when source/panel count permit, including one object-led or relationship-led reveal with real information delta?
- Are the primary motif's semantic lock, count logic, recognition silhouette, visible component stack, material/pattern, contact/attachment, and occluded unknowns consistent in the Presence Matrix?
- Does the detail hierarchy increase from distant recognition to medium construction to close material evidence, without redesigning the prop?
- If the motif is ambiguous, is one source-consistent visual reading maintained across all panels without asserting unseen facts?

## Exact Text Route

When the user explicitly requires text:

1. collect or infer only copy the user has authorized;
2. keep wording short and assign each line to a specific balloon/caption area;
3. preserve generous safety space and a clear reading order;
4. verify every character after generation;
5. if exact rendering cannot be verified, remove the text and disclose the limitation rather than deliver gibberish.

## Prompt-only Output

Return:

1. Source Story Card summary;
2. narrative permission and theme/state change;
3. panel count rationale, Prop/Motif Bible and Presence Matrix, and Panel Difference Map;
4. Style Bible, Style Fingerprint, Completion Lock, prop detail hierarchy, and originality-isolation summary;
5. one compiled tool-ready prompt;
6. `No image was generated or visually verified.`

If the source is missing, ask for it instead of fabricating the card.
