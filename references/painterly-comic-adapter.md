# Painterly Comic Animation Adapter

This adapter translates the abstract control methods of the public `painterly-frame` workflow into a self-contained rule set for source-grounded comic pages. It is an original adaptation for this Skill, not an external runtime dependency and not a request to imitate a particular artist, franchise, or existing frame.

## Rendering-only boundary

`photo-to-comic` owns the page: the source photo becomes semantic scene/story evidence, the beats determine the number of panels, the camera plan chooses shots, the motif system assigns object-led details, and the page remains a compact portrait `2:3` mosaic. This adapter owns only how each panel is painted and how that painted language stays coherent across panels.

Never treat the source photograph as a `painterly-frame` Edit Target inside this Skill. Do not import source-ratio inheritance, Preserve-and-enrich composition lock, crop/headroom, original subject placement or scale, original horizon/quiet-space distribution, photographed pose, head axis, gaze, expression, or camera position. Those are single-frame controls and would suppress comic narration.

Do not trade away panel storytelling for a painterly surface. A painterly page with five near-identical crops is still a failed comic sequence. Conversely, a varied sequence with unrelated brush treatments is a failed style lock.

## Style-dominance gate

The default medium must be unmistakable before the model receives the dense storyboard. Put a short style header within the first three prompt blocks:

> HAND-PAINTED ANIMATION COMIC PAGE. Build forms from interlocking opaque paint shapes, unequal colour turns, connected directional strokes, shared boundary light, and lost-and-found edges. This is not clean digital cel anime: no uniform complete outlines, no smooth two-band cel shading, no vector-clean surfaces, and no airbrushed commercial-anime finish.

This is not decorative negative prompting. It establishes the medium before `anime`, `contour`, `bright`, `high saturation`, or detailed panel descriptions can trigger a flat-cel prior. Use `stylized painted-animation facial proportions` for the character model; reserve `anime` wording for the user's explicit flat-cel request or for high-level readability discussion outside the production prompt.

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
- keep structural contours sparse, broken, and subordinate to painted masses; they clarify overlap, expression, prop construction, and important silhouette turns, then taper, break, or disappear into shared light elsewhere;
- complete both character and environment to the same authored finish level; never leave a sketchy background behind a rendered figure.

The desired medium is a **Painterly Comic Animation**: readable stylized-animation anatomy and comic-page rhythm, with authored painterly colour, planes, marks, and light. It is not photorealistic painterly rendering, clean digital cel anime, a global canvas filter, a photo underpainting, or a rigid two-to-four-band cel pass.

## Material Paint Proof Map

Before the final prompt, derive paint behavior from the actual source instead of listing generic texture adjectives. Select at least four present materials when available; choose fewer only when the source genuinely contains fewer important materials.

```yaml
material_paint_proof:
  - material: source-present owner
    construction: broad base plus unequal light/form turns
    stroke_direction: follows volume, gravity, wind, flow, or surface grain
    edge_behavior: focal fragments / broken support / lost context
    reflectance: matte / soft reflected colour / sparse crisp plane / atmospheric
    visible_proof: what must be legible at panel or detail scale
```

Useful translations, never a mandatory palette or material list:

- sky and cloud: broad layered scumbles and overlapping atmospheric sweeps turning around light, not smooth gradients plus pasted white blobs;
- grass, rice, or foliage: clustered directional wedges linked by wind and depth, with only a few sharp representatives, not leaf-by-leaf photo detail;
- skin: quiet opaque warm/cool planes with sparse sharp facial accents and reflected scene colour, not peach fill or beauty airbrush;
- hair: one dark painted mass with tapered overlapping ribbons and broken silhouette clumps, not evenly outlined strand inventory;
- cloth: angular planes and dry-brush folds radiating from tension, gravity, seams, and contact, not every wrinkle enclosed by ink;
- road, earth, concrete, or stone: weight-bearing planes with selective granular broken drags, not universal speckle;
- metal or glass: compact reflected planes and a few crisp seams that borrow surrounding colour, not a full glossy outline.

