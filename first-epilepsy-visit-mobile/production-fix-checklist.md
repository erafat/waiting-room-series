# Mobile Comic Production Fix Checklist

Created: 2026-05-17
Source branch: `bona-comic-update`
Review target: ready-for-review version by 2026-05-18

## Required Art Replacements

Regenerate or manually revise these visible panels before the next review:

- `assets/generated/01-hero-cover.png`
  - Required wardrobe change: Marcus should no longer wear the green hoodie. Regenerate the cover with Marcus as a late-20s adult patient in a muted teal-blue overshirt or lightweight chore jacket over a cream crew-neck T-shirt, dark straight-leg jeans or chinos, and clean white sneakers.
  - Keep Dr. Rehim consistent with the simplified physician design and avoid white coat / generic doctor styling.

- `assets/generated/page_02-03-family-support.png`
  - Visual QA 2026-05-17: Marcus now reads closer to adult, but the support line still has a speech-balloon tail.
  - Required fix: keep the support line, but render it as background text or a caption box with no speech-tail pointer.

- `assets/generated/page_08-04-journey-starts.png`
  - Dr. Rehim must match the earlier Dr. Rehim design from the 04 / Meet The Doctor panels.
  - Marcus should read as a late-20s adult patient and should no longer wear the green hoodie; use the muted teal-blue overshirt / lightweight chore jacket wardrobe.

## Completed Structure Edits

- `assets/generated/page_02-02-marcus-worry.png`
  - Marcus now reads as a late-20s young adult.
  - Text now reads: `I don't even know what an epileptologist does...`
- The visible prototype now removes the old `page_03-01-checking-in.png` front-desk image and keeps only `page_03-02-timeline-tip.png` for Checking In.
- The visible prototype now removes the old second Meet The Doctor image and keeps only `04a-doctor-door.png`.
- Unused generated assets removed from the public folder:
  - `assets/generated/page_03-01-checking-in.png`
  - `assets/generated/04b-marcus-reaction.png`
  - `assets/generated/04c-doctor-explains.png`

## Character QA Gate

Before declaring the branch ready:

- Marcus reads consistently as a late-20s Black man across the cover, day-arrives panels, check-in, doctor visit, story panels, and closing panels.
- Marcus uses the adult-casual wardrobe consistently where visible: muted teal-blue overshirt or lightweight chore jacket over a cream crew-neck T-shirt, dark straight-leg jeans or chinos, clean white sneakers; no green hoodie or sweatshirt.
- Dr. Rehim has the same hair, glasses, facial structure, and blazer style in the final panel as in `04a-doctor-door.png`.
- No generated panel includes accidental page labels, prompt labels, unreadable paperwork text, or inconsistent clinic branding.

## Text QA Gate

- Panel `01 / The Day Arrives`, second image: `I don't even know what an epileptologist does...`
- Panel `01 / The Day Arrives`, third image: support text has no speech tail. Still pending as of 2026-05-17 visual QA.
- Patient-facing clinical language remains plain and reassuring.

## Deploy Gate

- Preview `first-epilepsy-visit-mobile/prototype/index.html` on a phone-width viewport.
- Confirm all updated images load from `first-epilepsy-visit-mobile/assets/generated/`.
- Confirm the landing redirect still preserves QR/NFC query parameters into `prototype/`.
- Remove development-only files before publish.
