# Quality gate

Inspect the actual output at full view and thumbnail scale. Check structure before mood.

## Layout selection

- Use the portrait gates for a `3:4` nine-cell result and compare against `assets/layout-guide.png`; use the portrait four-panel gates for `assets/layout-guide-vertical-4.png`.
- Use the landscape gates for a `4:3` six-cell result and compare against `assets/layout-guide-4x3.png`; use the landscape four-panel gates for `assets/layout-guide-horizontal-4.png`.
- An explicit ratio or cell count always wins. Without one, route a source image at width/height `>=1.15` to landscape; otherwise use portrait. Theme Compose remains portrait by default.

## Portrait hard gates

1. The default canvas is portrait `3:4` unless the user explicitly overrides it.
2. Map the output to the fixed `1200 x 1600` design coordinates. The outer grid must occupy `x=96..1104`, `y=96..1104`, exactly `1008 x 1008`, with exactly `24` units of gutter. Top, left, and right ivory paper margins must each measure exactly `96` units and look equal at thumbnail scale. No optical adjustment is permitted.
3. Verify the nine exact `320 x 320` cell frames at columns `x=96..416`, `440..760`, `784..1104` and rows `y=96..416`, `440..760`, `784..1104`. Confirm that they read as nine copies of one shared square tile rather than nine independently drawn frames. After proportional scaling and rounding, every outer-grid and cell width must equal its height within one output pixel. Any larger difference is a hard failure. No tall rectangles, wide rectangles, unequal rows, unequal columns, stretched edge cells, merged cells, missing cells, or extra panels.
4. Verify generous negative space: the grid occupies exactly `84%` of canvas width and `63%` of canvas height, with a visibly deeper lower paper field. Reject an oversized or near-full-bleed grid.
5. Compare the result directly with `assets/layout-guide.png` at the same canvas size. Outer-square placement, equal top/left/right margins, gutter rhythm, and all nine square envelopes must visually coincide. The final image must not retain the guide's neutral gray, clean placeholder bars, circles, or rigid digital edges.
6. A quiet pale ivory-cream lower editorial zone is present. Text and subject icons occupy only a narrow 7–9% high band with generous blank ivory and remain subordinate to the grid.
7. Footer left contains only the exact copy as exactly two small left-aligned lines by default. Capital height is approximately 1.2–1.5% of canvas height and visibly about 20% smaller than the earlier default.
8. Footer right contains only subject-derived ultra-minimal icons. One primary subject requires exactly one icon. Multiple subjects require one icon per subject, clamped to two through five. Every icon has a recognizable subject cue, one main silhouette, at most one negative cut, and at most one support mark. No filler geometry or duplicated icon is allowed.
9. Exactly two designed colors appear: pale ivory cream `#F7F1E3` and the declared ink. Footer text and subject icons obey the same palette. Reject noticeably darker, yellower, brown, gray, or aged-paper backgrounds.
10. Every cell has one broad mass, void, crop, field, or rhythm. The grid does not become a detailed object sheet or collapse into empty generic logos.
11. Four to six cells are abstract, material, motion, erosion, or negative-space studies; two to four are semi-literal cue studies; at least one is a cropped signature; no more than one is a simplified scene fragment.
12. Only two to four signature cues survive across the full grid. Reject complete camera or lamp assemblies, precise repeated railing arches, brick-by-brick paving, coherent line-art, and several contextual details inside every cell.
13. Crop, shallow overlap, scale change, contact, or one gentle directional cue may appear, but no cell rebuilds complete foreground/midground/background depth or photorealistic volume.
14. Pictorial cores are solid, flat, opaque, rounded, and mildly irregular. Absorbed transition stays within roughly `0.15–0.35%` of a cell edge and does not visibly cloud or enlarge shapes. Strong halation remains a separate outer bloom. Reject wet, fuzzy, watercolor-like, or heavily absorbed ink.
15. All cells are materially distinct and grounded in the source, theme, or added-subject plan.
16. In Source + Added Subject mode, the addition appears in two to four cells, includes at least one relationship with a source anchor, and does not crowd the full grid.
17. Fine paper fibers, shallow tooth, and subtle pulp mottling remain continuous through pale ivory and ink across both grid and footer without eroding flat cores.
18. Strong boundary bloom is immediately visible at thumbnail scale, while the global diffusion veil remains low-to-medium and does not merge gutters, blur icons, wash out ink, erase retained detail, or destroy footer legibility.
19. The square scaffold remains exact while the print edge stays organic. Allow only a faint `2–5` unit inward dry-brush fringe and rare pinholes. Reject a rigid digital outline, but also reject any fringe that protrudes into gutters, bends the grid, shifts corners, or changes the measured square envelope.
20. No source pixels, copied source text, logo, watermark, third color, painterly rendering, glossy shading, or 3D appears.

## Landscape hard gates

