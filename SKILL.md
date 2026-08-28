---
name: photo-to-comic
description: >-
  Transform one user-supplied photograph into one original comic sequence of at least three visible panels, normally composed as a compact portrait 2:3 multi-column page, with source-derived themes, adaptive storytelling, varied shot scales, optional story-driven camera relocation, salient prop or motif authorship, and a stable painterly comic-animation rendering system. Use for 照片转漫画组图、照片漫画化叙事、漫画分镜页、manga page from a photo, adaptive-panel comic storytelling, prop-led comic sequencing, painterly comic control, or reviewing such an output. The painterly layer controls colour, planes, brushwork, materials, edges, and finish only; it must not lock the source camera, composition, pose, gaze, or aspect ratio. Do not use for a single cartoon portrait/filter, a two-panel diptych, source-free comic creation, exact franchise or artist imitation, or pixel-locked photo preservation.
---

# Photo to Comic

Turn one photograph into one finished comic page that feels authored as a sequence, not repeated crops of the same image. Preserve the source's people, place, objects, and emotional provenance while inventing only source-consistent adjacent moments. Treat the photograph as evidence for a scene-world, not as a locked camera. Let narrative information determine panel count and hierarchy. Always design the story, plausible action space, and camera grammar before writing the image prompt; never use the source photo as a ready-made panel underpainting.

## Routes

- **Create — default:** inspect the supplied photo, design the sequence, generate one finished raster comic page with at least three clearly separated panels, inspect it, and return it. Never collapse this route into one borderless hero frame or one image without panel divisions.
- **Prompt-only:** inspect the photo and return a source-aware production plan plus one tool-ready prompt; do not generate or imply verification.
- **Review / revise:** compare a comic page with its source, report continuity and sequence quality separately, and revise only when requested or when the default Create result needs one targeted correction.

If the source photograph is unavailable, ask the user to attach it. Do not invent a photo-specific plan from memory. Route requests for a single comic portrait or a source-free story away from this skill.

## Load Relevant References

- For any supplied source or output image, read [references/source-story-card.md](references/source-story-card.md).
- When choosing, researching, or translating a current, popular, named, or unspecified comic style, read [references/style-research.md](references/style-research.md).
- When using the painterly comic-animation default or translating painterly-frame methods, read [references/painterly-comic-adapter.md](references/painterly-comic-adapter.md).
- For every Create or Prompt-only route, read [references/sequence-engine.md](references/sequence-engine.md).
- Before generation or returning a prompt, read [references/prompt-compiler.md](references/prompt-compiler.md).
- After generation, during review, or before any retry, read [references/quality-gate.md](references/quality-gate.md).

## Core Contract

### One source, one theme, one sequence

- Treat the photo as a truth anchor and story seed, not as a surface to receive a comic filter.
- Derive one specific theme from a visible relationship, gesture, scale conflict, environmental pressure, or emotional contradiction.
- Give the sequence a perceptible state change or revelation. Quiet change is valid; generic mood labels are not a story.
- Default to one complete borderless comic page. Generate separate frames only when the user explicitly requests them.

### Storyboard before rendering

- Write a compact Visual Concept Brief before the Panel Difference Map: protagonist or force, source-specific tension, turning point, ending image, one primary visual motif, and no more than two secondary motifs when they have distinct jobs.
- Treat every panel as a shot with a job. A valid page needs a deliberate camera plan, not a wide/medium/close crop ladder. Name the shot scale, camera height/angle, focal owner, visible action, and information delta for every panel.
- For an automatic sequence of three or more panels, use at least three distinct shot scales across the page (for example extreme wide/wide, medium, and close/detail). If the source is too sparse for a literal subject close-up, use a meaningful environment/detail/relationship shot instead.
- At least one panel must establish scale or place, at least one must change attention or reveal a response, and the ending must alter the meaning of a recurring object, color, shape, or space. A new crop, border, or color cast is not a beat.
- Reconstruct a compact Scene World Model from visible support surfaces, depth bands, landmark adjacency, routes, reflections, occlusions, and open camera corridors. Preserve those relationships whether the imagined camera remains source-aligned or moves to a source-consistent position.
- Build a Camera Opportunity Map rather than an angle quota. Consider level, low-angle, high-angle/overhead, side, reverse, over-shoulder, and object-level positions; use a relocated camera only when it adds narrative information, emotional force, spatial clarity, or visual beauty with sufficient scene evidence. A strong source-aligned view may remain when it is the best shot. The page must still avoid a crop-only ladder: differentiation may come from camera relocation, action/state change, focal-owner change, relationship reveal, motif transformation, or time beat.
- Build an Action Affordance Map from the visible pose, gaze, held objects, support/contact, wind, weather, and nearby routes. Under Adjacent Moment, vary at least one meaningful action or body/object state when the evidence supports it; do not freeze every panel at the photographed pose.
- Audit the opening and ending as a pair. If they share a shot scale or both show the whole scene, they must differ on at least four visible axes including camera side/height, focal owner, subject action, foreground/depth pattern, value/color structure, or motif meaning. Otherwise replace one instead of calling repetition an echo.

