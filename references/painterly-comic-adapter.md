# Painterly Comic Animation Adapter

This adapter translates the abstract control methods of the public `painterly-frame` workflow into a self-contained rule set for source-grounded comic pages. It is an original adaptation for this Skill, not an external runtime dependency and not a request to imitate a particular artist, franchise, or existing frame.

## What this adapter controls

`photo-to-comic` still owns the page: the source photo becomes a scene-world, the beats determine the number of panels, the camera plan creates new views, the motif system assigns object-led details, and the page remains a compact portrait `2:3` mosaic. This adapter owns how each panel is painted and how the painted language stays coherent across panels.

Do not trade away panel storytelling for a painterly surface. A painterly page with five near-identical crops is still a failed comic sequence. Conversely, a varied sequence with unrelated brush treatments is a failed style lock.

## Composition Lock for a comic page

Freeze the outer page contract before rendering:

- exact portrait `2:3` canvas by default;
- at least three panels, with two-dimensional multi-column reading for four or more;
- dominant panel, supporting panels, gutters, and lateral reading moves are authored by the sequence engine;
- source camera is a reference anchor, not a crop template; reconstructed source-consistent viewpoints remain required;
- each panel keeps its own aspect family and shot role, while the page topology stays legible at thumbnail size.

Within each panel, preserve the source-supported subject count, landmark adjacency, support/contact surfaces, depth order, and recognizable silhouette. Restaging may change camera side, height, focal scale, foreground occlusion, and action state only when the Scene World Model and Action Affordance Map support it.

## Colour and value lock

Before line detail, author a colour map for the whole page and carry its roles through every panel:

1. Group the scene into roughly `5–9` interlocking large colour masses. They may be recomposed by shot, but they must remain related rather than pasted as independent blocks.
2. Organize the page into three broad value groups—light, middle, dark—then allow local turns inside those groups. Avoid continuous photographic shading and avoid a single dark wash over the whole page.
3. Assign spatial colour roles: `dominant field`, `structural counter`, `focal accent`, and `neutral bridge`; add one controlled collision only if the theme needs it. The focal accent should own the primary contrast axis, not every panel equally.
4. Lock the exposure key (high, balanced, or deep) and the main warm/cool relationship across the page. A new camera can change local area and emphasis, but not silently change the time of day or palette family.
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

## Face and identity packet

When a face appears, preserve the head axis, eye-line, gaze direction, expression, hair mass, and feature spacing from the source evidence. Simplify into designed anime planes, but do not let brush variation move the eyes, change the gaze, or redraw the person as a different character between panels. A close panel may clarify eyelids, hair locks, wetness, or light, but cannot invent a new identity.

## Cross-panel continuity packet

Freeze these fields before the first generation and reuse them in every panel:

```yaml
style_name: Painterly Comic Animation
page_ratio: portrait 2:3
macro_colour_masses: 5-9 interlocking masses
value_groups: 3 broad groups
exposure_key: high / balanced / deep, selected once
colour_roles: dominant field / structural counter / focal accent / neutral bridge
plane_language: reconstructed graphic shapes plus faceted planes
brush_continuity: connected neighbouring fields
illumination: shared light at form boundaries
material_grammar: local marks by material, not global texture
edge_hierarchy: focal sharp / support controlled / context softer
line_role: selective structural contour, subordinate to painted masses
face_geometry_guard: head axis / eye-line / gaze / expression / feature spacing
panel_finish: same painted completion family across all panels
```

Panel differences must come from shot scale, camera corridor, action, foreground, focal owner, motif state, panel geometry, or narrative meaning—not from changing the medium. A detail panel can use denser marks and sharper edges, but it keeps the same colour roles, light direction, plane logic, and contour family.

## Anti-filter and anti-sticker checks

Reject or target-correct the page when any of these are visible:

- the original photo is still recognizable as a filtered underpainting;
- large colour regions are flat pasted blocks with no plane turns, shared light, or boundary binding;
- a global brush/noise/film texture is applied equally to sky, face, cloth, stone, and water;
- every edge is equally sharp, equally soft, or uniformly blurred;
- the face is line-clean but the background is photographic, or one panel is sketchy while another is fully painted;
- painterly surface language has erased the comic page's shot hierarchy, gutters, motif reveal, or camera invention;
- a selected prop changes material, hardware, count, attachment, or semantic identity between panels.

## Prompt seed

When compiling the image prompt, use one compact clause such as:

> Painterly Comic Animation across the entire portrait 2:3 page: 5–9 interlocking colour masses, three broad value groups, scene-owned colour roles, reconstructed graphic shapes and faceted planes, connected neighbouring brush fields with shared illumination, material-specific marks, focal-sharp/support-controlled/context-soft edges, selective structural contours, identity-faithful anime face geometry, and one consistent completion level across every panel; no flat cel-band-only surface, pasted cutouts, global texture overlay, photo filter, uniform blur, or lineart-dominant finish.

