# Trend Research and Style Direction

Read when the user asks for current/popular/trending comic style, names a reference, or leaves style unspecified. The goal is informed originality, not imitation.

## Research Routes

### Current or unspecified style

Use live web research because popularity changes.

1. Check recent official platform rankings or curated lists, at least one recent award/shortlist, and one creator/process source. Favor publisher, platform, award, or creator-owned pages.
2. Sample enough works to avoid mistaking one title for a trend: ideally 6–12 works across at least two regions or formats such as print manga, digital/webcomic, and graphic novel.
3. Inspect only public thumbnails, covers, previews, or process material needed for abstract analysis. Do not download or package copyrighted pages.
4. Record the research date and extract no more than five transferable patterns: line/value tendency, color behavior, character-to-background contrast, pacing/layout, and material finish.
5. Select the direction that fits the current photograph and theme. Popularity is evidence, not an instruction to ignore source fit.

If browsing is unavailable, use the evergreen families below and state that the direction is trend-aware rather than freshly verified.

### Named work, franchise, or artist

- Identify the user's desired effect in ordinary visual language.
- Keep only broad traits such as energetic black shapes, quiet fine line, limited accent color, luminous digital rendering, elastic comedy, textured memoir, or vertical suspense pacing.
- Change the combination of line, palette, anatomy, texture, panel architecture, and setting treatment so the result has its own identity.
- Never include the artist/franchise name, exact character design, signature motif, costume, logo, prop, fictional location, or copied page skeleton in the generation prompt.

## Research Snapshot — 2026-08-24

This snapshot is orientation, not a permanent ranking. Refresh whenever the user says current/trending or when the snapshot is materially stale.