### Adaptive panel count

- Do not choose a target number first. List only beats that change state, change viewpoint meaningfully, or reveal new information; merge redundant beats; the remaining count becomes the panel count.
- Automatic sequence design uses at least 3 panels; most readable outputs naturally use 3–8. This is a legibility range, not a template. Exceed it only when the user asks or the output size can keep every panel readable.
- A 3-panel result must still form a complete minimum arc: establishment, meaningful change or reveal, and residue/echo. If the source cannot support those three distinct beats, reinterpret the moment through whole, relationship/detail, and changed echo rather than dropping to 2 panels or padding with repeated crops.
- If the user explicitly asks for exactly 2 images, treat it as a diptych/before-after comparison and route it away from this comic-sequence workflow.
- Each panel must have an independent information role. A new crop of the same pose is not a new beat.
- Adjacent panels should differ on at least three visible axes such as beat/time, shot scale, angle, subject scale, action, foreground, value pattern, color role, edge density, or panel geometry.

### Compact portrait page by default

- Unless the user explicitly requests another format, output one compact portrait page with exact width:height `2:3`. Interpret a user's “竖屏 3:2” as portrait `2:3`, not landscape `3:2`, `4:5`, `9:16`, or an open-ended scroll.
- For four or more panels, use a genuinely two-dimensional page topology: at least two columns, a staggered masonry structure, or a dominant panel with supporting split/inset panels. The reading path must travel laterally as well as downward.
- Prohibit the default failure pattern of one full-width panel after another. Do not make a single-column webtoon, five horizontal bands, a long vertical strip, or an extra-tall canvas unless the user explicitly asks for scroll format.
- On pages of five or more panels, use at least three panel-aspect families when content permits: one vertical, one horizontal, and one square-ish or irregular panel. No more than two panels may span the full page width, and no more than two full-width panels may appear consecutively.
- Give the turning point the dominant area, then fit supporting beats into adjacent page zones. Gutters should organize a compact print-page rhythm, not accumulate vertical length.

### Continuity and invention are separate controls

- Preserve identity, subject count, relationships, signature clothing/objects, defining landmark topology, and recurring color cues across the sequence.
- A subject may be intentionally out of frame, but do not accidentally add, merge, swap, or delete people, limbs, pets, props, architecture, or landmarks.
- Default narrative permission is **Adjacent Moment**: plausible before/during/after beats grounded in visible evidence. Use **Held Moment** when documentary fidelity is requested and **Poetic Expansion** only when the user invites metaphor or surrealism.
- Never present an inferred location, identity, date, hidden object, dialogue, or event as an observed fact.
- Continuity protects the world, not the original lens. Do not assume the source viewpoint must either be preserved or changed: let the Camera Opportunity Map choose what tells the story most clearly and beautifully. New views may reveal only source-supported relationships; keep uncertain or hidden areas simplified, occluded, or out of frame rather than inventing specific facts.

### Salient props and motifs receive authorship

- Inventory source-visible handheld objects, wearables/contact details, landmarks, and optical/surface echoes such as reflections or shadows. Select one primary motif and optionally up to two secondary motifs only when they strengthen the theme, visual tension, or spatial continuity. Do not force a prop arc when the source has no useful candidate.
- Build a Prop/Motif Bible for every selected item: observed count, silhouette and proportions, visible component stack, material, color/pattern, attachment or contact, location/orientation, source-supported states, and occluded unknowns. A prop is not continuous merely because a vaguely similar object appears.
- For an ambiguous but salient object, record its visible form and plausible readings separately. Use one source-consistent, fact-neutral visual interpretation throughout the page, or honor the user's explicit identification. Never let one panel treat the same item as a rod, another as a sword, and another as unrelated decoration; keep unobserved components hidden.
- The primary motif should normally appear in at least two panels and receive one object-led or relationship-led panel when the source and panel count support it. Magnification must reveal construction, contact, material, reflection, scale, motion, or changed meaning—not just crop closer.
- Allocate detail hierarchically: distant appearances may simplify texture but must retain the recognition silhouette and component proportions; a close or dominant prop panel must reveal more coherent structure and material information than the distant views. Panel scale may exaggerate graphic presence, never redesign the object.
- Give secondary motifs separate functions. A handheld prop may carry action, a shoe or strap may explain body-to-place contact, a landmark may stabilize scale/direction, and a reflection may transform meaning. Omit any secondary motif that only adds clutter.

### Original trend-aware style

