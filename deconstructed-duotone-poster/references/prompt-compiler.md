# Prompt compiler

Compile one concrete prompt in this order. Use visible nouns and verbs; do not rely on a style label.

## Paragraph 1: mode and semantic contract

- Source Transform: state that attached images are semantic references only. Name three to five retained anchors and only two to four signature cues to distribute across the complete grid. Explicitly discard original pixels, composition, lighting, assemblies, construction detail, and microdetail.
- Theme Compose: state that no source image exists. Name the text theme, derived anchors, and shared relation or mood.
- Source + Added Subject: name source anchors, the added subject, its input role, and which cells show it alone, in close detail, or interacting.

Require a completely new flat editorial print. Prohibit photography, tracing, full scene reconstruction, brands, watermarks, and copied source text.

## Paragraph 2A: portrait 3:4 nine-square grid and quiet footer

Label `assets/layout-guide.png` as a structural layout reference only. Require the final print to match its exact outer-square position, equal top/left/right margins, equal gutters, and repeated square-cell proportions. State that its neutral gray is non-semantic and must not appear in the result. Do not copy its clean digital edges, placeholder footer bars, or circles; redraw finished content with the selected duotone print language.

Put this geometry contract in the first two prompt sentences and repeat it near the end. Require a portrait `3:4` canvas using a fixed normalized design coordinate system of exactly `1200 x 1600` units. Define one visible paper-margin unit `M=96`; place the outer grid at `x=96..1104`, `y=96..1104`, making it exactly `1008 x 1008`. State plainly that the top, left, and right ivory margins are the same visible width: `96` units. Use gutters of exactly `24` units. Require nine cells of exactly `320 x 320` at columns `x=96..416`, `440..760`, `784..1104` and rows `y=96..416`, `440..760`, `784..1104`.

Before describing any imagery, require a two-stage visual construction: first establish one locked perfect-square outer scaffold; then repeat one identical perfect-square tile frame in three equal columns and three equal rows. Use the phrases `one shared square tile copied nine times`, `same side length on both axes`, and `three equal rows matching three equal columns`. Explicitly forbid composing nine freehand rectangles independently. Require a thumbnail check that compares the equal top/left/right paper bands and each cell's horizontal edge against its vertical edge.

State that these coordinates are immutable. Pictorial content may be clipped inside them but the frames may not move, stretch, optically compensate, redistribute space, or round the axes differently. When scaling to final pixels, use one identical scale factor for both axes; after rounding, outer-grid width must equal height and every cell width must equal height within one pixel. Any larger difference requires regeneration.

Preserve organic print character without weakening geometry. State that the exact frame is an invisible scaffold and only ink just inside each frame may form a faint `2–5` unit inward dry-brush fringe. The fringe may have slight hand-cut waviness and pinhole paper breaks but may never protrude into the ivory gutter, shift a corner, bow a grid line, or redefine the square envelope. Do not draw rigid digital outlines.

Place a quiet pale ivory-cream editorial zone beneath the smaller square grid. Keep its actual copy and icons within a narrow 7–9% high band and leave generous blank ivory around them. Require conspicuously more negative space than a full-bleed poster: the compact square print block floats on paper, with equal top/left/right margins and a substantially deeper lower paper field. State the exact footer copy and exact line break in quotation marks. Put it on the left as exactly two small left-aligned lines in chosen-color vintage typewriter-style monospaced serif text. Make the capital height approximately 1.2–1.5% of canvas height, about 20% smaller than the previous default, with 1.35–1.55 line spacing and uneven ink pressure.

Count and name the primary semantic subjects. On the right, require exactly one ultra-minimal icon for a single subject. For multiple subjects, require one icon per subject, clamped to two through five. State each icon identity and its single distinguishing cue. Build every icon from one solid silhouette, at most one pale-ivory negative-space cut, and at most one supporting ink mark. Prohibit arbitrary dots, squares, lines, rings, arcs, brackets, filler marks, duplicated icons, extra text, and miniature footer scenes.

## Paragraph 2B: landscape 4:3 six-square grid and quiet footer

Use this paragraph instead of Paragraph 2A for the landscape branch. Label `assets/layout-guide-4x3.png` as a structural layout reference only. Require a landscape `4:3` canvas using exactly `1600 x 1200` normalized units. Define the enlarged paper margin `M=188`; place the outer grid at `x=188..1412`, `y=188..996`. State that top, left, and right ivory margins are exactly equal at `188` units and are conspicuously larger than the prior landscape version.

Require one locked `1224 x 808` outer scaffold containing one shared exact-square tile copied six times in three columns and two rows. Use gutters of exactly `24` units. Require six cells of exactly `392 x 392` at columns `x=188..580`, `604..996`, `1020..1412` and rows `y=188..580`, `604..996`. Explicitly state that the outer scaffold is rectangular only because it contains a `3 x 2` array; every individual panel is a standard square with the same side length on both axes. Prohibit six independently improvised rectangles.