- [WEBTOON Popular](https://www.webtoons.com/en/ranking/popular) shows strong simultaneous demand for romance, fantasy, action, drama, comedy, thriller, and supernatural work rather than one dominant genre.
- [Manga Taishō 2026](https://www.mangataisho.com/) spans daily life, social observation, sports, fantasy, monsters, work, and ensemble drama among its finalists and selections.
- [2026 Eisner Awards](https://www.comic-con.org/awards/eisner-awards/) cover print and online work across children, teen, humor, memoir, reality-based, international, Asian, single-issue, and long-form categories.
- [WEBTOON Comics Tips](https://www.webtoons.com/en/canvas/comics-tips/layout-control-pacing-with-text-images/viewer?episode_no=25&title_no=892865) treats panel gaps, borders, foregrounds, text spacing, and eye flow as pacing tools.

Transferable conclusion: current appeal is plural. Strong work tends to have a decisive visual grammar, readable mobile/thumbnail silhouettes, controlled focal contrast, and pacing encoded in panel architecture. Do not claim a single universal “popular manga style.”

## Six Style Axes

Resolve all six before prompting.

1. **Line:** fine elastic nib / clean controlled contour / dry brush / heavy graphic ink / broken pencil.
2. **Value:** airy high-key / balanced three-value / deep black-white / colored cel groups / soft painterly grouping.
3. **Color:** monochrome / monochrome plus one source accent / limited 3–5 source-derived roles / full color with restrained hierarchy.
4. **Shape and anatomy:** observational / gently simplified / elastic comedy / heroic angular / lyrical elongated. Preserve identity even when stylizing.
5. **Texture:** clean digital / screentone / halftone / dry paper / colored pencil / brush grain. Use one primary material system.
6. **Layout rhythm:** print page / horizontal strip / vertical-scroll excerpt / irregular graphic-novel page / cinematic band sequence.

Name the result with descriptive traits, not a franchise label. Example: `quiet high-key monochrome observation with fine irregular nib, sparse screentone, one rust accent, and asymmetrical print-page pacing`.

## Style Priority and User Calibration

Use this order:

1. explicit user medium and style constraints;
2. a user-supplied preference image translated into abstract visual decisions;
3. the Painterly Comic Animation combined house default;
4. the Finished Luminous Cel Comic alternate when flat cel/opaque hard-edge rendering is explicit;
5. current trend research for compatible refinements such as pacing, contrast, or palette behavior;
6. another evergreen family only when the user requests it or the default is genuinely incompatible with the brief.

When a preference image is supplied, separate **content** from **style**. Do not carry over its person, prop, location, clothing, page skeleton, motif, or exact palette. Record only transferable decisions such as contour hierarchy, fill opacity, value-step count, color separation, facial simplification, background finish, material texture, border weight, and gutter language. Treat the preference image as analysis-only unless the user explicitly authorizes it as a generation input.

## Painterly Comic Animation — Combined House Default

Use this fingerprint when the user asks for a photo comic without selecting another medium. It keeps the earlier page and sequence contracts, then applies painterly-frame-inspired colour, plane, brush, material, and edge controls in an original comic-specific combination.

```yaml
style_fingerprint:
  line_role: selective medium-dark structural contours; thinner interior marks; never lineart-only
  fill_coverage: fully authored colour field; no unpainted photo underpainting or translucent-lineart finish
  macro_colour_masses: 5-9 interlocking large masses, recomposed per shot but related across panels
  value_system: three broad light/middle/dark groups with local painterly turns
  colour_structure: dominant field / structural counter / focal accent / neutral bridge; one primary contrast axis
  anatomy_and_face: simplified identity-faithful anime planes; preserve head axis, eye-line, gaze, expression, and feature spacing
  shape_and_plane: reconstructed graphic silhouettes and faceted planes with selective foreshortening
  brush_continuity: connected neighbouring brush fields and shared illumination at form boundaries
  material_finish: local mark grammar for hair, cloth, skin, grass, stone, metal, water, cloud, and other source materials
  edge_hierarchy: focal sharp; support controlled; context softer only for depth/atmosphere
  background_finish: fully painted and simplified to the same completion family as the character
  border_and_gutter: stable medium-dark frames and clean light gutters
```

### Painterly Completion Lock

```yaml
completion_lock:
  painterly_default_active: true unless explicitly overridden
  page_ratio: exact portrait 2:3; compact two-dimensional mosaic
  macro_colour_mass_count: 5-9
  value_group_count: 3
  exposure_key: selected once for the page
  connected_brush_fields: true
  shared_boundary_illumination: true
  faceted_plane_authorship: true
  material_local_marks: true
  focal_support_context_contrast: true
  line_is_structure_not_surface: true
  character_background_finish_match: true
  global_texture_overlay: false
  flat_cel_band_only: false
  photo_filter_or_underpainting: false
  face_geometry_guard: true
  panel_finish_drift: false
```

At thumbnail size, large colour/value shapes establish the page before brush detail. Internal colour turns and planes must describe volume; a global oil/noise texture, equal-detail treatment, uniform blur, or pasted subject cutout is a failure. Keep comic page rhythm, readable anatomy, and motif hierarchy visible beneath the paint.

## Finished Luminous Cel Comic — Alternate Flat-Cel Mode

Use this fingerprint only when the user explicitly asks for flat cel, opaque hard-edge fills, or the earlier finished-color direction:

```yaml
style_fingerprint:
  line_role: medium dark outer contours; thinner interior construction and expression marks; no hairline-only finish
  fill_coverage: complete opaque color in every pictorial panel; light gutters and intentional white phenomena are allowed
  value_system: two to four hard or clean-edged cel groups on people, clothing, props, and focal foreground
  color_structure: source-derived high-key environment, strong local separation, one controlled high-chroma focal accent when supported
  anatomy_and_face: gently simplified anime proportions; clean planes; readable eyes, mouth, hands, and silhouette; no photographic skin rendering
  background_finish: fully colored and deliberately simplified, with the same completion family as the subject
  material_finish: local and specific—water facets, grass clusters, bark cracks, stone wear, metal edges, fabric folds—never one global pencil texture
  soft_edge_budget: sky, cloud, mist, spray, water reflection, distant depth, or motivated glow only
  border_and_gutter: medium dark panel borders; clean warm-white or neutral-light gutters; stable across the page
```

The finish is **color-mass first, contour second, local texture third**. At thumbnail size, saturated and neutral color shapes should organize the page before thin marks become visible. A close-up may carry more construction and material detail, but it must not switch into a different rendering system.

### Completion Lock

Freeze these fields before panel prompting:

```yaml
completion_lock:
  colored_page_default: true unless explicitly overridden
  opaque_fill_coverage: complete across subject and environment
  cel_value_steps: 2-4, stable across panels
  line_dominance: structural, never the primary final surface
  character_background_finish_match: true
  skin_finish: simplified colored planes; no pores or airbrushed photo shading
  hair_finish: grouped locks and shadow masses; selective strands only
  gradient_budget: atmosphere and distant depth only
  texture_budget: material-local and focality-aware
  panel_finish_drift: false
```

### Lineart-Dominant Failure Signs

Reject the default result when any of these dominate without an explicit user request:

- pale or translucent color washes sitting behind a visible pencil/ink drawing;
- large pictorial areas that remain paper-white because color was never authored;
- dozens of equally weighted micro-lines defining hair, fabric, foliage, or stone instead of colored masses;
- continuous photographic gradients on faces, limbs, clothes, or props;
- skin pores, glossy photo highlights, shallow-depth-of-field realism, or airbrushed beauty rendering;
- richly rendered characters against unfinished sketch backgrounds, or fully painted backgrounds with line-only characters;
- one panel using cel blocks while another uses pencil, watercolor wash, or semi-photoreal rendering.

Do not confuse clean contour with lineart dominance. The house style uses visible ink, but color and grouped value carry volume, hierarchy, and finish.

## Alternate Style Families

These families are user-selected or brief-selected overrides, not the automatic default. Customize the axes from the source and write a new Completion Lock whenever one is chosen.

### Quiet Observational Manga

Best for daily life, travel, family, friendship, stillness, and subtle gestures. Fine imperfect line, restrained facial acting, high-key gray, sparse screentone, substantial quiet space, small environmental details, and patient beat-to-beat transitions.

### Monochrome Kinetic Ink

Best for action, sport, weather, machines, animals in motion, and architecture with strong diagonals. Decisive black masses, elastic brush lines, speed or impact marks used locally, aggressive scale changes, foreshortening, and clear action silhouettes.

### Luminous Digital Drama

Best for portrait, fashion, romance, nightlife, interiors, and emotional confrontation. Controlled clean line, source-derived color roles, luminous but motivated light, selective soft edges, expressive faces and hands, and elegant panel spacing. Avoid plastic skin and generic beauty retouching.

### Textured Graphic Memoir

Best for memory, family, history, place, landscape, and personal ritual. Dry brush or pencil, limited palette, visible paper or print texture, irregular but readable frames, object/detail echoes, and transitions that can move through time without spectacle.

### Bold Comic Pop

Best for pets, children, food, playful objects, comedy, and energetic social moments. Chunky contour, simplified shapes, high-chroma source accents, elastic expression, brisk timing, and one strong visual joke or reversal. Avoid sticker-sheet clutter.

### Atmospheric Suspense

Best for night, rain, urban space, waiting, isolation, or an ambiguous edge event. Controlled deep shadow, oblique framing, cropped foregrounds, one restrained accent color, longer pauses, and delayed information. Avoid generic horror symbols unless visible in the source.

## Style-to-Source Fit

Choose by evidence:

- gesture and motion favor kinetic ink or comic pop;
- small interpersonal cues favor quiet observation or luminous drama;
- history, memory, weathered material, or place evidence favor graphic memoir;
- night, occlusion, distance, or incomplete information favor suspense;
- a bright photo does not need to become dark, and a colorful photo does not require full color.

## Explicit Comic or Anime Request

When the user asks for 漫画、动漫、anime、manga, or a comic page, treat that as a request for a visual redraw, not merely a mood or color grade. Prefer a clearly authored combination of:

- visible ink/contour or pencil behavior;
- simplified, designed shapes and expressive but source-faithful anatomy;
- grouped cel-shaded or graphic values;
- a limited palette hierarchy and deliberate accent color;
- screentone, dry brush, paper, or another declared material system;
- panel composition with camera changes and readable gutters.

For the Painterly Comic Animation default, choose at least four operations including authored colour/value masses, faceted planes, connected brush fields, material-local marks, selective contours, and focal/context edge hierarchy; for the alternate flat-cel mode, choose grouped cel values and opaque hard-edge fills instead. State the operations in the Style Bible. Do not describe the result as “realistic comic,” “cinematic photo with comic colors,” or “anime filter” unless the user explicitly asks for a hybrid; even then, keep the comic operations visible at thumbnail size. A style direction that cannot be recognized without zooming into texture fails the comic-transformation gate.

## Originality Isolation Check

Before generation, confirm:

- the final style description contains no artist/franchise name;
- no current work supplied its character, costume, logo, prop, setting, signature effect, page silhouette, or exact palette;
- at least two major style axes differ from any single researched example;
- the page structure comes from this photo's beats, not a sampled page;
- only the user's photo will be attached to generation.
