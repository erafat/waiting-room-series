---
title: "Image 2.0 Style System"
lead_reference: "images-2-indie-comic"
use_case: illustration-story
created: 2026-04-23
---

# Image 2.0 Style System

## Intent

Generate scene art for a mobile-first medical explainer comic about a patient's first seizure doctor visit.

The art should feel:
- warm
- editorial
- human
- tactile
- calm rather than dramatic

The best-fit reference direction is the `images-2-indie-comic` branch from the local Image 2.0 style guide.

## What To Keep From The Existing Comic

- Marcus in an olive hoodie
- supportive mother in burgundy
- father in gray polo
- Dr. Rehim in gray blazer and clear glasses
- warm clinic environment
- approachable, non-threatening tone

## What To Change

- no multi-panel page compositions
- no giant speech balloons
- no long explanatory text inside the image
- stronger composition and more intentional negative space
- cleaner emotional focus per scene

## Generation Rules

1. Generate one scene at a time.
2. Use portrait composition sized for a mobile card.
3. Keep all critical text out of the image.
4. Avoid comic-panel borders unless a specific prompt asks for a two-moment split.
5. Do not include readable paperwork, forms, or medical chart text.
6. Keep the clinic modern, calm, bright, and believable.

## Character Lock

- Marcus: early-20s Black man, short fade, olive green hoodie, dark jeans, white sneakers
- Mrs. Johnson: Black woman, shoulder-length natural curls, burgundy cardigan, cream blouse
- Mr. Johnson: Black man, gray polo, khaki pants, broadest silhouette
- Dr. Rehim: light olive skin, dark side-swept hair, clear glasses, gray blazer, dark shirt, no white coat

## House Prefix

Use this at the start of each Image 2.0 prompt:

`Art-directed editorial comic illustration with tactile analog texture, warm human-centered storytelling, restrained palette, soft paper grain, generous negative space, emotionally legible body language, and composition designed for a mobile vertical reading experience.`

## Shared Constraints

- no speech balloons
- no readable text embedded in the art
- no stock-photo realism
- no glossy CGI finish
- no harsh hospital drama
- no cluttered background
- no medical horror cues

## Prompt Skeleton

```text
Use case: illustration-story
Asset type: mobile web comic scene card
Primary request: <one scene only>
Subject: Marcus, his parents, and/or Dr. Rehim
Scene/backdrop: modern neurology clinic, waiting room, consult room, or clinic exterior
Style/medium: warm indie comic editorial illustration with subtle paper grain
Composition/framing: portrait 4:5, clear focal point, readable on a phone
Lighting/mood: soft daylight, reassuring, calm
Color palette: cream, warm charcoal, olive, burgundy, muted teal accents
Materials/textures: off-white paper, inked outlines, soft watercolor wash
Constraints: no speech balloons, no readable text, no panel grid unless explicitly requested
Avoid: glossy CGI, photorealism, medical fear imagery, busy background clutter
```

## Pilot Deliverables

Generate these first:
- cover / hero
- check-in scene
- meeting doctor scene
- leaving with a plan scene