Keep coordinates immutable and use one identical scale factor on both axes. After rounding, every cell width must equal its height within one pixel. Preserve organic print character only through a faint `2–5` unit inward dry-brush fringe; never let it enter gutters or redefine a square.

Use the pale ivory footer area below `y=996`. Keep actual copy and icons within approximately `y=1054..1110`, with a clear blank band above and at least `90` units of ivory below. Put the exact copy near `x=188` as exactly two tiny left-aligned vintage typewriter-style lines with capital height `1.05–1.25%` of canvas height. Put only the planned subject-derived icon or icons on the right, no farther right than `x=1412`, using the same one-subject/one-icon and multiple-subject/two-to-five rules from Paragraph 2A. Keep icons only `30–42` units high. Do not copy the guide's neutral gray, placeholders, circles, or clean digital edges.

## Paragraph 2C: portrait 3:4 vertical four-panel layout

Use this paragraph when the user asks for a portrait `3:4` vertical four-panel poster. Label `assets/layout-guide-vertical-4.png` as a structural layout reference only. Require a fixed `1200 x 1600` canvas with `M=96`, a `2 x 2` block of four exact `492 x 492` squares at columns `x=96..588`, `612..1104` and rows `y=96..588`, `612..1104`, with `24`-unit gutters. State that the top, left, and right ivory margins are equal at `96` units and that the four cells are one shared square tile copied four times. Prohibit four freehand rectangles, stretched panels, coordinate drift, or optical square compensation. Keep the same quiet lower footer, two small left-aligned lines, and subject-derived icon rules from Paragraph 2A.

## Paragraph 2D: landscape 4:3 horizontal four-panel layout

Use this paragraph when the user asks for a landscape `4:3` horizontal four-panel poster. Label `assets/layout-guide-horizontal-4.png` as a structural layout reference only. Require a fixed `1600 x 1200` canvas with `M=188`, a single row of four exact `288 x 288` squares at `x=188..476`, `500..788`, `812..1100`, `1124..1412`, all at `y=188..476`, with `24`-unit gutters. State that the top, left, and right ivory margins are equal at `188` units and that the four cells are one shared square tile copied four times. Prohibit four freehand rectangles, stretched panels, coordinate drift, or optical square compensation. Keep the same quiet lower footer, two tiny left-aligned lines, and subject-derived icon rules from Paragraph 2B.

## Paragraph 3: medium-flat cells

Describe cells in reading order from the completed plan. For portrait nine-cell, describe cells 1–9; for portrait four-panel, describe cells 1–4; for landscape six-cell, describe cells 1–6; and for landscape four-panel, describe cells 1–4. Four-panel branches require at least three abstract/material-led studies and at most one semi-literal cue. In every branch, give each cell one broad filled mass, negative-space gesture, crop, material field, or mark rhythm; in landscape permit at most one support family and roughly two to seven large countable forms. Include at least one cropped signature and no more than one simplified scene fragment.

State that recognition belongs to the full cell family rather than every individual cell. Preserve only two to four signature cues in portrait or two to three in landscape. Permit crop, shallow overlap, scale change, contact, or one gentle directional cue. Remove full equipment assemblies, precise architectural openings, brick-by-brick paving, coherent line-art, foreground/midground/background staging, photorealistic volume, lighting, and microdetail.

For landscape, explicitly require the same graphic reduction as the portrait references: silhouettes and cream voids first, internal drawing removed, details merged into broad blocks. Ban colored-pencil texture, sketching, engraving, cross-hatching, contour hatching, stippled shading, repeated fur or feather strokes, leaf veins, small windows, fine food texture, and any linework used to model volume. If a cue needs those details, enlarge and crop it rather than drawing it.

## Paragraph 4: soft pictorial edges

Keep canvas, square cells, and gutters geometrically exact. Render each pictorial form with a stable opaque flat-fill core, eased corners, rounded terminals, mild hand-cut wobble, and slight asymmetry. Limit absorbed ink gain and paper-fiber breakup to a narrow `0.15–0.35%` transition band. Require strong halation as a separate outer light bloom rather than as blurred or spreading ink. Avoid wet ink, fuzzy absorption, watercolor edges, razor-sharp clipping masks, hard polygons, perfect stock-icon geometry, and CAD-clean intersections.

## Paragraph 5: two-color rendering

