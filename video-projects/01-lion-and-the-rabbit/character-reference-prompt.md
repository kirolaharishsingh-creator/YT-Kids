# Lion & Rabbit Reference — Generation Prompt

**Purpose:** a clean, isolated reference for this fable's two characters, so
Shots 2–6 stay visually consistent with each other. Unlike the mascot and
jungle, this is fable-specific — not reused in future videos (each fable has
its own throwaway cast per `character-bible/style-guide.md`).

**Style-matching approach:** feed BOTH locked references in as
`image_references` together, so this generation is anchored to the whole
established world, not just the text description:
- **Mascot** (job `4ec59e46-1a00-4a0c-9af4-494798847350`) — anchors the
  character-rendering style (painterly detail, expressive faces, fur/feather
  treatment)
- **Jungle** (job `e397fad4-d452-47c8-a77d-ae5050fbf224`) — anchors the
  palette, lighting, and magical atmosphere

**Model:** `seedream_v4_5` (same as both locked references)
**Aspect ratio:** 9:16 · **Quality:** high
**Cost:** 1 credit (confirmed via preflight; multiple references don't add cost)

---

## Prompt

```
Two-character reference sheet, side by side on a simple plain background, a majestic golden-maned lion standing tall and imposing on the left, arrogant proud posture, amber-gold fur with a darker rich mane, expressive face capable of showing both arrogance and sudden fury, a small clever brown rabbit sitting calmly and alertly on the right, soft brown fur, bright attentive eyes, composed and unbothered expression rather than frightened, both characters facing forward, full body clearly visible, no clothing, no accessories, no props, classic fairy tale book illustration style, richly detailed painterly watercolor and gouache textures, delicate fine linework, warm whimsical magical atmosphere with soft glowing light, timeless illustrated-storybook charm, soft-edged rendering with gentle atmospheric depth, warm earthy colour palette — terracotta, marigold yellow, leaf green, deep indigo shadows, simple soft neutral background, no scenery details, single clean reference sheet, sharp focus, high resolution, no photorealism, no flat vector, no cel-shading, no 3D render, no dark or moody colours, no dull or washed-out colours, no text, no watermark, no logos
```

## Status

⬜ Not yet generated. Once generated, review against the locked mascot and
jungle for style consistency before using as the `image_references` input
for Shots 2–6 in `shot-list.md`.