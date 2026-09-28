# Request modes

## Source Transform

Inspect every source image, then keep three to five high-value anchors: a dominant contour, one or two signature parts, one material or motion behavior, and optionally one shallow relation. Treat the source as a cue pool rather than a composition to trace. Preserve only two to four signature cues across the full grid. Remove incidental lighting, photographic microtexture, repeated minor parts, background clutter, detailed assemblies, and most construction detail.

Use the attached image as a semantic and structural reference only. Do not promise exact identity or product fidelity; this system intentionally reinterprets.

Separately count primary semantic subjects for footer icons. Count concrete subjects or distinct objects that materially define the request; do not count lighting, texture, motion, color, background clutter, or repeated instances of the same subject as additional subjects.

## Theme Compose

Use this mode when no image is supplied. Parse the text into two to five concrete anchors and one relation or mood. For “road, beach, and sea,” useful anchors are curve, lane rhythm, sand field, horizon, foam, and travel. Keep recognition collective: use a few noun-specific cues and let most cells interpret motion, material, contour, reflection, or negative space. Do not invent a complete realistic beach scene.

Plan all cells from the stated theme: nine or four in portrait, or six or four in landscape. Do not claim to have inspected a source. Use ordinary world knowledge only to make the requested nouns imageable. Generate with only the selected structural layout guide attached.

## Source + Added Subject

Use the source for three to five balanced anchors and treat the requested addition as a separate subject role.

- If the addition is text-only and generic, such as a bicycle, umbrella, bird, or car, construct it from the description without asking for an image.
- If exact identity, character design, artwork, pet markings, or product geometry matters, request or use an added-subject reference image.
- Label a second image as **added-subject reference**, not a style reference or edit target.
- Allocate two to four portrait cells or one to three landscape cells to the addition: at least one isolated reduction, at least one relationship with a source anchor when two or more addition cells are used, and optionally one abstract trace or material behavior. Do not render a detailed whole-subject study unless identity requires it.
- Keep at least five portrait cells or three landscape cells primarily grounded in the original source system. Never paste the added subject into every cell.
- Give the added subject the same medium-flat abstraction, soft printed edges, palette, paper, and glow as everything else.

## Footer copy

Choose the exact English copy before compiling the image prompt.

- Prefer 3–7 ASCII words and 12–32 characters.
- Use exactly two short left-aligned lines by default. Choose the line break before generation and preserve it exactly. Aim for 1–4 words per line and similar visual width without forcing equal character counts.
- Describe the shared idea, not every cell: `ROAD, SAND AND SEA`, `A QUIET COASTAL TURN`, `NIGHT BIRDS OVER WATER`.
- Use uppercase for short noun phrases; use sentence case only when it reads more naturally.
- Allow commas and periods; avoid quotation marks, slashes, symbols, dates, coordinates, and long punctuation.
- If the user supplies copy, preserve every character and break it naturally into two lines unless the user explicitly requests one line. If it cannot fit two short lines, warn that small image text may distort and offer a shorter version.

## Footer subject icons

Choose footer icon identities before compiling the prompt.

- If there is one primary subject, create exactly one icon. This single-subject rule overrides any general two-to-five range.
- If there are two to five primary subjects, create exactly one icon per subject.
- If there are more than five primary subjects, select the five most semantically important and create exactly five icons.
- Treat repeated instances of one subject as one icon type. Do not repeat an icon merely to fill space.
- In Source + Added Subject mode, include an icon for the added subject when it is semantically primary; keep the total at five or fewer.
- In Theme Compose mode, use the concrete theme nouns as subjects. Abstract words such as mood, motion, silence, travel, heat, or memory do not receive icons unless the request explicitly personifies them.
- Give each icon one unmistakable subject cue while reducing it to one main filled silhouette, at most one negative-space cut, and at most one supporting mark. Do not use arbitrary dots, squares, rules, rings, arcs, or brackets as decoration unless they are necessary parts of the subject icon.

