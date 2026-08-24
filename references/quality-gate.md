# Dual Quality Gate

Inspect the actual photo and actual result. A prompt cannot pass a visual gate.

The result must pass both:

1. **Source continuity:** the people, objects, relationships, and place remain recognizably derived from the supplied photograph.
2. **Sequence authorship:** the page has a coherent theme, real narrative progression, distinct panel roles, readable pacing, and a deliberate comic visual grammar.

A beautiful comic with unrelated people or place fails. A faithful photo duplicated into several framed crops also fails.

## Critical Source Failures

Fail immediately when applicable:

- wrong, merged, duplicated, or accidentally missing person/animal/object;
- face, hair, clothing, accessory, pet marking, product silhouette, or relationship drifts materially across panels;
- important left-right order, touch, gaze, ownership, support/contact, landmark order, or place topology changes without narrative authorization;
- a selected salient prop or motif changes visible count logic, recognition silhouette, proportions, component stack, material/pattern, ownership/contact, attachment/insertion, or semantic category across panels without an authorized state change;
- an ambiguous source form is rendered as unrelated object classes in different panels, or unseen components are invented as factual detail;
- a reconstructed viewpoint invents precise hidden architecture, geography, text, object backs, or body detail that the source does not support;
- hidden source detail is invented and treated as fact;
- a location, date, identity, dialogue, sign, or event is fabricated as observed truth;
- the output resembles a researched franchise character, costume, logo, prop, world, or copied page structure more than the source.

## Critical Sequence Failures

Fail immediately when applicable:

- fewer than three panels, or panel boundaries are unreadable;
- panels are repeated crops/zooms of the same pose with no information delta;
- no specific theme, state change, revelation, or meaningful visual contrast can be stated;
- most adjacent panels differ only through effects, color cast, or panel border;
- panel count is padded and can be reduced without losing information;
- characters and setting change style from panel to panel;
- without an explicit alternate-medium request, the page is lineart-dominant, only lightly tinted, semi-photoreal, or inconsistently finished instead of a complete opaque-color cel comic;
- the character and background use incompatible finish systems, or one panel is sketch/pencil/wash while another is fully colored;
- the page is a screenshot/contact sheet of the source, or a wide/medium/close crop ladder with no authored concept;
- every panel stays on the source-camera side and could be produced by cropping or zooming the original photograph;
- a three-to-four-panel page has no reconstructed viewpoint, or a five-plus-panel page has fewer than two, unless camera fidelity was explicitly requested;
- the opening and ending repeat the same camera side, subject scale, focal owner, action state, depth pattern, and scene information without a changed motif meaning;
- the result is still photographic or only color-graded, with no visible ink, shape, value-group, material, or page-grammar transformation;
- tiny panels, tangled reading order, or decoration make the page unreadable;
- the default output is not exact portrait `2:3`, is needlessly extra-tall, or reads as a `9:16`/scroll screenshot without an explicit user request;
- a four-plus-panel page is a single vertical column, or every panel is a full-width horizontal band stacked from top to bottom;
- a selected primary motif stays an under-resolved background mark in every panel, or its supposed close-up adds no construction, contact, material, scale, optical, state, or meaning information;
- secondary motifs compete at equal emphasis or become a catalog of decorative details with no distinct page roles;
- the result is a comic filter, generic anime wallpaper, sticker sheet, or storyboard thumbnails rather than a finished comic page;
- default output contains gibberish text, fake logos, watermarks, or signatures.

## Thumbnail Gate — 128–256 px

Every applicable item must pass:

- the page reads as one composition with a clear entry, path, and exit;
- the outer page silhouette is a compact portrait `2:3` rectangle unless the user explicitly overrode it;
- the panel topology reads as a two-dimensional page with visible lateral eye movement, not a long vertical strip;
- at least three panels have clearly different macro silhouettes, value patterns, or information roles;
- at least three shot scales are legible across the page and at least two camera heights/angles are visibly different;
- the focal owner changes across at least three panels when the source permits (for example place, person/gesture, object/detail, animal/reaction, or environmental trace);
- the most important beat owns enough area or contrast;
- gutters and panel boundaries remain legible;
- the character/environment model and palette feel continuous;
- the source-derived motif or relationship is recognizable without reading text;
- the primary motif, when selected, has a stable recognition silhouette and visible page-level emphasis; secondary motifs remain subordinate and legible;
- no panel looks like the same photo copied again.
- the page reads as a deliberate comic redraw at thumbnail size rather than a photograph with a filter.
- under the default house style, opaque colored silhouettes and grouped values organize the page before thin line detail; it does not read as paper, pencil, or ink with color washed behind it.
- the opening and ending have unmistakably different macro compositions and narrative jobs; if they share a scale, at least four visible axes differ.

