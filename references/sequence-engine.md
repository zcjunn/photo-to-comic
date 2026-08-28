# Adaptive Sequence Engine

Read for every Create or Prompt-only route. Design narrative first; panel count is a consequence.

## Reconstruct the Scene World

Before choosing shots, convert the Source Story Card into a coarse scene-world rather than treating the photograph as the only legal composition.

```yaml
source_camera: the observed camera side, height, distance, and dominant sight line
support_and_depth: subject supports plus near/mid/far bands
adjacency_and_routes: what borders, overlaps, leads toward, or sits behind what
camera_corridors: plausible low / high / side / reverse / over-shoulder / object-POV / overhead positions
uncertain_zones: hidden detail that must stay simplified, occluded, or out of frame
```

The source proves relationships, not a full 3D set. Move the camera only through supported corridors. Preserve landmark order and contact; do not invent specific hidden structures to complete a reverse view.

Build a Camera Opportunity Map instead of a viewpoint quota:

```yaml
camera_candidates:
  - mode: source-aligned / level-relocated / low / high-or-overhead / side / reverse / over-shoulder / object-level
    narrative_gain: none / low / medium / high
    aesthetic_gain: none / low / medium / high
    scene_confidence: low / medium / high
    decision: use / reject / keep source-aligned
    reason: what new relationship, emotion, scale, or visual structure this camera contributes
```

- Use a relocated camera only when it has positive narrative or aesthetic gain and adequate scene confidence.
- A strong source-aligned view may remain when it is the most effective shot; do not force low/high/reverse angles as a checklist.
- The page still cannot be a crop ladder. When camera relocation is not useful, create information gain through action/state change, focal-owner change, relationship/detail reveal, motif transformation, foreground, or time beat.

## Build the Action Affordance Map

List small changes supported by pose, gaze, held objects, support/contact, weather, reflections, and visible routes. Examples include turning the head, changing grip, tilting a held object, shifting weight, looking toward a reflection, or allowing hair/cloth/grass to answer wind.

- Under Held Moment, keep the action state fixed and create difference through shot scale, relation, detail, focal owner, foreground, value ownership, panel geometry, or an earned camera change.
- Under Adjacent Moment, a page of four or more panels should include at least one meaningful source-supported action or prop-state change when the evidence allows it.
- Under Poetic Expansion, nonliteral movement still needs the same identity and scene anchors.
- A new action or pose may improve staging and beauty, but it must remain physically plausible, preserve identity/contact, and support the beat rather than becoming unrelated fashion posing.

## Visual Concept Brief

Before listing panels, write five short lines:

```yaml
theme: one source-specific proposition, not a mood label
central_force: the person, object, relationship, weather, or scale conflict carrying the page
turning_point: the moment attention, meaning, or power changes
ending_image: the final visual residue or changed echo
recurring_motif: one source-derived color, shape, object, gesture, or spatial line
secondary_motifs: zero to two source-derived carriers with distinct jobs
```

The brief prevents the page from becoming a contact sheet. Every beat must either move the central force toward the turning point or change how the recurring motif is understood. If a panel cannot be explained by that brief, delete or redesign it.

## Prop and Motif Orchestration

Use the Salient Prop and Motif Inventory from the Source Story Card before finalizing beats.

### Select and assign roles

- Choose one primary motif only when it materially supports the theme, page silhouette, action, or spatial tension. Add at most two secondary motifs, each with a different job.
- Common roles are: `action carrier` for a held or movable object; `contact witness` for shoes, hands, straps, or support; `scale/direction anchor` for towers, doors, vehicles, or repeated architecture; and `optical echo` for reflection, shadow, water, or glass.
- If no candidate earns a role, do not manufacture a prop subplot. People, weather, space, or light may remain the central force.

### Build a prop arc, not a catalog

For a selected primary motif, design at least two appearances when the panel count and source support them:

1. **Establish:** make the recognition silhouette, location, ownership/contact, or scale relationship legible.
2. **Reveal or magnify:** dedicate an object-led or relationship-led panel to one new layer—component construction, hand/foot contact, material response, optical reflection, motion state, or landmark scale.
3. **Altered echo — optional:** return the motif through a changed action, viewpoint, reflection, shadow, absence, or scale so its meaning changes.

Do not force all three stages when two strong appearances complete the thought. A magnified panel that only crops closer without revealing new structure, material, contact, scale, or meaning has no narrative delta.

### Detail and screen-space budget

- Give the primary motif enough area or local contrast to be recognized at thumbnail size and enough close/medium coverage to establish coherent construction.
- Distant appearances may merge minor texture, but they must keep the same recognition silhouette, major proportions, component order, color/pattern, and contact logic.
- A close panel must increase information: clearer component joins, material behavior, wear, reflection, droplets, grip, support, or scale evidence. It must not be less finished than the background version.
- Perspective exaggeration may enlarge a prop for graphic tension, but it may not change what parts exist, reverse attachment, mutate the material, or add decorative hardware.

### Prop Presence Matrix

Create this beside the Panel Difference Map:

```yaml
selected_motifs:
  - motif_id: stable label
    role: primary / secondary
    construction_key: concise recognition silhouette plus visible component stack
    material_key: visible material, finish, pattern, and edge response
    semantic_lock: confirmed identity / user-identified / stable fact-neutral visual reading
panels:
  - id: P1
    motif_presence: visible / reflected / shadowed / intentionally absent
    motif_job: establish / construction reveal / contact / material / scale anchor / altered echo
    screen_scale: background / supporting / focal / extreme detail
    visible_components: what is actually shown
    state_and_orientation: permitted change only
    contact_or_reflection: physical or optical relation
    detail_level: recognition / structure / material
    continuity_note: count, occlusion, or topology protection
```

Freeze the construction and material keys across the page. Vary only permitted state, viewpoint, scale, contact, reflection, or narrative meaning.

## Build a Beat Pool

Generate only source-relevant candidates:

- **Orientation:** establish place, scale, relation, or weather.
- **Attention:** reveal where a person, animal, or viewer looks.
- **Preparation:** a hand, foot, tool, vehicle, door, or body shifts before action.
- **Action:** the clearest visible or source-consistent movement.
- **Reaction:** another subject, environment, reflection, or object answers the action.
- **Detail:** a small clue changes interpretation rather than merely showing texture.
- **Counterpoint:** foreground/background or large/small information creates tension.
- **Aftermath:** a trace remains after the action.
- **Echo:** the final panel returns to a shape, color, object, or space with changed meaning.
- **Metaphor:** only in Poetic Expansion; one source-derived nonliteral beat.

For each candidate, write its `narrative_delta`: what changes or becomes newly knowable. Delete candidates with no delta.

## Let Beats Set the Panel Count

- Minimum is three panels because this skill creates a comic group with a readable arc, not a diptych.
- A three-panel minimum must contain three necessary roles: establishment, meaningful change or reveal, and residue/echo. For a simple portrait, object, or landscape, derive these through whole, relationship/detail, and changed echo without inventing a large event.
- A clear gesture, journey, interaction, or small event may support four to six beats.
- A dense multi-subject scene may support seven or eight beats if each person/beat remains readable.
- Nine or more panels require explicit user intent or enough output resolution; otherwise merge minor beats.

Never let automatic design fall to two panels. If a user explicitly requests exactly two, route the task as a diptych or before/after comparison rather than weakening this sequence contract.

Do not pad. Do not force setup–action–reaction when the photograph supports a quieter structure. Do not split one pose into multiple crops and call it pacing.

## Camera Grammar Contract

Treat the panel map as a storyboard, not a crop recipe. Use these as defaults and adapt them to the source:

