# Visual system

## Portrait 3:4 nine-square layout

- Canvas: portrait `3:4` by default. Obey another ratio only when the user explicitly requests it.
- Use a fixed normalized design canvas of exactly `1200 x 1600` units for the default portrait `3:4` output. Scale all coordinates proportionally to the final raster; do not recompute them from generated content.
- Establish one paper-margin unit `M=96`. Place the outer grid at `x=M..1200-M`, `y=M..M+1008`, therefore `x=96..1104`, `y=96..1104`. Its width and height are both exactly `1008` units. Top, left, and right paper margins are visibly identical at exactly `96` units. Do not center the grid vertically.
- In relative terms, make each top/left/right margin `8%` of canvas width. Make the square grid `84%` of canvas width and `63%` of canvas height. Use these proportions as a visual cross-check, not as an alternative layout.
- Use gutters of exactly `24` units. Make every cell exactly `320 x 320` units at these bounds: columns `x=96..416`, `440..760`, `784..1104`; rows `y=96..416`, `440..760`, `784..1104`.
- Think in nested squares before adding content: first one `1008 x 1008` outer square; then a repeated 3-by-3 array made from one shared `320 x 320` square tile frame copied nine times. Do not describe or generate nine independent rectangles. The same tile edge length controls every row and column.
- Treat these bounds as immutable layout geometry. Generate or clip pictorial content inside them. Never resize a cell independently, fit the grid by height, distribute leftover space, stretch edge cells, round one axis differently, or let glow redefine the measured frame.
- When scaling to output pixels, use the same scale factor on both axes. After rounding, outer-grid width must equal height and every cell width must equal height within one output pixel. Any larger difference is a hard failure, not an acceptable optical adjustment.
- Keep the exact square scaffold visually legible through equal ivory gutters. Preserve the desired hand-printed edge by allowing only a faint irregular pigment fringe inside each square boundary: `2–5` design units inward from the locked frame, with occasional pinhole gaps. The fringe may wobble locally but may not move a frame edge, invade a gutter, or change the measured square silhouette. Never draw a separate hard outline around the cells.
- Footer: use the larger remaining pale ivory-cream area below the grid as quiet paper. Keep actual text and icons within a narrow 7–9% high band, with generous blank ivory above and below. The footer must feel subordinate, not like a second poster. The entire poster should read as a small square print block floating in a broad paper field.
- Footer left: reserve roughly 58–68% of footer width for exactly two short, small, left-aligned English lines.
- Footer right: reserve roughly 14–26% for one to five subject-derived ultra-minimal icons. Leave clear blank space between copy and icons and around the footer.

## Landscape 4:3 six-square layout

- Use a fixed normalized canvas of exactly `1600 x 1200` units. Use this branch for an explicit landscape `4:3` or six-grid request, or for a source image whose width is at least `1.15` times its height when no ratio is stated.
- Establish one enlarged paper-margin unit `M=188`. Place the outer six-cell grid at `x=188..1412`, `y=188..996`. Top, left, and right paper margins are visibly identical at exactly `188` units. Do not center the grid vertically. The compact grid must float inside a conspicuously larger paper field.
- Use gutters of exactly `24` units. Make every cell exactly `392 x 392` units at columns `x=188..580`, `604..996`, `1020..1412`; rows `y=188..580`, `604..996`.
- Think in one locked `1224 x 808` outer scaffold populated by a repeated 3-by-2 array made from one shared `392 x 392` square tile frame copied six times. The outer scaffold is rectangular because it contains three square columns and two square rows; each tile itself remains a mathematically exact square.
- Treat these bounds as immutable. Never fit the cells by available height, enlarge one row, stretch edge cells, or improvise six independent panels. Scale both axes with one identical factor; after rounding, every cell width must equal its height within one output pixel.
- Keep equal ivory gutters visibly open. Permit only a faint irregular pigment fringe `2–5` units inward from each locked square boundary. It may not enter a gutter, move a corner, or alter the measured square envelope.
- Use `assets/layout-guide-4x3.png` as geometry-only reference. Never use its neutral gray, placeholder footer bars, circles, or clean digital edges as finished content.
- Footer: use the remaining pale ivory band below `y=996`. Keep copy and icons within approximately `y=1054..1110`, leaving a clear blank band above and at least `90` units of ivory below. The footer must be smaller and quieter than the prior landscape version.
- Footer left: place exactly two tiny left-aligned English lines near `x=188`; reserve roughly 58–68% of the usable width. Target a capital height of only `1.05–1.25%` of canvas height.
- Footer right: place the subject-derived ultra-minimal icons within the rightmost 14–24% of usable width, ending no farther right than `x=1412`. Keep icons approximately `30–42` units high, in one quiet row where possible, with generous clear space around them.

