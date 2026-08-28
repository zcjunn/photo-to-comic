# Prompt Compiler

Compile cards into visible production instructions. The prompt should be shorter than the analysis but explicit enough to control a multi-panel page.

## Compiler Order

1. Output: exactly one finished borderless comic page, default exact portrait width:height `2:3`, reading direction, and exact adaptive panel count of at least three. Name any explicit user ratio override.
2. Scene World Model and Action Affordance Map: source camera, support/depth, adjacency/routes, camera corridors, uncertain zones, and plausible action states.
3. Visual Concept Brief: central force, source-specific tension, turning point, ending image, and recurring motif.
4. Source role and narrative permission: the user's photo is the truth anchor; Held Moment, Adjacent Moment, or Poetic Expansion.
5. Theme and state change: one concrete proposition and the sequence movement.
6. Continuity Bible: identities, count, appearance, relationships, object geometry, place topology, recurring palette cues.
7. Prop/Motif Bible and Presence Matrix: selected primary/secondary roles, semantic locks, construction and material keys, recurrence, magnification/reveal, detail hierarchy, and intentional absence.
8. Page architecture: page zones, columns, each panel's aspect/span, dominant and supporting panels, prop screen-space budget, lateral-plus-downward reading path, gutter rhythm, and opening/ending contrast.
9. Panel map: one sentence per panel covering beat, visible action, viewpoint mode, camera corridor, shot/angle, focal owner, prop/motif job and visible components, evidence, value/color job, and transition.
10. Style Bible, Style Fingerprint, and Completion Lock: the six axes, at least four visible comic transformations, page composition/exposure lock, 5–9 interlocking colour masses, three value groups, scene-owned colour roles, faceted planes, connected brush fields, shared illumination, material-local marks, face geometry, focal-versus-context edge treatment, background completion, and no artist or franchise names.
11. Cross-panel differentiation and continuity: name the important changes and constants, including at least three shot scales, two angle/height changes, three focal owners, the reconstructed-viewpoint quota, frozen prop construction/material keys, and one frozen rendering-completion system.
12. Text and exclusions: wordless default; no invented people/objects/facts, repeated crops, camera lock, duplicate bookends, prop semantic or construction drift, lineart-dominant or mixed-finish output, photo-filter treatment, illegible lettering, franchise residue, or watermark.

## Create Template

