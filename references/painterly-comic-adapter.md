# Painterly Comic Animation Adapter

This adapter translates the abstract control methods of the public `painterly-frame` workflow into a self-contained rule set for source-grounded comic pages. It is an original adaptation for this Skill, not an external runtime dependency and not a request to imitate a particular artist, franchise, or existing frame.

## Rendering-only boundary

`photo-to-comic` owns the page: the source photo becomes semantic scene/story evidence, the beats determine the number of panels, the camera plan chooses shots, the motif system assigns object-led details, and the page remains a compact portrait `2:3` mosaic. This adapter owns only how each panel is painted and how that painted language stays coherent across panels.

Never treat the source photograph as a `painterly-frame` Edit Target inside this Skill. Do not import source-ratio inheritance, Preserve-and-enrich composition lock, crop/headroom, original subject placement or scale, original horizon/quiet-space distribution, photographed pose, head axis, gaze, expression, or camera position. Those are single-frame controls and would suppress comic narration.

Do not trade away panel storytelling for a painterly surface. A painterly page with five near-identical crops is still a failed comic sequence. Conversely, a varied sequence with unrelated brush treatments is a failed style lock.

## Page lock, not source-composition lock

Freeze the outer page contract before rendering:

- exact portrait `2:3` canvas by default;
- at least three panels, with two-dimensional multi-column reading for four or more;
- dominant panel, supporting panels, gutters, and lateral reading moves are authored by the sequence engine;
- the source camera is one optional shot, not a crop template or protected anchor;
- each panel keeps its own aspect family and shot role, while the page topology stays legible at thumbnail size.

Within the scene-world, preserve truth anchors such as identity, subject count, signature clothing/objects, ownership/contact, landmark recognizability, and enough spatial logic to keep the location coherent. Do not preserve the source distribution as a panel template. Each beat may recompose subject placement, pose, gaze, expression, scale, foreground, horizon, depth pattern, and visible environment from a source-consistent camera.

Build a Camera Opportunity Map rather than copying the single-frame directorial lock. Consider level, low-angle, high-angle/overhead, side, reverse, over-shoulder, and object-level positions. Score each candidate for `narrative gain`, `aesthetic gain`, and `scene confidence`; use it only when the gain is real. Keeping one effective source-aligned view is allowed. Forcing a low/high/reverse angle merely to satisfy variety is a failure, as is making every panel a crop of the source.

## Colour and value lock

Before line detail, author a colour map for the whole page and carry its roles through every panel:

1. Use an area-adaptive mass budget: a dominant/large panel can carry roughly `5–9` interlocking colour masses; a small support panel may use `3–6`. Recompose the masses for each shot rather than preserving the source's colour-area geometry.
2. Organize the page into three broad value groups—light, middle, dark—then allow local turns inside those groups. Avoid continuous photographic shading and avoid a single dark wash over the whole page.
3. Assign spatial colour roles: `dominant field`, `structural counter`, `focal accent`, and `neutral bridge`; add one controlled collision only if the theme needs it. The focal accent should own the primary contrast axis, not every panel equally.
4. Keep one coherent time/weather and palette family, but allow panel-specific exposure emphasis, value ownership, and warm/cool balance when the narrative beat, camera position, or focal owner benefits. Do not require identical colour areas or one unchanging exposure map.
5. Protect source-derived local colours that carry identity or motif meaning—hair, clothing, umbrella, strap, shoe, tower, water reflection, or another selected object—while simplifying unimportant micro-colour noise.

## Painted-animation render contract

Use a comic-readable painted field rather than a flat cel filter or an unstructured oil texture:

- reconstruct silhouettes and large planes with deliberate graphic shapes and selective foreshortening;
- use faceted planes and internal colour turns to describe volume; do not rely on outlines alone;
- connect neighbouring forms with related brush direction, temperature, and value so the panel reads as one field;
- bind adjacent forms with shared illumination at boundaries; avoid a subject that looks pasted over a background;
- reserve the crispest edges and highest local contrast for the focal owner, keep support edges controlled, and soften only contextual depth or atmosphere;
- give materials their own mark grammar: hair locks, cloth folds, wet stone, grass, metal, water, cloud, and skin each receive different mark scale and direction;
- keep structural contours selective and subordinate to painted masses; they clarify overlap, expression, prop construction, and important silhouette turns;
- complete both character and environment to the same authored finish level; never leave a sketchy background behind a rendered figure.