## Medium-flat abstraction

- Let the full six- or nine-cell family carry recognition collectively. A single abstract cell may be ambiguous when the neighboring cells restore the theme.
- Treat each cell as one broad filled mass, negative-space gesture, crop, material field, or mark rhythm plus at most one to three supporting mark families. Aim for roughly three to nine large forms; count a dot, dash, ripple, post, or fragment rhythm as one family.
- In portrait, include four to six abstract, material, motion, or negative-space studies and two to four semi-literal cue studies. In landscape, include four to five abstract/material-led studies and only one to two semi-literal cue studies. In either layout, include no more than one simplified scene fragment; crop or reduce structural cues rather than rendering detailed objects.
- For landscape, impose a stricter graphic budget matching the portrait references: each cell contains one dominant silhouette or negative-space system, roughly two to seven large countable forms, and at most one supporting rhythm family. At thumbnail size, forms must read as solid blocks rather than drawing. If a form requires internal strokes to be recognizable, enlarge, crop, or reduce it again.

## Portrait 3:4 vertical four-panel layout

- Use this branch for an explicit portrait `3:4` vertical four-panel request. It is a quieter 2-by-2 square block on the same portrait canvas, not four stretched cards.
- Use the fixed `1200 x 1600` canvas and the same `M=96` outer paper margin. Place four exact `492 x 492` cells at `x=96..588` and `612..1104`, with rows `y=96..588` and `612..1104`; the gutter is exactly `24` units.
- Treat the block as one shared square tile copied four times. Keep top, left, and right paper margins exactly equal at `96` units. After proportional scaling, every cell width must equal its height within one output pixel.
- Use `assets/layout-guide-vertical-4.png` as geometry-only reference. Keep the footer quiet and subordinate, with the same two-line typewriter copy and one-to-five subject-icon rule.

## Landscape 4:3 horizontal four-panel layout

- Use this branch for an explicit landscape `4:3` horizontal four-panel request. Place four exact squares in one row.
- Use the fixed `1600 x 1200` canvas with `M=188`. Place `288 x 288` cells at `x=188..476`, `500..788`, `812..1100`, and `1124..1412`, all at `y=188..476`; gutters are exactly `24` units.
- Treat the row as one shared square tile copied four times. Keep top, left, and right paper margins exactly equal at `188` units. After proportional scaling, every cell width must equal its height within one output pixel.
- Use `assets/layout-guide-horizontal-4.png` as geometry-only reference. Leave the lower paper field open for the same small two-line footer and subject-derived icons.
- Preserve only two to four signature details across the entire grid: for example, a road bend, lane-dash rhythm, lamp disk, railing cadence, wheel arc, profile edge, foam cuts, or leaf cluster. Do not place several signature parts in every cell.
- Translate structures rather than illustrate them: railing -> a few unequal blocks and voids; brick paving -> two or three broken plane cuts; camera crossbar -> one bar, joint, and hanging drop; road -> one broad curve and sparse dash rhythm; cloud -> one torn field; sea -> broken reflection bands.
- Prefer irregular fields, pooled shapes, broad arcs, radial cuts, torn edges, floating islands, dotted trails, broken stripes, negative-space channels, and quiet density shifts. Avoid coherent line-art, precise architectural openings, detailed hardware, and literal perspective scenes.
- Treat linework as a failure mode. Do not model volume with hatching, contour strokes, engraving, pencil texture, repeated fur or feather marks, leaf veins, small windows, tiny food texture, or descriptive surface scratches. Paper texture and grain may break a flat fill microscopically, but must never become drawn detail.
- Permit crop, overlap, scale change, and one gentle directional tendency. Do not reconstruct full foreground/midground/background depth.