## Panel-Scale Gate

- Each panel has one clear focal owner and one narrative delta.
- Adjacent panels differ on at least three visible axes, unless deliberate repetition is the concept.
- The page contains at least three distinct shot scales, two camera heights/angles, and three focal owners when the source permits; otherwise document the source limitation and use the strongest available substitutes.
- No two panels reuse the same source composition; border, tint, crop, or zoom alone does not count as differentiation.
- Reconstructed viewpoints preserve support, adjacency, landmark order, and depth logic while leaving uncertain zones simple or occluded.
- The reconstructed-viewpoint quota is met and the page is not locked to the source-camera side.
- Under Adjacent Moment, at least one source-supported action or prop state changes when the source and panel count allow it.
- Actions connect plausibly; hands, limbs, props, gaze, and support/contact remain coherent.
- Intentional off-panel subjects leave a readable clue or are documented by the beat structure.
- Panel geometry and gutter size correspond to narrative weight and time shift.
- Four-plus-panel pages use at least two columns or an equivalent inset/masonry topology; five-plus-panel pages have at least two lateral reading moves.
- Five-plus-panel pages use no more than two full-width panels and, when content permits, include vertical, horizontal, and square-ish or irregular panel shapes.
- Background detail supports place continuity without competing equally in every panel.

## Prop and Motif Gate

- The source inventory selected one primary motif and no more than two secondaries only when they materially support theme, action, spatial tension, or continuity.
- The primary motif is recognizable in at least two panels when source and panel count permit, and at least one appearance is object-led or relationship-led rather than incidental background.
- The magnified/reveal panel adds source-supported information about construction, material, contact, support/insertion, reflection/shadow, motion state, or scale. Crop alone does not pass.
- Distant, medium, and close appearances share one recognition silhouette, major proportions, visible component stack, count logic, material/pattern, contact/attachment, and semantic lock.
- Detail follows a hierarchy: distant view preserves recognition; medium view clarifies construction; close view reveals coherent material or contact. A close view cannot be less resolved or differently designed.
- Ambiguous objects use one stable fact-neutral visual reading unless the user identifies them. Unseen blades, backs, interiors, labels, mechanisms, or attachments remain occluded or simple.
- Secondary motifs each perform a different function such as contact witness, scale/direction anchor, or optical echo; remove any motif that only adds clutter.
- Material response is specific and consistent: wet metal, fabric, glass, leather, painted plastic, water reflection, or worn stone should not collapse into the same generic glossy texture.

## Finished-Color Style Gate

Apply this gate unless the user explicitly requested another medium. Every item must pass:

- **Color coverage:** every pictorial panel is completely and intentionally colored. Light gutters and source-motivated white cloud, snow, mist, water glints, or highlights are valid; unfinished paper-white subject or environment regions are not.
- **Contour hierarchy:** medium dark contours define silhouettes, overlaps, expressions, folds, and prop construction; thinner interior marks remain subordinate. The page is not carried by a web of equal fine lines.
- **Cel volume:** people, skin, hair, clothing, key props, and focal foreground use two to four coherent hard or clean-edged value groups. Continuous photo gradients, airbrushed skin, pores, and glossy beauty rendering do not dominate.
- **Color-mass priority:** at 128–256 px, major hue and value shapes establish entry, hierarchy, and depth before line texture becomes readable.
- **Character/environment match:** background and character share one completion family. Backgrounds are fully colored and simplified, not photographic/painterly plates or unfinished sketches behind cel characters.
- **Material locality:** water, grass, bark, stone, metal, fabric, and cloud use different selective texture behavior. Global pencil grain, global hatch, or one texture overlay cannot substitute for material authorship.
- **Soft-edge budget:** gradients and lost edges are concentrated in atmosphere, reflection, glow, spray, or distant depth; foreground bodies, clothing, props, and plants remain designed through clear shapes.
- **Cross-panel lock:** contour weight, fill opacity, cel-step count, face/skin/hair model, saturation logic, background completion, texture family, border weight, and gutter color remain stable throughout the page.

If the user explicitly requested monochrome, pencil, watercolor, painterly, or line art, replace this gate with an equally explicit medium-specific Completion Lock; do not treat the house default as higher priority than the user.

## Detail Gate