```text
Transform Image 1 into exactly one finished, borderless compact portrait comic page with width:height exactly 2:3 and [N] clearly readable panels, read [direction]. This is a compact print-page composition, not landscape 3:2, not 4:5, not 9:16, not an extra-tall canvas, and not a top-to-bottom webtoon strip. Use Image 1 as the sole truth anchor for characters, clothing, objects, relationships, and place. Image 1 establishes the scene-world, not a locked camera: preserve its proven topology while reconstructing source-consistent new viewpoints. Do not paste or repeat the original photo as panel underpainting.

Scene World Model: source camera [side/height/distance]; support/depth [relationships]; adjacency/routes [relationships]; camera corridors [plausible new positions]; uncertain zones [keep simplified, occluded, or out of frame]. Action Affordance Map: [source-supported gaze, hand, prop, posture, reflection, weather, or route changes].

Visual Concept Brief: central force [person/object/relationship/place]; tension [source-specific conflict]; turning point [what changes]; ending image [what remains]; recurring motif [source-derived visual carrier].

Narrative permission: [Held Moment / Adjacent Moment / explicitly authorized Poetic Expansion]. Theme: [one concrete proposition]. The sequence moves from [state A] to [state B], leaving [unresolved residue]. Keep all invented adjacent action plausible within the same short moment and place.

Continuity Bible: preserve [subject identities/count], [face/hair/clothing/accessories or pet markings], [relationship and left-right/touch/possession cues], [signature object geometry], and [landmark/horizon/support/depth topology]. [Name any intentional off-panel omission.] Do not add, merge, swap, or accidentally remove people, limbs, animals, props, buildings, or landmarks.

Prop/Motif Bible: primary motif [one selected source-visible object, landmark, contact detail, or optical echo]; secondary motifs [zero to two, each with a separate role]. For each, preserve [semantic lock or stable fact-neutral reading], [visible count logic], [recognition silhouette and proportions], [visible component stack], [material/finish], [color/pattern], [contact/ownership], [topology/orientation], and [occluded unknowns]. Primary motif arc: [establish] → [construction/contact/material/scale reveal] → [optional altered echo]. Its close or dominant appearance must reveal more coherent source-supported information than its distant appearances. Do not redesign the motif when magnifying it.

Page architecture: use a genuinely two-dimensional [two- or three-column] mosaic on the fixed 2:3 page. [Name page zones, dominant panel, supporting splits/insets, each panel's shape/span, and the primary motif's screen-space/detail budget.] The eye enters at [entry], moves laterally to [next zone], descends to [middle zone], crosses laterally again, and exits through [final residue]. Use [small/medium/large] gutters according to [beat/action/time transition]. For four or more panels, never stack every panel in one column; for five or more, use at least three panel-aspect families when content permits and no more than two full-width panels. Opening/ending contrast: [at least four visible differences if they share a scale, plus changed motif meaning].

Panel map:
P1 — [beat + narrative delta]; [source-aligned or reconstructed-source-consistent]; [camera corridor + evidence]; [shot scale + camera height/angle]; [visible action + evidence]; [focal owner]; [prop/motif presence, job, screen scale, visible components, state/contact/reflection, detail level, and continuity note]; [value/color role]; [transition].
P2 — [...]
[continue exactly through PN]

Style Bible: [line], [value], [color], [shape/anatomy], [texture], [layout rhythm], [primary motif edge/material/detail hierarchy versus context]. Comic transformation operations: [at least four concrete redraw decisions]. Unless the user explicitly requests another medium, use the Painterly Comic Animation fingerprint: selective structural contours subordinate to painted masses; 5–9 interlocking colour masses; three broad light/middle/dark value groups with local colour turns; dominant field, structural counter, focal accent, and neutral bridge roles; reconstructed graphic silhouettes and faceted planes; connected neighbouring brush fields with shared boundary illumination; material-specific marks; focal-sharp/support-controlled/context-soft edges; simplified identity-faithful anime face geometry with head axis, eye-line, gaze, expression, and feature spacing protected; fully authored backgrounds in the same completion family; medium-dark borders and clean light gutters. At thumbnail size, large colour/value shapes must organize the page before thin line detail. Use one consistent character model, environment model, exposure key, palette logic, plane language, brush continuity, edge hierarchy, border language, and material finish across all panels. Let the source-derived [primary motif] recur with changed meaning while secondary motifs perform separate jobs. Do not render the source as a photo with a filter, flat pasted colour blocks, a global texture overlay, uniform blur, a lineart-only panel, or a mixture of sketch and rendered panels. If flat cel or opaque hard-edge rendering is explicitly requested, substitute the alternate Finished Luminous Cel Comic lock.

Make adjacent panels differ visibly on at least three axes: beat/time, camera corridor, shot scale, angle, subject scale, action, foreground, value shape, color role, edge density, or panel geometry. Use at least three shot scales, two camera heights/angles, and three focal owners when the source permits. Include at least one reconstructed viewpoint for 3–4 panels or at least two for 5+ panels. Do not solve variation by changing the character design or art style.

Default wordless visual storytelling: no dialogue, captions, title, legible signage, letters, numbers, logos, watermark, or signature. Avoid repeated crops of one pose, locking every panel to the source camera, opening/ending duplication, unsupported reverse-view detail, screenshot/contact-sheet composition, equal-grid monotony unless thematically justified, a one-column vertical stack, every panel spanning full width, five horizontal bands, a long strip or scroll canvas, accidental extra/missing subjects, face/clothing drift, invented source facts, a prop switching semantic category, count, silhouette, component stack, material, pattern, contact, or attachment across panels, a close prop panel with less information than a distant view, copied franchise characters/costumes/props/locations/layouts, generic anime wallpaper, photographic rendering, photo filter, flat pasted colour blocks, global brush/noise texture, uniform blur, unbound sticker-like subjects, lineart-dominant or mixed-finish output, translucent wash as the only finish, airbrushed or pore-detailed skin, photographic depth-of-field finish, dozens of equal hair strands, global hatching, mismatched character/background rendering, one sketch panel beside a fully painted panel, plastic skin, excessive effects, and unreadable tiny panels.
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
- State which panels are reconstructed viewpoints and what source evidence supports each one. “Different angle” without a camera corridor is not enough.
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
- Does every panel have a distinct shot scale, camera position, focal owner, and information delta?
- Are there at least three shot scales and two angle/height changes across the page?
- Does the page meet the reconstructed-viewpoint quota, with source evidence for every new camera corridor?
- If the source supports action, does at least one panel change gaze, pose, grip, prop state, or environmental response?
- Are the opening and ending visibly different at thumbnail scale, with at least four differences when they share a shot scale?
- Does the Style Bible name at least four visible redraw operations that make the result non-photographic?
- Unless another medium is explicit, does the prompt freeze the Painterly Comic Animation fingerprint and fully authored colour coverage across both character and environment?
- Are 5–9 interlocking colour masses, three value groups, scene-owned colour roles, faceted planes, connected brush fields, shared illumination, material-local marks, focal/support/context edge hierarchy, face geometry, and atmosphere-only softness explicitly locked across panels?
- Would the page still read first as authored colour/value shapes and a comic page at thumbnail size, rather than as a line drawing, pasted blocks, or a photo with a brush filter?
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
