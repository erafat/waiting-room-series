---
title: "Epilepsy First Visit Mobile Redesign"
delivery: mobile_web
lead_model: openai_image_2
created: 2026-04-23
---

# Epilepsy First Visit Mobile Redesign

This folder is the mobile-first remake of the epilepsy first-visit comic.

The old version was a print-minded comic page stack:
- multiple panels per page
- dialogue rendered inside the image
- good tone, but too dense for a phone

The new version is a mobile reading system:
- one core idea per screen
- real HTML/CSS text outside the generated art
- fewer generated scenes, each doing more emotional and narrative work
- designed for NFC / waiting-room use on an actual phone

## Core Production Rules

1. Use Image 2.0 for scene art, character consistency, mood, and environment.
2. Do not rely on the model to render long speech balloons, checklist text, or medical explanation text.
3. Keep critical copy in HTML/CSS so it stays editable, accessible, and readable on mobile.
4. Treat each screen as a card in a vertical story, not as a shrunken comic page.
5. Prefer 4:5 portrait scene art inside a scrolling page instead of full-page multi-panel comics.

## Character Consistency

Use [prompts/character-consistency-method.md](./prompts/character-consistency-method.md) as the repeatable workflow for recurring-character generation.

Short version:
- lock one active character-sheet anchor before scene work
- use real photos only to preserve broad likeness, not portrait detail
- keep the recurring character at the same detail level as the rest of the cast
- regenerate one scene at a time and version outputs before replacing anything

## What Carries Forward

- Marcus + family + Dr. Rehim as the core cast
- warm reassuring tone
- clear explanation of what happens in the visit
- emphasis on partnership, not intimidation

## What Changes

- the story becomes a vertical beat sequence
- heavy text pages become a mix of scene cards, text cards, and checklist cards
- the generated artwork becomes cleaner and more art-directed
- the waiting-room / check-in use case becomes the primary context

## Recommended Production Order

1. Review [storyboard.md](./storyboard.md)
2. Lock the copy in [content-script.md](./content-script.md)
3. Generate pilot scenes from `prompts/`
4. Replace placeholder art in `prototype/index.html`
5. Test on an actual phone in the clinic context
6. Only then generate the rest of the scene set

## Folder Map

- [storyboard.md](./storyboard.md): mobile beat structure
- [content-script.md](./content-script.md): exact screen copy
- [prompts/00-style-system.md](./prompts/00-style-system.md): Image 2.0 art system
- [prompts/01-cover-hero.md](./prompts/01-cover-hero.md): hero prompt
- [prompts/02-check-in-scene.md](./prompts/02-check-in-scene.md): check-in prompt
- [prompts/03-meeting-doctor-scene.md](./prompts/03-meeting-doctor-scene.md): consultation prompt
- [prompts/05-tell-your-story-scene.md](./prompts/05-tell-your-story-scene.md): history / listening prompt
- [prompts/06-before-during-after-scene.md](./prompts/06-before-during-after-scene.md): seizure-sequence prompt
- [prompts/06-full-story-scene.md](./prompts/06-full-story-scene.md): optional full-story explainer prompt based on the original print page
- [prompts/07-making-sense-scene.md](./prompts/07-making-sense-scene.md): explanation prompt
- [prompts/character-consistency-method.md](./prompts/character-consistency-method.md): repeatable image-consistency workflow
- [prompts/04-next-steps-scene.md](./prompts/04-next-steps-scene.md): departure / plan prompt
- [prototype/index.html](./prototype/index.html): mobile demo using real text and temporary placeholder art
- [assets/generated/README.md](./assets/generated/README.md): destination for final Image 2.0 assets