The desired medium is a **Painterly Comic Animation**: readable anime/comic anatomy and page rhythm, with authored painterly colour, planes, marks, and light. It is not photorealistic painterly rendering, a global canvas filter, a photo underpainting, or a rigid two-to-four-band cel pass.

## Face identity versus panel performance

When a face appears, preserve identity-bearing structure: face proportions, relative feature spacing, hair mass, recurring character cues, and age impression when evident. Head axis, eye-line, gaze direction, expression, mouth state, and head turn are storyboard-controlled performance variables and may change between panels to express the beat. Distinguish intentional performance change from accidental identity drift. A close panel may clarify eyelids, hair locks, wetness, or light, but cannot redraw the person as a different character.

## Cross-panel continuity packet

Freeze these fields before the first generation and reuse them in every panel:

```yaml
style_name: Painterly Comic Animation
page_ratio: portrait 2:3, independent of source ratio
macro_colour_masses: dominant panel 5-9 / small support panel 3-6
value_groups: 3 broad groups
exposure_continuity: one time/weather family with panel-specific emphasis allowed
colour_roles: dominant field / structural counter / focal accent / neutral bridge
plane_language: reconstructed graphic shapes plus faceted planes
brush_continuity: connected neighbouring fields
illumination: shared light at form boundaries
material_grammar: local marks by material, not global texture
edge_hierarchy: focal sharp / support controlled / context softer
line_role: selective structural contour, subordinate to painted masses
face_identity_guard: face proportions / relative feature spacing / hair mass / recurring cues
panel_performance_variables: head axis / eye-line / gaze / expression / pose / hand state
panel_finish: same painted completion family across all panels
```

Panel differences may come from shot scale, camera position/height, action, foreground, focal owner, motif state, panel geometry, or narrative meaning—not from changing the medium. Camera relocation is optional when it helps; shot-scale and information-role differences are not. A detail panel can use denser marks and sharper edges while keeping the same colour, plane, brush, and material family.

## Anti-filter and anti-sticker checks

Reject or target-correct the page when any of these are visible:

- the original photo is still recognizable as a filtered underpainting;
- large colour regions are flat pasted blocks with no plane turns, shared light, or boundary binding;
- a global brush/noise/film texture is applied equally to sky, face, cloth, stone, and water;
- every edge is equally sharp, equally soft, or uniformly blurred;
- the face is line-clean but the background is photographic, or one panel is sketchy while another is fully painted;
- painterly surface language has erased the comic page's shot hierarchy, gutters, motif reveal, or camera invention;
- the result is one painterly hero image, a borderless single frame, or fewer than three visible panels;
- every panel preserves the source camera, composition, pose, gaze, and environment distribution as if the photo were an Edit Target;
- a selected prop changes material, hardware, count, attachment, or semantic identity between panels.

## Prompt seed

When compiling the image prompt, use one compact clause such as:

> Create one portrait 2:3 comic page with at least three visible panels. Treat Image 1 as semantic scene/story evidence, never as an Edit Target: do not inherit its ratio, composition, subject placement, pose, gaze, horizon, or camera as locks. Let each beat choose its own shot scale and, when useful, a level, low, high/overhead, side, reverse, over-shoulder, or object-level camera. Render every panel in one Painterly Comic Animation system: area-adaptive interlocking colour masses, three broad value groups, scene-owned colour roles, reconstructed graphic shapes and faceted planes, connected neighbouring brush fields with shared illumination, material-specific marks, focal-sharp/support-controlled/context-soft edges, selective structural contours, identity-faithful facial proportions, and one consistent completion family; no single-frame result, crop-only sequence, flat cel-band-only surface, pasted cutouts, global texture overlay, photo filter, uniform blur, or lineart-dominant finish.