The map must include source ownership and visible proof. A generic sentence such as `different materials have different texture` is insufficient.

## Three-scale painterly proof

- **Thumbnail:** irregular interlocking masses, asymmetric silhouette breaks, and varied edge rhythm survive; the page is not organized by uniformly inked object borders.
- **Panel:** faceted internal turns, a structural stroke current, shared illumination, and physically bound adjacencies are visible without zooming into texture.
- **Detail:** at least three important source-present materials show different mark scale, direction, edge, and reflectance; important forms are not enclosed by one perfect vector-like perimeter.

If the page would still be called clean digital cel anime after the gutters are removed, it fails this adapter even when colour, anatomy, and layout are attractive.

## Face identity versus panel performance

When a face appears, preserve identity-bearing structure: face proportions, relative feature spacing, hair mass, recurring character cues, and age impression when evident. Head axis, eye-line, gaze direction, expression, mouth state, and head turn are storyboard-controlled performance variables and may change between panels to express the beat. Distinguish intentional performance change from accidental identity drift. A close panel may clarify eyelids, hair locks, wetness, or light, but cannot redraw the person as a different character.

## Cross-panel continuity packet

Freeze these fields before the first generation and reuse them in every panel:

```yaml
style_name: Painterly Comic Animation
medium_identity: visibly hand-painted animation comic; not clean digital cel anime
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
line_role: sparse broken contour fragments, subordinate to painted masses; lost-and-found edges
material_paint_proof: source-specific, visible at panel/detail scale
three_scale_proof: irregular masses at thumbnail / connected planes and light at panel / divergent material marks at detail
face_identity_guard: face proportions / relative feature spacing / hair mass / recurring cues
panel_performance_variables: head axis / eye-line / gaze / expression / pose / hand state
panel_finish: same painted completion family across all panels
```

Panel differences may come from shot scale, camera position/height, action, foreground, focal owner, motif state, panel geometry, or narrative meaning—not from changing the medium. Camera relocation is optional when it helps; shot-scale and information-role differences are not. A detail panel can use denser marks and sharper edges while keeping the same colour, plane, brush, and material family.

## Anti-filter and anti-sticker checks

Reject or target-correct the page when any of these are visible:

- the original photo is still recognizable as a filtered underpainting;
- large colour regions are flat pasted blocks with no plane turns, shared light, or boundary binding;
- the whole page resolves as clean digital cel anime with uniform smooth outlines, hard two-band shading, vector-clean surfaces, or commercial-anime polish;
- a global brush/noise/film texture is applied equally to sky, face, cloth, stone, and water;
- every edge is equally sharp, equally soft, or uniformly blurred;
- the face is line-clean but the background is photographic, or one panel is sketchy while another is fully painted;
- painterly surface language has erased the comic page's shot hierarchy, gutters, motif reveal, or camera invention;
- the result is one painterly hero image, a borderless single frame, or fewer than three visible panels;
- every panel preserves the source camera, composition, pose, gaze, and environment distribution as if the photo were an Edit Target;
- a selected prop changes material, hardware, count, attachment, or semantic identity between panels.

## Prompt seed

When compiling the image prompt, use one compact clause such as:

> HAND-PAINTED ANIMATION COMIC PAGE, not clean digital cel anime. Create one portrait 2:3 page with at least three visible panels. Build every panel from area-adaptive interlocking opaque paint masses, three broad value groups with unequal internal turns, reconstructed faceted shapes, connected directional brush fields, shared boundary illumination, source-specific material marks, and sparse lost-and-found contour fragments; no uniform complete outline, smooth two-band cel surface, vector-clean polish, photo underpainting, pasted blocks, or global texture. Treat Image 1 as semantic scene/story evidence, never as an Edit Target: do not inherit its ratio, composition, subject placement, pose, gaze, horizon, or camera as locks. Let each beat choose its own shot scale and, when useful, an earned level, low, high/overhead, side, reverse, over-shoulder, or object-level camera. Keep focal fragments sharp, support edges broken, contextual edges atmospheric, identity-faithful painted-animation facial proportions, and one consistent completion family across the page.