| Narrative job | Useful camera choices | What must change in the image |
|---|---|---|
| Orientation / scale | extreme wide, wide, high or distant level view | place, depth bands, and subject-to-environment ratio |
| Attention / preparation | medium, over-shoulder, low or canted view | gaze, gesture, leading line, or imminent action |
| Detail / clue | close or extreme detail, object POV, partial occlusion | a new object relationship, texture clue, or value contrast |
| Reaction / reveal | telephoto, reverse angle, subject-to-subject view | another source-visible subject or environmental response |
| Aftermath / echo | changed wide, overhead, or negative-space composition | the same motif returns with changed meaning |

Hard requirements for automatic sequences:

- Use at least three distinct shot scales across any page of three or more panels. A three-panel page must not be a simple wide/medium/close crop ladder; each scale must carry a different beat and focal owner.
- Give every panel an independent information role and use multiple focal owners when the source permits: for example landmark/space, person/gesture, object/detail, animal/reaction, or environmental trace. Do not make every panel subject-centered.
- Treat level, low-angle, high-angle/overhead, side, reverse, over-shoulder, and object-level cameras as candidates, not quotas. Choose them when they strengthen narrative, spatial clarity, emotional force, or visual beauty; reject them when they only add arbitrary novelty.
- The source photograph's exact composition may appear once when it is the strongest shot. Its general camera direction may recur when useful, but each panel must be genuinely re-staged; multiple crops, tints, textures, or zooms without a new narrative delta are failures.
- If the source is a sparse landscape or still life, achieve shot diversity through scale, topographic angle, detail/relationship, foreground occlusion, and negative space; do not invent a protagonist or event merely to create coverage.
- If no relocated camera earns a place, document that choice and make the sequence distinct through beat, action/state, focal relationship, motif meaning, value ownership, and panel geometry. “No forced angle change” never permits a crop-only page.

## Opening and Ending Contrast

The ending is not another establishment shot. Compare P1 and PN before prompting.

- If they share the same shot scale, require at least four visible differences among: camera side/height, subject scale, focal owner, action/pose, foreground or occlusion, depth-line direction, value/color ownership, panel geometry, and motif meaning.
- If both show the whole scene, the final panel must reveal a changed relationship or use a different spatial proposition such as reverse/over-shoulder, overhead, object POV, emptied space, or a transformed action state.
- A deliberate visual rhyme is allowed only when the recurring motif changes meaning and the two panels remain distinguishable at thumbnail size.
- If the last panel can be swapped with the first without changing the story, replace one of them.

## Comic Transformation Contract

The final page must visibly redraw the source. Select at least four of these operations in the Style Bible and prompt:

- deliberate ink or contour behavior rather than photographic edges;
- simplified, designed shapes or gently stylized anatomy while preserving identity;
- grouped cel-shaded or graphic value masses instead of continuous photo shading;
- limited palette roles with one controlled focal accent;
- a primary material system such as screentone, dry brush, pencil, or printed paper grain;
- authored silhouette, perspective exaggeration, or selective foreshortening;
- panel/gutter rhythm that participates in the storytelling.

Reject any direction described only as cinematic color grading, lens effects, HDR, film grain, or “make it look like a comic.” If a generated panel still reads as the original photograph with a filter, rebuild the line, value grouping, shape language, and material finish before changing decorative effects.

## Style Fingerprint and Painterly Completion Lock

Style is not allowed to re-roll independently for each photograph or panel. Build the Panel Difference Map and Camera Opportunity Map first; then compile the Painterly Comic Animation fingerprint from `style-research.md` and `painterly-comic-adapter.md` around those authored shots. The rendering system serves the sequence and may not overwrite its cameras, poses, performances, or panel geometry.

