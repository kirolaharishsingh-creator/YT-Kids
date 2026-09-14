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

- **Character:** an old, wise **myna bird** (chosen because mynas are a
  genuinely common storytelling narrator device in Indian folk tradition —
  not tied to any specific existing fable's cast, so it stays neutral and
  available across all stories) perched on a branch or windowsill, in the same
  fairy-tale illustration style.
- **Design:** deep brown/black feathers, a bright yellow-orange beak and eye
  patch, small reading glasses (this detail exists purely for
  personality/branding, not literal accuracy), a warm expression.
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
