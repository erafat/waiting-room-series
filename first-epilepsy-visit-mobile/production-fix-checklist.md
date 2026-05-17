# Mobile Comic Production Fix Checklist

Created: 2026-05-17
Source branch: `bona-comic-update`
Review target: ready-for-review version by 2026-05-18

## Required Art Replacements

Regenerate or manually revise these panels before the next review:

- `assets/generated/page_02-02-marcus-worry.png`
  - Marcus should read as a young adult in his early 20s, not a teenager.
  - Replace the text with exactly: `I don't even know what a seizure doctor does...`

- `assets/generated/page_02-03-family-support.png`
  - Marcus should read as a young adult in his early 20s.
  - Keep the support line, but render it as background text or a caption box with no speech-tail pointer.

- `assets/generated/page_03-01-checking-in.png`
  - Receptionist/front-desk staff should be a Black woman in her 50s-60s.
  - Marcus should read as a young adult in his early 20s.

- `assets/generated/page_08-04-journey-starts.png`
  - Dr. Rehim must match the earlier Dr. Rehim design from the 04 / Meet The Doctor panels.
  - Marcus should read as a young adult in his early 20s.

## Character QA Gate

Before declaring the branch ready:

- Marcus reads consistently as an early-20s Black man across the cover, day-arrives panels, check-in, doctor visit, story panels, and closing panels.
- Dr. Rehim has the same hair, glasses, facial structure, and blazer style in the final panel as in `04a-doctor-door.png` and `04b-marcus-reaction.png`.
- The receptionist is not young/generic and clearly reads as a Black woman in her 50s-60s.
- No generated panel includes accidental page labels, prompt labels, unreadable paperwork text, or inconsistent clinic branding.

## Text QA Gate

- Panel `01 / The Day Arrives`, second image: `I don't even know what a seizure doctor does...`
- Panel `01 / The Day Arrives`, third image: support text has no speech tail.
- Patient-facing clinical language remains plain and reassuring.

## Deploy Gate

- Preview `first-epilepsy-visit-mobile/prototype/index.html` on a phone-width viewport.
- Confirm all updated images load from `first-epilepsy-visit-mobile/assets/generated/`.
- Confirm the landing redirect still preserves QR/NFC query parameters into `prototype/`.
- Remove development-only files before publish.