- Build style from observable decisions: line, value, color, anatomy/shape, texture, and layout rhythm.
- Treat an explicit user preference or user-supplied style-calibration page as higher priority than automatic trend selection. Extract a reusable Style Fingerprint from visible decisions; do not copy its characters, objects, composition, page skeleton, logos, or protected fictional world.
- Current popular works may inform abstract traits, never the final prompt's artist/franchise name, exact character design, signature motif, page layout, logo, or protected fictional world.
- If the user requests an exact living-artist or franchise style, acknowledge the reference and translate it into a distinct combination of broad traits.
- Unless the user explicitly asks to use another supplied image as a generation reference, attach only the source photograph. Public comic images used during research remain analysis-only.

### Default painterly comic-animation house style

- When the user does not explicitly request monochrome, pencil, watercolor, flat cel, line art, or another medium, use **Painterly Comic Animation** as the stable default. It combines a readable anime/comic page with authored painterly colour, planes, marks, and light; it is not photorealistic painterly rendering. Sequence authorship always outranks single-frame painterly preservation.
- Read [references/painterly-comic-adapter.md](references/painterly-comic-adapter.md) and freeze one rendering-only Style Fingerprint and Completion Lock across every panel: exact portrait `2:3` page geometry; area-adaptive interlocking colour masses; three broad value groups; scene-owned colour roles; reconstructed graphic shapes; faceted planes; connected brush fields; shared boundary illumination; material-specific marks; focal/support/context edge hierarchy; selective structural contours; and identity-faithful anime facial proportions. Do not inherit the source photo's pixel ratio, crop, headroom, subject placement, horizon, pose, head axis, gaze, expression, or camera as painterly locks.
- Colour masses and value groups must organize the page before line detail at thumbnail size. The surface must be fully authored, but not reduced to rigid cel bands: use internal colour turns and plane changes to describe volume. Avoid pasted cutouts, unpainted photo regions, and a single global brush/noise overlay.
- Keep one coherent time/weather and palette family across panels, while allowing panel-specific exposure emphasis, value ownership, and warm/cool balance when the beat or camera position benefits. Preserve the page's dominant field, structural counter, focal accent, and neutral bridge without forcing identical colour-area distribution in every panel.
- Connect adjacent forms with related brush direction, temperature, value, and shared illumination. Use different mark grammars for hair, cloth, skin, grass, stone, water, cloud, and metal. Edges are sharpest at the focal owner, controlled in support areas, and softer only in contextual depth or atmosphere.
- Simplify faces into designed anime planes while preserving identity-bearing facial proportions, relative feature spacing, hair mass, and recurring character cues. Head axis, eye-line, gaze, expression, body pose, and hand state are panel-specific performance variables chosen by the storyboard; they must change intentionally rather than drift accidentally. Match character and environment completion; never place a clean anime figure over a photographic, sketchy, or unrelated painterly plate.
- A user-requested alternate medium overrides this house style, but it still requires one explicit Style Fingerprint and one Completion Lock across the whole page. Do not force painterly colour onto an explicit black-and-white or flat-cel request.

### Alternate finished-color cel-comic mode

- When the user explicitly requests flat cel, opaque hard-edge fills, or the earlier `Finished Luminous Cel Comic` direction, use that mode instead: medium-dark structural contours, complete opaque fills, two to four grouped cel value steps, simplified anime anatomy, fully coloured backgrounds, local material texture, and clean light gutters.
- Keep the same page, sequence, camera, motif, and continuity contracts. This alternate mode must not silently become lineart, watercolor, semi-photoreal rendering, or a mixed-finish page.

### Comic transformation, not photo treatment

- “Comic”, “manga”, or “anime” means a visible redraw with an authored visual grammar, not a photographic grade. For the painterly default, choose at least four concrete operations from: selective structural contours, simplified anime planes, three-group value design, scene-owned colour roles, faceted shape reconstruction, connected brush fields, material-specific marks, focal/context edge hierarchy, graphic silhouette or perspective exaggeration, and page-level panel rhythm. For the alternate flat-cel mode, use grouped cel values and opaque hard-edge fills instead of painterly turns.
- Keep one Style Bible, Style Fingerprint, and Completion Lock across the page, and make the transformation legible at thumbnail size. If the result could be mistaken for the original photo with a filter, pasted colour blocks, a softly tinted line drawing, global painterly texture, or a mixture of sketch and rendered panels, fail the comic-transformation gate and rebuild the authored masses, planes, brush continuity, line hierarchy, shape language, and material finish.

### Text discipline

- Default to wordless visual storytelling: no dialogue, captions, title, legible signs, watermark, or generated lettering.
- If the user explicitly supplies or requests exact text, keep it short, reserve clean balloons/caption areas, and verify every character. If the active image workflow cannot render exact text reliably, return a wordless page and state the limitation instead of accepting gibberish.