## Soft-edge print language

- Keep outer canvas, invisible square scaffold, square cells, and gutters geometrically exact. Keep pictorial shapes flat and stable inside cells. Separate structural geometry from surface character: the scaffold is exact; only the inward pigment fringe is hand-printed.
- Build the core graphic from solid fills with rounded terminals, eased corners, mild hand-cut wobble, and slight asymmetry. The core silhouette must remain opaque, countable, and visually clean.
- Limit absorbed ink spread to a narrow transition band of roughly `0.15–0.35%` of a cell edge. Use only faint paper-fiber breakup and rare pinhole show-through. Do not let absorption visibly enlarge, dissolve, or cloud the form.
- Add strong luminous halation as a separate optical layer outside the stable core. Glow must not be simulated by increasing ink bleed or smearing paper texture.
- Keep exact circles, rectangles, straight lines, and sharp Bézier corners rare inside pictorial cells unless a signature object requires them. Even then, soften them with ink gain and imperfect registration.
- Reject razor-cut clipping masks, CAD-clean architecture, brittle polygons, hard black outlines, repeated stock icons, and perfectly identical repeated marks.

## Color and footer typography

- Use exactly two designed colors: fixed pale ivory cream `#F7F1E3` and one user-chosen solid ink color.
- Fill every upper cell with the chosen ink; use pale ivory cream for shapes, negative cuts, margin, and gutters. Invert a cell only when it improves variation and still preserves the two-color system.
- Keep the footer pale ivory cream. Set the English copy and subject icons in the chosen ink.
- Render footer copy as exactly two left-aligned lines in a vintage typewriter-style monospaced serif. In portrait, target a capital height around 1.2–1.5% of canvas height; in landscape, use the smaller 1.05–1.25% range defined above. Use line spacing around 1.35–1.55 times the capital height, uneven ink pressure, slight character wear, and imperfect baseline registration while staying readable. Do not add headings, labels, numbers, logos, or other text.
- Count primary subjects with `references/request-modes.md`. Use exactly one icon for a single subject. For multiple subjects, use one icon per subject with a minimum of two and maximum of five.
- Build each icon as one main solid silhouette, at most one cream negative-space cut, and at most one supporting ink mark. Preserve one distinctive cue such as a wheel, handle, beak, leaf, roofline, profile, faucet bend, burner ring, or camera drop. Keep icons flatter and simpler than the grid studies.
- Arrange icons in one quiet left-to-right row or a compact two-row group only when three to five icons need it. Keep icon boxes equal in size, aligned to a shared baseline or grid, and separated consistently. Do not add filler marks, repeat icons, or turn the icon group into a miniature scene.

## Paper and strong optical finishing

1. Build one continuous uncoated pale ivory-cream `#F7F1E3` paper sheet across grid and footer: fine cellulose fibers, shallow tooth, and very subtle broad pulp variation. Keep the paper visually light, not yellow-brown or aged parchment.
2. Keep chosen-color ink cores solid and flat. Add only mild absorption, rare pinhole-scale ivory show-through, and a very narrow feathered print edge.
3. Add strong warm halation as a separate soft-light bloom at every cream/ink boundary. Let the bloom extend roughly `2–3.5%` of a cell edge while the underlying core stays flat, opaque, and sharply readable.
4. Use only a low-to-medium global diffusion veil. The halo must be obvious at thumbnail scale, but the ink itself must not look wet, fuzzy, washed out, watercolor-like, or heavily absorbed.
5. Add fine natural monochrome film grain above the paper, with sparse medium clumps. Keep it finer and more random than the paper fibers.

Reject smooth digital surfaces, uniform noise, canvas weave, cloth fibers, deep watercolor pits, wet-ink clouds, fuzzy absorption, waxy Gaussian blur, opaque fog, fully blown halos, chromatic aberration, dark yellow paper, gray dirt, stains, scratches, or heavy damage.

## Anti-style

Reject photography, literal source collage, traced reconstruction, deep perspective, architectural drafting, photorealistic volume, watercolor, oil paint, airbrush shading, glossy gradients, 3D bevels, drop shadows, comic outlines, UI cards, dense poster typography, ornamental frames, cheap sharp-vector iconography, and interchangeable generic symbols.