Name fixed pale ivory cream `#F7F1E3` plus the selected solid ink and hex value. Require exactly two designed colors. Fill upper cells primarily with the selected ink and form shapes with pale-ivory cuts; keep the footer pale ivory with selected-ink type and subject icons. Use broad stable flat masses and controlled internal rhythms. Prohibit darker beige, yellow-brown paper, black, pure white, gray, accent colors, outlines, graphic gradients, shading, bevels, shadows, and 3D.

## Paragraph 6: paper, strong glow, grain, and exclusions

Require one continuous light uncoated pale-ivory paper substrate through grid and footer, with fine cellulose fibers, shallow tooth, and very subtle broad pulp mottling. Require solid flat ink cores, mild absorption, rare pinhole paper show-through, and only a narrow feathered print edge.

Require strong warm boundary halation as a separate soft-light layer extending roughly `2–3.5%` of a cell edge plus only a low-to-medium global diffusion veil. The glow is obvious at thumbnail scale while flat ink cores, square gutters, footer text, subject icons, and signature cues remain crisp and readable. Add finer natural monochrome film grain with sparse medium clumps as a separate layer.

End with the strongest exclusions: no source reconstruction, no detailed object sheet, no empty generic icon sheet, no colored-pencil or sketch appearance, no hatching or descriptive linework, no photographic microdetail, no deep perspective, no hard cheap vector edges, no rectangular cells, no unequal rows or columns, no unequal top/left/right margins, no wrong cell count, no oversized or full-bleed grid, no coordinate drift, no organic distortion of the square scaffold, no dark beige paper, no smeared ink, no excessive absorption, no third color, no missing footer, no one-line default footer, no oversized footer type, no arbitrary footer geometry, no incorrect icon count, no extra text, no repeated cells, no weak glow, no smooth digital surface, no uniform noise, and no painterly or glossy rendering.

## Footer copy rules

Choose the exact copy and exact two-line break before generation. Prefer 3–7 ASCII words and 12–32 characters, with 1–4 words per line. Use user-supplied copy verbatim and change only the line break unless the user explicitly requests one line. Keep punctuation simple. Repeat both lines once near the start and once near the footer instruction when text accuracy is important.

## Footer icon rules

- Write the subject inventory explicitly before the image prompt.
- One primary subject -> exactly one icon.
- Two to five primary subjects -> exactly one icon per subject.
- More than five primary subjects -> exactly five icons for the five dominant subjects.
- State the icon count twice: once with the subject inventory and once in the footer instruction.
- Name the silhouette and distinctive cue for every icon. Keep each icon to one main fill, at most one negative cut, and at most one support mark.
- Do not ask the image model to choose a random icon count or invent decorative filler.

## Color normalization

- cobalt blue `#315EA8`
- powder blue `#9CB7CF`
- vermilion `#C84E38`
- brick red `#9F4639`
- forest green `#315D47`
- olive green `#6E7538`
- violet `#66518D`
- charcoal navy `#283743`

Use these only to resolve broad names. Obey a supplied hex value exactly. Optical texture may create microscopic tonal variation, but the designed ink system remains two-color.

## Negative block

`no visible source photograph, no photorealism, no tracing, no reconstructed source composition, no full equipment assembly, no detailed architectural opening, no brick-by-brick paving, no coherent line-art scene, no colored-pencil texture, no sketch appearance, no engraving, no cross-hatching, no contour hatching, no stippled shading, no fur strokes, no feather strokes, no leaf veins, no fine food texture, no descriptive surface scratches, no full foreground-middle-background scene, no deep converging perspective, no photographic microdetail, no architectural drafting, no razor-sharp clipping masks, no brittle polygons, no CAD-clean pictorial intersections, no generic stock icons, no empty logo sheet, no independently improvised cell frames, no rectangular cells, no tall cells, no wide cells, no unequal row heights, no unequal column widths, no unequal top left and right paper margins, no wrong cell count, no oversized grid, no full-bleed grid, no stretched grid, no coordinate drift, no optical square compensation, no organic distortion of the square scaffold, no outward fringe invading gutters, no cell-size difference beyond one output pixel, no third color, no darker beige, no yellow-brown paper, no graphic gradients, no black outlines, no drop shadows, no 3D, no wet ink, no fuzzy absorption, no smeared edges, no watercolor bleed, no excessive paper breakup, no extra text, no labels, no numbers, no logo, no watermark, no merged cells, no missing cells, no extra panels, no repeated cells, no missing footer, no one-line default footer, no oversized footer type, no footer illustration, no arbitrary footer dots, no arbitrary footer squares, no arbitrary footer rules, no filler marks, no duplicated subject icons, no incorrect subject-icon count, no miniature footer scene, no unrelated symbols inside cells, no smooth digital surface, no uniform noise overlay, no canvas weave, no cloth fibers, no dirty gray paper, no stains, no weak glow, no opaque fog, no heavy scratches`