## Workflow

1. Determine the route, output form, reading direction, and whether current-style research is needed. Default to one compact portrait `2:3` page; only an explicit user format request may replace that canvas contract. Infer safe defaults instead of asking taste questions that the photo can answer.
2. Inspect the source with the available image viewer. Build the Source Story Card, Scene World Model, Action Affordance Map, and salient Prop/Motif Inventory, separating observed evidence, inference, protected anchors, creative opportunities, ambiguity, and source limitations.
3. Choose Held Moment, Adjacent Moment, or explicitly authorized Poetic Expansion. Write one theme proposition and one state-change line.
4. Write the Visual Concept Brief, select one primary motif and up to two useful secondary motifs, and build their Prop/Motif Bibles. Generate a beat pool, remove beats without narrative delta, and let the survivors set the panel count. Build the Panel Difference Map, Prop Presence Matrix, and Continuity Bible.
5. Convert the beat map into a camera, motif, and compact-page plan: enforce distinct shot scales, nonrepeating information roles, one dominant panel, one meaningful prop/relationship reveal when a primary motif is selected, and a visibly different opening/ending pair. Evaluate level, low, high/overhead, side, reverse, over-shoulder, and object-level cameras by narrative gain, aesthetic gain, and scene confidence; use only the moves that help, and record why any source-aligned view remains. For four or more panels, assign every panel a page zone, column span, aspect family, motif role, and detail level, then verify a lateral-plus-downward reading path on the portrait `2:3` canvas. Let panel area and gutter size express narrative and motif weight, not an equal grid or full-width vertical stack.
6. Resolve style priority: explicit user preference or medium request first, then the Painterly Comic Animation house default, then current trend evidence only for compatible abstract refinements. Resolve the six style axes and four or more concrete comic transformation operations; write one Style Bible, one Style Fingerprint, and one Completion Lock shared by every panel.
7. Compile one priority-ordered source-aware prompt. Describe every panel’s role, camera decision, action, value/color job, and transition, then state the fixed page geometry and the painterly colour-mass, value-group, plane, brush-continuity, shared-light, material, edge, face-identity, background-completion, border, and anti-filter contracts once for the whole page. If flat cel is explicitly requested, substitute its alternate completion lock.
8. Run the preflight veto: reject any prompt that could return a single frame; has fewer than three visible panels; lacks a specific state change; copies the source pose/composition into every panel; uses fewer than three shot scales; contains only crop/zoom differences; forces arbitrary camera moves with no narrative or aesthetic gain; describes only a photo filter; permits a lineart-dominant, pasted-block, global-texture, uniform-blur, or mixed-finish page without an explicit user override; omits the exact portrait `2:3` canvas; allows a four-plus-panel single-column/full-width stack; or leaves a selected primary motif without a stable construction key, meaningful reveal, recurrence, and cross-panel detail hierarchy. Then use the real image generation/editing mechanism once with the photo attached through its actual image-input path. Generate one page by default.
9. Inspect source and result at thumbnail, panel, and detail scale. The result must pass world continuity, prop/motif construction and material continuity, camera/action invention, bookend contrast, compact-page geometry, comic-transformation, painterly continuity or explicit alternate-medium completion, cross-panel Style Fingerprint, and authored-sequence gates.
10. If one module fails, make at most one targeted correction that preserves successful modules. If it still fails, return the best inspected result and name the exact limitation.

## Decision Priority

1. User request, consent, privacy, and image-role boundaries
2. Identity, count, relationships, Prop/Motif Bibles, protected text, and scene-world topology
3. One source-specific theme and credible narrative permission
4. Multi-panel narrative, panel roles, state change, shot-scale hierarchy, reading flow, and visible differentiation
5. Story-driven camera/action choices plus cross-panel identity, prop, and scene-world continuity
6. Rendering-only Style Fingerprint: painterly colour-mass, value, plane, brush, material, edge, contour, and finish authorship (or the explicit alternate-medium lock)
7. Optional effects, balloons, or decoration

## Output Contract

- **Create:** exactly one finished inspected comic page containing at least three visibly separated panels, defaulting to a compact portrait `2:3` multi-column layout, plus a concise Chinese note stating the theme, chosen style direction, and why the panel count/camera choices fit the source. Never return a single-frame painterly illustration under this route. Do not expose the full internal prompt unless asked.
- **Prompt-only:** Source Story Card summary, narrative permission, theme, panel count rationale, Prop/Motif Bible and Presence Matrix, Panel Difference Map, Style Bible, Style Fingerprint, Completion Lock, one tool-ready prompt, and `No image was generated or visually verified.`
- **Review:** report `Source continuity` and `Sequence authorship` separately, name critical failures, and give one targeted correction plan.