```yaml
style_fingerprint:
  contour_hierarchy: selective structural contours; thinner interior marks; line never the whole surface
  macro_colour_masses: 5-9 in a dominant panel; 3-6 in a small support panel; always area-adaptive
  value_groups: 3 broad light/middle/dark groups with local colour turns
  colour_roles: dominant field / structural counter / focal accent / neutral bridge
  face_and_anatomy: simplified identity-faithful anime planes; facial proportions, relative feature spacing, age cues, and hair mass guarded
  shape_and_plane: reconstructed graphic silhouettes and faceted planes
  brush_continuity: connected neighbouring brush fields with shared boundary illumination
  material_texture: local mark grammar by material, never global texture
  edge_hierarchy: focal sharp / support controlled / context softer
  background_finish: fully painted, simplified, same completion family as character
  border_gutter_language: stable medium-dark frames and clean light gutters
completion_lock:
  painterly_default_active: true unless explicitly overridden
  page_ratio: exact portrait 2:3 compact mosaic
  scene_light_family: coherent time, weather, and palette family; panel exposure/value emphasis may vary
  source_ratio_inherited: false
  source_composition_or_pose_locked: false
  line_is_structure_not_surface: true
  character_background_finish_match: true
  global_texture_overlay: false
  flat_cel_band_only: false
  photo_filter_or_underpainting: false
  face_identity_guard: true
  panel_performance_can_change: true
  panel_finish_drift: false
```

- Let the source change hue roles, focal accent, weather, and energy. Preserve one palette family, three-value logic, plane language, brush continuity, material hierarchy, and identity model, while adapting mass count, value ownership, exposure emphasis, and image-space light pattern to each panel's size and camera.
- At thumbnail size, the page must be organized first by interlocking colour/value shapes. A dominant panel may need `5-9` major masses while a small support panel may need only `3-6`. Detail panels may carry denser bristles, cracks, droplets, seams, or hardware, but all panels keep the same palette family and completion language.
- Connect neighbouring forms with related brush direction, temperature, value, and shared illumination. Keep edges sharpest at the focal owner, controlled in support areas, and softer only in contextual depth or atmosphere.
- Reject flat pasted colour blocks, global oil/noise texture, uniform blur, photo underpainting, lineart-only panels, and clean anime figures over photographic backgrounds.
- If the user explicitly requests flat cel, opaque hard-edge, black-and-white, pencil, watercolor, or another medium, replace this fingerprint with the requested medium's explicit Completion Lock while preserving the page and sequence contracts.

## Panel Difference Map

Build this before prompting:

```yaml
canvas_ratio: portrait 2:3 by default / explicit user override
reading_direction: left-to-right page by default / right-to-left when requested / scroll only when explicitly requested
page_shape: compact portrait print page by default / explicit alternate format
panels:
  - id: P1
    beat_role: orientation / attention / preparation / action / reaction / detail / counterpoint / aftermath / echo
    narrative_delta: what changes or is revealed
    shot_scale: extreme wide / wide / medium / close / extreme detail
    angle: level / high / low / overhead / canted / side / reverse / over-shoulder / object POV
    viewpoint_mode: source-aligned / relocated-source-consistent
    camera_decision: use / reject / keep source-aligned
    narrative_gain: none / low / medium / high
    aesthetic_gain: none / low / medium / high
    scene_confidence: low / medium / high
    camera_corridor: where the imagined camera is relative to the source camera and subjects
    viewpoint_evidence: visible topology that makes this position plausible
    focal_owner: subject, object, landmark, or void
    prop_motif_owner: selected motif or none
    prop_motif_job: establish / construction reveal / contact / material / scale anchor / altered echo / context only
    prop_screen_scale: background / supporting / focal / extreme detail
    visible_prop_components: source-supported parts actually shown
    prop_state_contact_reflection: permitted state and physical or optical relation
    prop_detail_level: recognition / structure / material
    visible_action: one primary action
    action_evidence: visible pose, held object, support, route, weather, reflection, or none for Held Moment
    foreground_or_occlusion: none or one meaningful device
    value_shape: dominant light/dark grouping
    color_role: dominant, structural, focal accent, or quiet field
    edge_texture: focal and context behavior
    panel_geometry: relative size and shape
    page_zone: top-left / top-right / middle-left / middle-right / bottom-left / bottom-right / spanning named zones
    column_span: one column / partial span / full width
    panel_aspect: vertical / horizontal / square-ish / irregular
    full_width: true / false
    transition_from_previous: moment-to-moment / action-to-action / subject-to-subject / scene-to-scene / aspect-to-aspect / non-sequitur-poetic
```