1. Canvas is landscape `4:3`, mapped to exactly `1600 x 1200` normalized units.
2. Outer grid occupies `x=188..1412`, `y=188..996`. Top, left, and right ivory margins each measure exactly `188` units. Reject the earlier oversized `128`-margin placement or any grid wider than `1224` units.
3. Verify six exact `392 x 392` cells at columns `x=188..580`, `604..996`, `1020..1412` and rows `y=188..580`, `604..996`, with exactly `24` units of gutter. Every cell width equals height within one output pixel. Reject tall or wide panels, unequal rows or columns, merged cells, missing cells, or extra panels.
4. Verify the six cells read as copies of one shared square tile in a `3 x 2` array. The `1224 x 808` outer scaffold may be rectangular; the individual cells may not.
5. Compare directly with `assets/layout-guide-4x3.png`. Placement, margins, gutter rhythm, and all six square envelopes must coincide without retaining neutral gray or placeholder marks.
6. Footer remains below `y=996`; copy and icons stay roughly within `y=1054..1110`, with a clear blank band above and at least `90` units of ivory below. Text is exactly two tiny left-aligned lines with capital height `1.05–1.25%` of canvas height. Icons are only `30–42` units high, obey the subject inventory and one-to-five rule, and end no farther right than `x=1412`.
7. Apply portrait hard gates 9–20 unchanged, replacing nine-cell counts with the six-cell balance: four to five abstract/material-led studies, only one to two semi-literal cue studies, at least one cropped signature, no more than one simplified scene, and only two or three signature cues across the full grid.
8. Every cell passes the silhouette-first test: one dominant filled mass or cream void, roughly two to seven large countable forms, and at most one supporting rhythm family. Reject any cell that reads as colored pencil, sketch, engraving, line art, hatching, stippled shading, repeated fur/feather strokes, leaf veins, small construction lines, or detailed food surface. Paper grain may interrupt flat fills microscopically but may not describe form.

## Four-panel hard gates

1. A portrait four-panel result uses `3:4` and the fixed `1200 x 1600` coordinates: four exact `492 x 492` squares at columns `x=96..588`, `612..1104` and rows `y=96..588`, `612..1104`, with `24`-unit gutters and equal `96`-unit top/left/right margins. Compare against `assets/layout-guide-vertical-4.png`.
2. A landscape four-panel result uses `4:3` and the fixed `1600 x 1200` coordinates: four exact `288 x 288` squares at `x=188..476`, `500..788`, `812..1100`, `1124..1412`, all at `y=188..476`, with `24`-unit gutters and equal `188`-unit top/left/right margins. Compare against `assets/layout-guide-horizontal-4.png`.
3. In either branch, the panels read as one shared square tile copied four times. Every panel width equals height within one output pixel; reject any tall, wide, merged, missing, stretched, or independently improvised panel.
4. Use at least three abstract/material-led studies and at most one semi-literal cue, with one cropped signature and no more than one simplified scene fragment. Apply the shared footer, palette, edge, paper, glow, grain, and icon gates below.

Any hard-gate failure requires one regeneration. Put the failed rule in the first two prompt sentences and revise the weakest cells. Do not present a second failed result as fully successful.

## Abstraction balance audit

- Describe each cell in one focused phrase naming its broad field, void, crop, or rhythm. If the phrase reads like an equipment inventory or full scene description, simplify. If the full cell set could describe any unrelated theme, restore one grounded cue in only the weakest cell.
- Preserve selected structures sparingly: a reduced railing-post rhythm, two paving cuts, one camera bar and hanging drop, wheel arc, profile edge, or wave cut. Reject literal arch-by-arch, brick-by-brick, bolt-by-bolt, hair-by-hair, or leaf-by-leaf reconstruction.
- Reject full foreground/midground/background staging and dominant vanishing-point perspective. Accept a single softened directional cue that helps recognition.
- If the source image could be approximately reconstructed from the grid, abstraction is insufficient. If the source cannot be recognized at all without the captions, abstraction is excessive.

## Edge audit

- Grid borders remain mathematically fixed; pictorial cores inside cells feel flat, hand-cut, rounded, and softly luminous.
- Look for eased corners, mild contour wobble, and only a very narrow printed transition. Reject visible ink clouds, broad fuzzy absorption, watercolor bleed, excessive fiber breakup, perfectly smooth Bézier icons, repeated identical modules, sharp triangular clipping, and hard digital joins.
- Retained details and footer icons must have readable opaque cores under the glow. Reject both brittle sharpness and shapeless blur.

## Footer audit

- The footer is a quiet editorial accent, not a second poster.
- The English copy is readable, matches the planned string, and follows the planned two-line break. Regenerate once if it becomes one line, invents characters, or distorts badly.
- The type feels monospaced, serifed, unevenly inked, and very small without becoming illegible.
- Right-side icons match the counted subjects. A single subject has exactly one icon; multiple subjects have two to five icons, one per subject. Reject arbitrary dots, squares, bars, rings, arcs, brackets, filler marks, repeated icons, and miniature footer scenes.
- No other text appears anywhere.

## Finish audit

- Strong halation creates a visible luminous band while each shape retains a readable core.
- Global diffusion is obvious but not opaque fog.
- Paper reads as very light ivory cellulose with subtle cloudy pulp variation, not deep beige, yellow parchment, fabric, canvas, watercolor pits, dirt, or uniform noise.
- Ink cores remain solid and flat with only mild absorption and rare pinhole paper show-through.
- Film grain is finer and more random than paper fibers and stays optically inside the two-color family.

## Prompt-only audit

Verify that the prompt states the request mode, semantic anchors, selected layout, its complete fixed coordinate contract and cell bounds, the shared-square-tile construction metaphor, equal top/left/right margins, one-pixel geometry tolerance, exactly four, six, or nine equal square cells, the matching layout guide, a faint inward-only printed fringe, generous negative space, quiet lower footer, exact two-line footer copy and line break, smaller type scale, explicit subject inventory and icon count, icon identities and reductions, layout-appropriate abstraction ratio, stable flat cores, restrained `0.15–0.35%` ink transition, separate strong halo, pale ivory `#F7F1E3`, selected ink value, continuous subtle paper texture, separate grain, and the negative block.