- Faces, hair, clothes, markings, selected prop construction/material, and important landmarks are consistent.
- Line, opaque fill, cel value steps, texture, edge behavior, anatomy stylization, background finish, and border/gutter language form one Style Bible, Style Fingerprint, and Completion Lock.
- At least four concrete comic transformation operations are visible: designed contour, simplified shape/anatomy, grouped values, limited palette hierarchy, material print/brush system, authored perspective/silhouette, or page-level rhythm.
- If the source's photographic rendering remains dominant, fail this gate even when the palette is attractive.
- Texture is material-specific rather than a global overlay.
- Color comes from declared source roles or a motivated re-script; focal accents do not wander randomly.
- Effects, speed lines, glow, particles, halftone, or broken borders are selective and narratively motivated.
- Any required text is exact, legible, correctly ordered, and safely placed.

## Scored Review

Score `0 = fail`, `1 = acceptable`, `2 = strong`.

1. Source identity, count, and relationship continuity
2. Appearance, Prop/Motif Bible, material, and reconstructed scene-world continuity
3. Theme specificity, visual concept, and state change
4. Panel-role necessity, camera/action/prop invention, motif arc, and adaptive count
5. Adjacent-panel visual differentiation and focal-owner changes
6. Compact `2:3` page geometry, lateral reading flow, hierarchy, and gutter pacing
7. Cross-panel Style Bible, Style Fingerprint, and Completion Lock consistency
8. Line/opaque-fill/cel-value/color/shape/texture authorship and non-photographic transformation
9. Comic-page finish and thumbnail readability
10. Originality and absence of reference/franchise residue

Pass only when there is no critical failure, items 1–7 have no zero, and the total is at least 16/20. Report Source continuity and Sequence authorship separately.

## One Targeted Correction

Change only the failed module and preserve successful decisions.

| Failure | Targeted correction |
|---|---|
| Identity or clothing drift | Restate the concise character model and protected appearance in every panel; remove optional costume detail |
| Extra/missing subjects or objects | Restore the exact source count and mark any intentional off-panel omission explicitly |
| Prop construction or material drift | Freeze one recognition silhouette, component stack, count logic, material/pattern, contact/attachment, and semantic lock; correct only the inconsistent appearances |
| Under-resolved primary motif | Reassign one panel as a prop/relationship-led reveal and increase coherent structure, contact, material, reflection, or scale information without changing the prop design |
| Ambiguous prop switches identity | Return to the observed form, choose one fact-neutral visual rendering, hide unknown components, and use that same semantic category across the page |
| Motif clutter | Keep one primary and only secondary motifs with distinct contact, landmark, or optical-echo jobs; return the rest to context |
| Place topology drift | Reinstate landmark order, support/horizon, depth bands, and recurring environment anchors |
| Repeated crops | Replace one redundant panel with a different beat, action state, angle, value shape, and narrative delta |
| Source-camera lock | Rebuild the Scene World Model and move one or two shots into source-supported low, high, side, reverse, over-shoulder, object-POV, or overhead corridors |
| Duplicate opening and ending | Keep the stronger bookend; rebuild the other with a different camera corridor, focal owner, action state, depth pattern, and motif meaning |
| Weak or generic theme | Rebuild the proposition from one visible relationship/pressure and remove unrelated drama |
| Padded panel count | Merge or delete beats without delta; resize the remaining panels by importance |
| Unreadable page flow | Simplify the grid, strengthen entry/exit, and make gutter sizes correspond to transitions |
| Vertical-strip layout | Restore the fixed portrait `2:3` canvas; rebuild the page as a two- or three-column mosaic, limit full-width panels, and create at least two lateral reading moves |
| Style drift | Reinstate one six-axis Style Bible and one character/environment model across all panels |
| Still photographic | Rebuild line, value groups, shape simplification, and material texture; remove filter underpainting |
| Lineart-dominant or lightly tinted finish | Restore complete opaque color masses, two to four cel value groups, medium structural contours, grouped hair/skin planes, and fully colored backgrounds; remove global pencil/hatch/wash dominance |
| Character/background finish mismatch | Keep the successful focal design, then redraw the incompatible environment or subject into the same cel-step, fill-opacity, edge, texture, border, and saturation system |
| Mixed completion across panels | Freeze one Style Fingerprint and Completion Lock, then correct only the panels whose contour weight, fill opacity, shading steps, gradient budget, or background finish drifted |
| Overdesigned effects | Remove nonessential glow, speed lines, textures, broken borders, and decorations; restore focal hierarchy |
| Gibberish text | Remove all lettering or restore only exact verified copy in reserved areas |
| Franchise residue | Remove names, motifs, costumes, props, logos, and page echoes; rederive design from the source and broad traits |

If the corrected result still fails, return the best inspected output with the exact limitation. Do not call it a pass.
