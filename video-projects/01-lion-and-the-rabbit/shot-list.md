# Shot List: The Lion and the Rabbit

Each row = one AI generation. All prompts append the fixed style fragment from
`character-bible/style-guide.md`.

| # | Beat | Shot | Generation ID |
|---|------|------|--------------|
| 1 | Hook | Peacock mascot on branch, addressing camera, warm expression | ✅ `e1dd7083-a14a-4475-ae56-45e8abc4f6ed` |
| 2 | Setup | Wide: lion standing over bowing forest animals, rabbit at front | ✅ `ac8e275e-9005-4659-84f5-67688edfb0af` |
| 3 | Trick (a) | Rabbit walking calmly up to angry lion | ✅ `0c06c1ae-3213-4695-a4a7-25e67647ddd0` |
| 4 | Trick (b) | Lion and rabbit approaching edge of stone well | ✅ `f4c9b13b-5554-4208-ad2c-2eaba49c65a7` |
| 5 | Payoff (a) | Close-up: lion's reflection glaring up from well water | ✅ `1b80cde9-265d-40ad-b760-0c0d27034559` |
| 6 | Payoff (b) | Lion leaping into well / ripples settling, no lion visible | ✅ `f3db5b2e-2363-4539-9ed6-517bac10bb4b` |
| 7 | Moral | Peacock mascot again, same crest/lighting as shot 1 | ✅ `50ec919a-d570-4566-a247-6c9357b1465c` |

**Voiceover:** one continuous narration track per `scripts/lion-and-the-rabbit.md`,
same voice/TTS setting to be reused for every future fable.

**Status: all 7 shots locked.** ✅ Every still image for fable #1 is
generated and approved — see `shot-2-iteration-log.md` and
`shot-3-iteration-log.md` for the debugging history on the two hardest
shots. Next stage: animation pass (Kling), below.

---

## Generation prompts (shots 2–6)

**Consistency approach — lion+rabbit reference locked.** ✅ See
`character-reference-prompt.md` in this folder — generation `663aa18d`,
approved. Feed the **`Lion-Rabbit-Fable1`** Element into Shots 2–6 as
`image_references` (alongside the jungle reference for location — see
below) so the same lion and rabbit stay consistent across the whole fable.

**Location consistency:** Shots 2–4 use the Forest Clearing panel and Shots
4–6 use the Ancient Well panel from the locked jungle sheet. Feed the
**`Neelvan-Forest`** Element in as an additional `image_references` input
on these shots alongside the lion/rabbit reference, so this fable's forest
matches every other fable's forest.

### Shot 2 — Setup

✅ **Locked — generation `ac8e275e-9005-4659-84f5-67688edfb0af`** (`seedream_v4_5`,
9:16, high quality, 1 credit). Took 5 attempts to land — see
`shot-2-iteration-log.md` in this folder for the full history (each attempt
fixed one issue and regressed another: a background seam from the jungle
reference's multiple panels blending together, and the lion not reading as
dominant/feared). Final locked prompt below.

```
A single unbroken forest clearing scene, one continuous camera view, one consistent depth of field, not a split-screen, no panels, no seams, no dividing lines, one seamless painted environment, an imposing golden-maned lion standing tall and arrogant at the center on slightly raised ground, clearly the largest and most powerful figure in the frame, surrounded by forest animals each showing distinct individual fearful body language: on the left, one spotted deer frozen mid-step with ears pinned back and tail tucked low, ready to bolt; further left, a second spotted deer crouched low with front legs bent, head turned away avoiding the lion's gaze; on the right, one monkey curled small with arms wrapped around itself, shoulders hunched up to its ears; further right, a second monkey backing away on all fours, glancing back over its shoulder in fear; in front, four small birds each in a different startled pose — one with wings half-raised as if about to flee, one crouched flat to the ground, one facing away, one looking up wide-eyed — scattered unevenly, not in a row, not symmetrical; a small brown rabbit sitting calmly and unafraid at the very front of the group closest to camera, upright and relaxed, a clear visual contrast to every other animal's fear, dappled warm sunlight filtering through trees, classic fairy tale book illustration style, richly detailed painterly watercolor and gouache textures, delicate fine linework, warm whimsical magical atmosphere with soft glowing light, timeless illustrated-storybook charm, soft-edged rendering with gentle atmospheric depth, warm earthy colour palette — terracotta, marigold yellow, leaf green, deep indigo shadows, minimal clutter, vertical 9:16 composition, sharp, high resolution, no photorealism, no flat vector, no cel-shading, no 3D render, no text, no watermark, no logos, no mirrored poses, no duplicate animal poses, no symmetrical left-right layout
```