Every adjacent pair should differ on at least three visible axes. Across the whole page, avoid repeating the same shot scale, face size, camera height, centered pose, value map, and panel geometry unless repetition itself is the theme.

Before prompting, run this compact audit:

```yaml
distinct_shot_scales: 3 or more
distinct_focal_owners: 3 or more when source permits
same_composition_reused: false
camera_opportunity_map_completed: true
camera_variation_is_story_driven: true
forced_angle_quota: false
crop_only_panels: false
comic_transformation_operations: 4 or more
painterly_comic_default_active: true unless explicitly overridden
macro_colour_masses: dominant panel 5-9; small support panel 3-6
value_group_count: 3 broad groups
colour_roles_locked: true
connected_brush_fields: true
shared_boundary_illumination: true
faceted_plane_authorship: true
material_local_marks: true
edge_hierarchy_consistent: true
line_is_structure_not_surface: true
color_masses_dominate_lines_at_thumbnail: true
character_background_finish_match: true
flat_cel_only_or_semi_photoreal_drift: false
global_texture_overlay: false
photo_underpainting: false
face_identity_guard: true
panel_performance_can_change: true
source_aligned_view_allowed_when_best: true
source_composition_pose_or_gaze_repeated_in_every_panel: false
opening_ending_visible_differences: 4 or more when they share a scale
portrait_ratio_exact: 2:3 unless explicitly overridden
single_column_stack: false for 4+ panels unless scroll is explicitly requested
full_width_panel_count: 2 or fewer for 5+ panels
lateral_reading_moves: 2 or more for 5+ panels
panel_aspect_families: 3 or more for 5+ panels when content permits
primary_motif_recurrence: 2 or more when a primary motif is selected and source supports it
prop_or_relationship_led_panels: 1 or more when a primary motif is selected
prop_construction_or_material_drift: false
ambiguous_prop_semantic_switch: false
prop_detail_hierarchy: distant recognition < medium structure < close material information
```

If any line fails, redesign the beat map rather than adding effects to the prompt.

## Continuity Versus Difference

Hold constant across panels:

- identities, faces, hair, clothing layers/colors, accessories, pet markings;
- subject and object count unless an omission is intentional and documented;
- landmark order, support surfaces, recurring props, weather/time window;
- line family, palette roles, anatomy model, texture family, border/gutter language;
- Style Fingerprint and Completion Lock: area-adaptive macro colour masses, three-value logic, coherent time/weather/palette family, plane language, connected brush fields, shared illumination, edge hierarchy, identity-faithful face/hair simplification, background completion, and material-local marks (or the explicit alternate-medium lock);
- one recurring visual motif derived from the photo, if useful.
- selected prop recognition silhouettes, visible component stacks, count logic, materials/patterns, contact/attachment, semantic locks, and occluded unknowns.

Vary deliberately:

- time beat, action state, shot scale, camera position when useful, subject scale, crop, foreground, eye path;
- head axis, eye-line, gaze, expression, pose, hand state, and image-space light/value emphasis when the storyboard calls for them;
- panel size, gutter pause, value ownership, accent color placement, edge density;
- which part of the relationship is revealed.
- permitted prop state, orientation, screen scale, contact, reflection, material response, or motif meaning.

A style shift between panels is not meaningful differentiation. Keep one Style Bible.

## Layout and Reading Rhythm

