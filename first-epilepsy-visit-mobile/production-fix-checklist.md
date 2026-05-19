# Mobile Comic Production Fix Checklist

Created: 2026-05-17
Source branch: `bona-comic-update`
Review target: ready-for-review version by 2026-05-18

## Required Art Replacements

Status as of 2026-05-18: visible Marcus wardrobe replacements are complete in the public preview assets.

- `assets/generated/01-hero-cover.png`
  - Complete: Marcus no longer wears the green hoodie. The cover now shows Marcus as a late-20s adult patient in a muted teal-blue overshirt / lightweight jacket over a cream crew-neck T-shirt.
  - Keep Dr. Rehim consistent with the simplified physician design and avoid white coat / generic doctor styling.

- `assets/generated/page_08-04-journey-starts.png`
  - Complete: Marcus no longer wears the green hoodie and reads as a late-20s adult patient in the muted teal-blue overshirt / lightweight jacket wardrobe.
  - Dr. Rehim is closer to the earlier Dr. Rehim design from the 04 / Meet The Doctor panels.

## Completed Structure Edits

- `assets/generated/page_02-02-marcus-worry.png`
  - Marcus now reads as a late-20s young adult.
  - Text now reads: `I don't even know what an epileptologist does...`
- The visible prototype now removes the old `page_03-01-checking-in.png` front-desk image and keeps only `page_03-02-timeline-tip.png` for Checking In.
- The visible prototype now removes the old second Meet The Doctor image and keeps only `04a-doctor-door.png`.
- Visible Marcus wardrobe sweep completed across the cover, day-arrives panels, check-in, doctor visit, story panels, explanation panels, before-you-leave panels, and closing panel.
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
- Panel `01 / The Day Arrives`, fourth image: `But here's the thing` appears as a rectangular caption box without a speech-tail pointer.
- Patient-facing clinical language remains plain and reassuring.

## Deploy Gate

- Preview `first-epilepsy-visit-mobile/prototype/index.html` on a phone-width viewport.
- Confirm all updated images load from `first-epilepsy-visit-mobile/assets/generated/`.
- Confirm the landing redirect still preserves QR/NFC query parameters into `prototype/`.
- Remove development-only files before publish.