**Known limitation, accepted:** the model rendered 1 deer + 1 monkey + 4
birds instead of the requested 2 deer + 2 monkeys — a smaller "bowing
crowd" than scripted, but this is also why the mirroring problem
disappeared (nothing duplicate left to mirror). Traded a bigger crowd for
correct staging, no seam, and real fear in the body language.

**Reference for Shots 3-6:** feed generation `ac8e275e-9005-4659-84f5-67688edfb0af`
as `image_references` (as already planned below) so the lion/rabbit/forest
match this locked shot exactly.

### Shot 3 — Trick (a)

✅ **Locked — generation `0c06c1ae-3213-4695-a4a7-25e67647ddd0`** (`seedream_v4_5`,
9:16, high quality, 1 credit). Took 3 attempts — see
`shot-3-iteration-log.md` in this folder. Final locked prompt below.

```
A single full immersive forest scene, NOT a reference sheet, NOT two separate character portraits, ignore any grid or side-by-side layout from reference images entirely — use references only for character design, fur colour, and art style, never for composition or framing, one continuous unbroken environment, one camera, one consistent depth of field, absolutely no vertical line, no seam, no border, no split screen, no diptych, no panel divide anywhere in the image, both characters exist together naturally in the same integrated space, not mirrored, not facing each other across a centerline divide — instead, the small brown rabbit walking calmly at a natural angle across the clearing, three-quarter view, the golden-maned lion prowling toward it from a different angle and distance, overlapping naturally in perspective the way two animals sharing a real physical space would, rabbit relaxed and unbothered, ears up, composed expression, lion looming large, furious and impatient, glaring, bared teeth, tense hunched shoulders, clearly larger and more powerful than the rabbit, plain forest clearing with tall trees and dappled warm sunlight, no ancient well, no waterfall, no river, no great banyan tree, classic fairy tale book illustration style, richly detailed painterly watercolor and gouache textures, delicate fine linework, warm whimsical magical atmosphere with soft glowing light, warm earthy colour palette — terracotta, marigold yellow, leaf green, deep indigo shadows, one clear location, minimal clutter, vertical 9:16 composition, sharp, high resolution, no photorealism, no flat vector, no cel-shading, no 3D render, no text, no watermark, no logos
```

**Reference for Shot 4:** feed generation `0c06c1ae-3213-4695-a4a7-25e67647ddd0`
as `image_references` (as already planned below).

### Shot 4 — Trick (b)

✅ **Locked — generation `f4c9b13b-5554-4208-ad2c-2eaba49c65a7`** (`seedream_v4_5`,
9:16, high quality, 1 credit). First attempt approved — the anti-split-screen/
anti-landmark-bleed language carried forward from Shots 2-3 worked
immediately here. Final locked prompt below.

```
A single full immersive forest scene, NOT a reference sheet, NOT two separate character portraits, ignore any grid or side-by-side layout from reference images entirely — use references only for character design, fur colour, and art style, never for composition or framing, one continuous unbroken environment, one camera, one consistent depth of field, absolutely no vertical line, no seam, no border, no split screen, no diptych, no panel divide anywhere in the image, both characters exist together naturally in the same integrated space, not mirrored, not facing each other across a centerline divide — the same small brown rabbit and the same golden-maned lion approaching the edge of an old moss-covered stone well together, standing at slightly different depths and angles rather than mirrored, the rabbit in front gesturing with one paw toward the well opening, calm and confident expression, the lion just behind and to the side, leaning forward and peering down toward the well with deep suspicion, narrowed eyes, wary posture, clearly larger and more powerful than the rabbit, the old stone well moss-covered with a small wooden bucket on a rope, late-afternoon warm golden light, forest clearing setting with tall trees, no waterfall, no great banyan tree, no additional landmarks, classic fairy tale book illustration style, richly detailed painterly watercolor and gouache textures, delicate fine linework, warm whimsical magical atmosphere with soft glowing light, warm earthy colour palette — terracotta, marigold yellow, leaf green, deep indigo shadows, one clear location, minimal clutter, vertical 9:16 composition, sharp, high resolution, no photorealism, no flat vector, no cel-shading, no 3D render, no text, no watermark, no logos
```

**Known minor deviation, accepted:** the lion looks at the rabbit rather
than down into the well as the prompt requested — not a problem, since the
"peering into the well" beat belongs to Shot 5's reflection close-up
anyway.

**Reference for Shots 5-6:** feed generation `f4c9b13b-5554-4208-ad2c-2eaba49c65a7`
as `image_references` (as already planned below).

