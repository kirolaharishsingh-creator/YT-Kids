# Visual & Narration Style Guide

Purpose: every fable has a different animal cast, so the channel's visual
consistency has to come from **art style + a recurring host character**, not
from reusing the same characters story to story. Follow this on every
generation so the channel reads as one show, not disconnected clips.

## Art style (use in every image/video generation prompt)

- **Style:** classic **fairy tale book illustration** — richly detailed,
  painterly watercolor/gouache textures, delicate fine linework, warm whimsical
  magical atmosphere with soft glowing light, timeless illustrated-storybook
  charm, soft-edged rendering with gentle atmospheric depth. No photorealism,
  no flat vector/cel-shading, no 3D render. (Photorealistic AI humans/animals
  are the fastest way to look like generic AI slop and to hit inconsistency
  problems face-to-face.)
- **Palette:** warm earthy tones (terracotta, marigold yellow, leaf green, deep
  indigo night skies) — evokes Indian folk-art without copying a specific
  copyrighted illustration style. Add soft magical highlights/glow sparingly
  (candlelight, moonlight, dawn light) to reinforce the fairy tale feel.
- **Line/shape language:** delicate, detailed, expressive — painterly rather
  than flat/graphic, but should still read clearly at small Shorts thumbnail
  size and at a glance while scrolling.
- **Backgrounds:** minimal but specific (a riverbank, a palace courtyard, a
  forest clearing) — one clear location per shot, softly painted with
  atmospheric depth, no clutter.

Keep a fixed prompt fragment (the lines above, condensed) and append it to
every single generation prompt, fable after fable, so the model's output stays
visually consistent even though the animal/human cast changes each time.

## Recurring host: the narrator mascot

To give the channel a recognizable face despite the cast changing every video,
every fable opens and/or closes on the same narrator character.

- **Character:** a majestic **peacock** (switched from parrot, then myna — the
  brief was "feathery, beautiful, a colour-goddess type icon people stop
  scrolling for," and the peacock is the natural answer: it's India's national
  bird, defined by extravagant, jewel-toned plumage, and reads as grand and
  eye-catching on sight, not just "colorful"). **Important boundary, carried
  over from the channel's earlier direction:** this is styled as a majestic
  *animal* character — regal, ornate, "goddess-like" in visual grandeur only —
  never a literal deity or religious figure. Keeps the channel clear of the
  religious-depiction risk already ruled out earlier. Perched gracefully on a
  branch or palace balustrade, in the same fairy-tale illustration style.
- **Design:** richly, *fully* feathered and jewel-toned, built to be the single
  most eye-catching thing on screen — a confident, regal **"queen" presence**,
  not a soft/pretty portrait. Iridescent sapphire-blue neck and breast,
  emerald-green back, teal and gold highlights, a tall ornate crown-like crest
  of feathers atop the head (reads as a crown, not just a small tuft), full
  voluminous layered plumage across the whole body — not just the tail — so
  the character feels lush and abundant rather than sparse. An elegant long
  tail with the classic peacock "eye"-spot feather pattern, worn gracefully
  trailing/folded in standard poses (not fully fanned open, so the character
  stays compact and readable at small thumbnail size — a full fanned display
  is a possible special "hero" pose for later, not the default). Sharp, clear,
  well-defined facial features (not soft-focus or hazy), confident direct
  gaze, dramatic rather than gentle lighting, large expressive eyes, a
  dignified regal expression, small delicate gold-rimmed reading glasses
  (keeps the wise-narrator personality thread — easy to drop if it undercuts
  the regal tone). Crisp, high-definition rendering throughout — never blurry,
  hazy, or dim/gloomy in tone.
- **Role:** delivers the hook line at the start ("Do you know what happens when
  a crow gets too clever...") and the moral at the end. The middle of the video
  is the fable itself, told in-scene without the mascot present.
- **Why this solves the consistency problem:** you only need to keep ONE
  character consistent across every video (the mascot), not the entire rotating
  cast — a much smaller, achievable version of the character-consistency
  problem.

**Before generating the mascot for the first time**, produce a dedicated
character reference/turnaround image and reuse that exact reference (same seed
image / same reference asset) in every subsequent generation that includes the
mascot, rather than re-describing it from text each time. Store that reference
image in `character-bible/` once generated.

## Narration voice

- Same narrator voice (same TTS voice or same voice actor) every single video —
  this matters as much as visual consistency for brand recognition.
- Pace: fast but clear — a 15–20 second video has no room for dead air.
- Structure: **Hook (2-3s) → Story (10-14s) → Moral (2-3s)**.

## On-screen text

- Fable title, small, top or bottom corner, consistent font/position every
  video.
- The moral repeated as on-screen text in the final 2-3 seconds (helps
  accessibility and rewatch/screenshot value).
