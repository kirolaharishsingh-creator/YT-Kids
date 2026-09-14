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

**Consistency approach:** generate Shot 2 first — it establishes the lion and
rabbit's designs. Once you have that image, feed it back in as an
`image_references` input on Shots 3–6 so the same lion and rabbit stay
consistent across the whole fable (same technique as the mascot: reference
the actual output image, don't just repeat the text description).

### Shot 2 — Setup

```
A wide forest clearing scene, an imposing golden-maned lion standing tall and arrogant at the center, a group of forest animals — deer, monkeys, small birds — bowing nervously in a loose circle around him, a small brown rabbit standing calmly at the front of the group, dappled warm sunlight filtering through trees, classic fairy tale book illustration style, richly detailed painterly watercolor and gouache textures, delicate fine linework, warm whimsical magical atmosphere with soft glowing light, timeless illustrated-storybook charm, soft-edged rendering with gentle atmospheric depth, warm earthy colour palette — terracotta, marigold yellow, leaf green, deep indigo shadows, one clear forest-clearing location, minimal clutter, vertical 9:16 composition, sharp, high resolution, no photorealism, no flat vector, no cel-shading, no 3D render, no text, no watermark, no logos
```

### Shot 3 — Trick (a)

```
The same small brown rabbit from before, walking calmly and unhurried toward the same golden-maned lion, who looks furious and impatient, forest clearing background, tense but composed mood, classic fairy tale book illustration style, richly detailed painterly watercolor and gouache textures, delicate fine linework, warm whimsical magical atmosphere with soft glowing light, warm earthy colour palette — terracotta, marigold yellow, leaf green, deep indigo shadows, one clear location, minimal clutter, vertical 9:16 composition, sharp, high resolution, no photorealism, no flat vector, no cel-shading, no 3D render, no text, no watermark, no logos
```
*(feed Shot 2's output as `image_references` for lion/rabbit consistency)*

### Shot 4 — Trick (b)

```
The same lion and rabbit approaching the edge of an old moss-covered stone well in the forest, the rabbit gesturing toward the well, the lion peering forward with suspicion, late-afternoon warm light, classic fairy tale book illustration style, richly detailed painterly watercolor and gouache textures, delicate fine linework, warm whimsical magical atmosphere with soft glowing light, warm earthy colour palette — terracotta, marigold yellow, leaf green, deep indigo shadows, one clear location, minimal clutter, vertical 9:16 composition, sharp, high resolution, no photorealism, no flat vector, no cel-shading, no 3D render, no text, no watermark, no logos
```
*(feed Shot 2's output as `image_references`)*

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