### Shot 5 — Payoff (a)

✅ **Locked — generation `1b80cde9-265d-40ad-b760-0c0d27034559`** (`seedream_v4_5`,
9:16, high quality, 1 credit). First attempt approved. Final locked prompt
below.

```
A single continuous close-up shot looking down into an old moss-covered stone well, one unified image, no split screen, no panel divide, no vertical or horizontal dividing line, the dark water's surface deep inside the well reflecting the face of the same golden-maned lion glaring angrily back up, furious narrowed eyes, bared teeth visible in the reflection, gentle ripples just settling around the reflected face, warm dappled light catching the water's surface and the wet stone walls of the well, moss and a few trailing vines along the stone rim visible at the edges of frame, classic fairy tale book illustration style, richly detailed painterly watercolor and gouache textures, delicate fine linework, warm whimsical magical atmosphere with soft glowing light, warm earthy colour palette — terracotta, marigold yellow, deep indigo shadows, vertical 9:16 composition, sharp, high resolution, no photorealism, no flat vector, no cel-shading, no 3D render, no text, no watermark, no logos, use reference images only for the lion's exact facial design and art style, never for composition or layout
```

**Note:** feeding Shot 2's/Shot 4's raw job ID (rather than a locked
Element) as a reference caused a `400 Bad Request` on actual submission
here, even though `get_cost` preflight accepted it — stick to the two
locked Elements (`Lion-Rabbit-Fable1`, `Neelvan-Forest`) for reference
inputs going forward, not prior shots' raw generation IDs.

**Reference for Shot 6:** no characters in that shot (empty well after the
splash) — just use `Neelvan-Forest` for the well/location design.

### Shot 6 — Payoff (b)

✅ **Locked — generation `f3db5b2e-2363-4539-9ed6-517bac10bb4b`** (`seedream_v4_5`,
9:16, high quality, 1 credit). First attempt approved. Final locked prompt
below.

```
A single continuous unbroken scene, one camera, one consistent depth of field, no split screen, no panel divide, no dividing lines, a wide view of an old moss-covered stone well standing alone in a quiet forest clearing, tall trees surrounding the clearing, water inside the well rippling outward in circles and just beginning to settle after a splash, no characters visible anywhere in the frame, empty and still, warm fading afternoon light, long soft shadows, classic fairy tale book illustration style, richly detailed painterly watercolor and gouache textures, delicate fine linework, warm whimsical magical atmosphere with soft glowing light, timeless illustrated-storybook charm, soft-edged rendering with gentle atmospheric depth, warm earthy colour palette — terracotta, marigold yellow, leaf green, deep indigo shadows, one clear location, minimal clutter, vertical 9:16 composition, sharp, high resolution, no photorealism, no flat vector, no cel-shading, no 3D render, no text, no watermark, no logos
```

### Shot 1 — Hook

✅ **Locked — generation `e1dd7083-a14a-4475-ae56-45e8abc4f6ed`** (`seedream_v4_5`,
9:16, high quality, 1 credit). First attempt approved.

```
A single continuous unbroken forest scene, one camera, one consistent depth of field, no split screen, no panel divide, no dividing lines, the same majestic peacock mascot perched gracefully on a tree branch in the forest, tail feathers trailing elegantly downward not fully fanned, addressing the camera directly with a warm, inviting, engaging expression, as if about to tell a story, small gold-rimmed reading glasses, soft warm morning sunlight filtering through leaves, forest clearing setting with tall trees, classic fairy tale book illustration style, richly detailed painterly watercolor and gouache textures, delicate fine linework, warm whimsical magical atmosphere with soft glowing light, timeless illustrated-storybook charm, soft-edged rendering with gentle atmospheric depth, warm earthy colour palette — terracotta, marigold yellow, leaf green, deep indigo shadows, one clear location, minimal clutter, vertical 9:16 composition, sharp, high resolution, no photorealism, no flat vector, no cel-shading, no 3D render, no text, no watermark, no logos, use reference images only for the peacock's exact design and art style, never for composition or layout
```

### Shot 7 — Moral

✅ **Locked — generation `50ec919a-d570-4566-a247-6c9357b1465c`** (`seedream_v4_5`,
9:16, high quality, 1 credit). Took 2 attempts — see below.

