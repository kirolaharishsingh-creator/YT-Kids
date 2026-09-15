# Shot List: The Lion and the Rabbit

Each row = one AI generation. All prompts append the fixed style fragment from
`character-bible/style-guide.md`.

| # | Beat | Shot | Asset needed |
|---|------|------|--------------|
| 1 | Hook | Peacock mascot on branch, addressing camera, warm expression | Reuse mascot-peacock-final.png as image_references |
| 2 | Setup | Wide: lion standing over bowing forest animals, rabbit at front | New generation |
| 3 | Trick (a) | Rabbit walking calmly up to angry lion | New generation |
| 4 | Trick (b) | Lion and rabbit approaching edge of stone well | New generation |
| 5 | Payoff (a) | Close-up: lion's reflection glaring up from well water | New generation |
| 6 | Payoff (b) | Lion leaping into well / ripples settling, no lion visible | New generation |
| 7 | Moral | Peacock mascot again, same reference as shot 1 | Reuse mascot-peacock-final.png as image_references |

**Voiceover:** one continuous narration track per `scripts/lion-and-the-rabbit.md`,
same voice/TTS setting to be reused for every future fable.

**Status:** mascot locked and reference image in repo
(`character-bible/mascot-peacock-final.png`) — ready to generate this
fable's remaining shots.

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

```
Close-up shot looking down into an old stone well, the reflection of the same golden-maned lion glaring angrily back up from the water's surface, ripples just settling around the reflection, warm dappled light catching the water, classic fairy tale book illustration style, richly detailed painterly watercolor and gouache textures, delicate fine linework, warm whimsical magical atmosphere with soft glowing light, warm earthy colour palette — terracotta, marigold yellow, deep indigo shadows, vertical 9:16 composition, sharp, high resolution, no photorealism, no flat vector, no cel-shading, no 3D render, no text, no watermark, no logos
```
*(feed Shot 2's output as `image_references` for the lion's exact appearance)*

### Shot 6 — Payoff (b)

```
An old moss-covered stone well in a quiet forest clearing, water rippling and settling after a splash, no characters visible, empty and still, warm fading afternoon light, classic fairy tale book illustration style, richly detailed painterly watercolor and gouache textures, delicate fine linework, warm whimsical magical atmosphere with soft glowing light, warm earthy colour palette — terracotta, marigold yellow, leaf green, deep indigo shadows, one clear location, minimal clutter, vertical 9:16 composition, sharp, high resolution, no photorealism, no flat vector, no cel-shading, no 3D render, no text, no watermark, no logos
```

**Aspect ratio for all shots:** 9:16 (vertical, matches the final Shorts format).

---

## Animation pass (Kling) — all 7 shots animated

Each of the 7 shots (including both mascot shots) gets animated from its
still image into a short video clip, then stitched together in editing.

**Settings:**
- Model: `kling3_0` (standard quality)
- Duration: 3 seconds per clip (Kling's minimum — trim to each beat's exact
  timing in the edit; total raw footage 21s trimmed down to the 18s final cut)
- Sound: **off** — narration is added separately as one continuous voiceover
  track per `scripts/lion-and-the-rabbit.md`, so Kling's built-in audio isn't
  needed and costs more for nothing
- Input: each shot's still image as `start_image`
- Aspect ratio: 9:16

**Confirmed cost (preflight-checked, no credits spent):** 4.5 credits per
3-second clip × 7 shots = **~31.5 credits total** for the fully animated pilot.

**Animation prompts** — keep these simple; the still image already carries
the design, the animation prompt just needs to describe the *motion*:

| Shot | Motion prompt |
|---|---|
| 1 (mascot hook) | Gentle idle sway, feathers softly shifting, blinking, addressing camera with warm expression |
| 2 (setup) | Animals shifting nervously, lion's mane rippling slightly, subtle ambient forest motion (leaves, light) |
| 3 (trick a) | Rabbit walking forward calmly, lion's chest heaving with anger, tail flicking |
| 4 (trick b) | Rabbit gesturing toward the well, lion leaning forward to look, cautious movement |
| 5 (payoff a) | Water rippling gently, reflection wavering, lion's reflected face reacting with sudden fury |
| 6 (payoff b) | Water rippling outward from a splash, then slowly settling to stillness |
| 7 (mascot moral) | Gentle idle sway, warm reassuring expression, subtle feather shimmer |