- Choose reading direction from user or format. Default to left-to-right across a compact page; use right-to-left or scroll only when explicitly requested.
- Give the beat with the largest emotional or action delta the largest panel. A quiet aftermath may also own a large panel when negative space is the point.
- Use small gutters for continuous beat-to-beat action, medium gutters for slowdown, large gutters for scene/time change, and extra-large gaps only for deliberate delay or rupture.
- Use one dominant panel and supporting panels when the sequence has clear hierarchy. Use equal panels only when repetition, routine, comparison, or deadpan timing is the concept.
- Keep panel borders and gutters readable at thumbnail size. Broken borders, overlaps, or inset panels need a narrative reason.
- Maintain a clear entry point, one main reading path, and a final visual exit or residue. On four-plus-panel pages, the path must cross columns before descending again; a purely downward path is a failure unless scroll was requested.

## Compact 2:3 Page Architecture

The automatic canvas is exact portrait `2:3` (width:height). It should read as one compact printed comic page at thumbnail size, not a captured webtoon strip.

- Divide the page into two or three working columns and two or three height zones before assigning panels. Record `page_zone`, `column_span`, `panel_aspect`, and `full_width` for every panel.
- For four or more panels, use at least two columns or a deliberate inset/overlap topology. Do not stack every panel as a full-width horizontal band.
- For five or more panels, require at least two lateral reading moves and, when the content permits, three shape families: vertical, horizontal, and square-ish or irregular.
- No more than two panels may be full width on a five-plus-panel page, and no more than two full-width panels may appear consecutively. Prefer only one full-width panel when a dominant opening or closing beat needs it.
- Keep total gutters compact. White space may slow a beat, but it may not elongate the canvas beyond `2:3` or turn the page into a scroll.

Useful starting topologies, to be adapted rather than copied mechanically:

- **Three panels:** one dominant panel beside or above a split pair; never three identical full-width bands.
- **Four panels:** asymmetric `2 × 2` structure with one panel spanning two zones and three supporting panels.
- **Five panels:** top-left wide plus top-right vertical; middle-left detail plus middle/right dominant panel; offset bottom echo. The eye zigzags across the page instead of falling straight down.
- **Six to eight panels:** readable masonry with one dominant panel, medium support panels, and no column of tiny thumbnails.

## Page Shape

- Default to one portrait `2:3` page regardless of the source photo orientation.
- A landscape strip, square page, `4:5`, `9:16`, or tall scroll is allowed only when the user explicitly requests that output format.
- Even when the source contains vertical motion, express it inside the compact page through panel aspect, spanning, diagonal flow, or an inset rather than silently extending the canvas.
- Preserve source orientation only inside individual panels when it improves the sequence; the photo is evidence, not the output canvas contract.

## Difference Failure Examples

Reject or redesign when:

- every panel is the same portrait at wide/medium/close crop;
- camera angle, body pose, face direction, and value pattern stay unchanged;
- the same source photo appears as a literal repeated underpainting;
- every panel could be produced by cropping or zooming the source camera;
- the first and last panels repeat the same camera side, subject scale, focal hierarchy, and scene information;
- extra effects substitute for new story information;
- one panel introduces a new person, costume, landmark, or prop merely to create variety;
- the grid is uniform even though one beat clearly matters more;
- four or more panels form one vertical column, every panel spans the full width, or the page reads as several horizontal bands stacked from top to bottom;
- the output is taller than portrait `2:3`, resembles a `9:16` screenshot, or requires scrolling despite no explicit scroll request;
- five or more panels lack lateral reading movement or panel-aspect diversity;
- a selected primary prop remains a vague background mark and never receives an object/relationship-led reveal;
- an ambiguous form changes semantic category across panels, or its count, recognition silhouette, component stack, material, attachment, or orientation family drifts;
- a close prop panel reveals less coherent construction or material information than a distant appearance;
- every visible object receives equal emphasis, producing a catalog of decorative close-ups rather than a motif hierarchy;
- the panel count can be reduced without losing information.