```
A single continuous unbroken forest scene, one camera, one consistent depth of field, no split screen, no panel divide, no dividing lines, the same majestic peacock mascot perched gracefully on a tree branch in the forest, an elaborate full crown-like halo of peacock-eye feathers radiating all the way around the head like a sunburst, each feather tipped with a classic blue-and-gold peacock eye-spot pattern, a small jeweled gold tiara at the center front of the head, small gold-rimmed reading glasses, large sparkling warm brown eyes, tail feathers trailing elegantly downward not fully fanned, addressing the camera directly with a warm, reassuring, knowing expression, gentle closing smile, as if wrapping up a story and sharing its lesson, soft warm golden sunlight filtering through leaves, bright daytime warm lighting matching a sunny forest clearing, not dusk, not blue-toned, forest clearing setting with tall trees, classic fairy tale book illustration style, richly detailed painterly watercolor and gouache textures, delicate fine linework, warm whimsical magical atmosphere with soft glowing light, timeless illustrated-storybook charm, soft-edged rendering with gentle atmospheric depth, warm earthy colour palette — terracotta, marigold yellow, leaf green, deep indigo shadows, one clear location, minimal clutter, vertical 9:16 composition, sharp, high resolution, no photorealism, no flat vector, no cel-shading, no 3D render, no text, no watermark, no logos, use reference images only for the peacock's exact character design and art style, never for composition or layout
```

**Attempt 1 rejected** (job `02672a65`) — used a simpler crest description
and "warm late-afternoon" lighting, producing a visibly different crest
shape from Shot 1 (compact top-fan of plain plumes vs. Shot 1's full
radiating halo of eye-spot feathers) and a cooler dusk-toned background.
Since Shots 1 and 7 bookend the same video as the same host character,
matching crest design and lighting between them was corrected for in
attempt 2 (locked above) by explicitly describing Shot 1's exact crest
structure and demanding daytime warm lighting rather than relying on
"same as before" phrasing alone.

**All 7 shots for fable #1 are now locked.** Next stage: animation.

**Aspect ratio for all shots:** 9:16 (vertical, matches the final Shorts format).

---

## Animation pass (Kling) — all 7 shots animated

Each of the 7 shots (including both mascot shots) gets animated from its
still image into a short video clip, then stitched together in editing.

**Superseded plan (kept for record):** originally assumed a uniform 3s per
clip (Kling's minimum), 21s raw footage trimmed to an 18-20s final cut,
~31.5 credits total. **This assumed the voiceover would land in the
channel's standard 15-20s target — it came in at 33.7s instead** (locked
generation `3de96755-0356-4636-999c-dc82497a5fa1`, Isla voice). Rather than
re-cut the script, the plan below stretches each clip to match its actual
narration segment.

**Settings:**
- Model: `kling3_0` (standard quality)
- Duration: **variable per shot**, matched to that shot's narration segment
  (see table below) — not a uniform 3s anymore
- Sound: **off** — narration is added separately as one continuous voiceover
  track (job `3de96755`), so Kling's built-in audio isn't needed and costs
  more for nothing
- Input: each shot's still image as `start_image`
- Aspect ratio: 9:16

**Duration per shot, matched to the 33.7s voiceover (word-count-weighted,
~34s total, trim ~0.3s in the edit):**

| Shot | Beat | Narration segment | Clip length | Motion prompt |
|---|---|---|---|---|
| 1 | Hook | "What happens when the forest's biggest bully picks on the wrong rabbit?" | 5s | Gentle idle sway, feathers softly shifting, blinking, addressing camera with warm expression |
| 2 | Setup | "Every animal had to send the lion food, or he'd hunt them all himself. Today, it was the rabbit's turn." | 6s | Animals shifting nervously, lion's mane rippling slightly, subtle ambient forest motion (leaves, light) |
| 3 | Trick (a) | "Forgive me, said the rabbit. Another lion in this forest tried to stop me, and said he rules here now." | 6s | Rabbit walking forward calmly, lion's chest heaving with anger, tail flicking |
| 4 | Trick (b) | "The lion roared. Show me." | 4s | Rabbit gesturing toward the well, lion leaning forward to look, cautious movement |
| 5 | Payoff (a) | "The lion saw his rival..." | 4s | Water rippling gently, reflection wavering, lion's reflected face reacting with sudden fury |
| 6 | Payoff (b) | "...and leapt in to fight him." | 4s | Water rippling outward from a splash, then slowly settling to stillness |
| 7 | Moral | "Moral of the story? Cleverness beats a bully every time." | 5s | Gentle idle sway, warm reassuring expression, subtle feather shimmer |

**Cost, updated for variable durations:** ~1.5 credits/sec (sound off) ×
~34s total ≈ **~51 credits** for the fully animated pilot (up from the
original ~31.5 credit estimate, because the video is now ~34s instead of
~18-20s). Confirm exact per-clip cost via `get_cost` before submitting each
one, same as the still-image workflow.
