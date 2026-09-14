# Forest Location Sheet — Generation Prompt

**Purpose:** the location equivalent of the mascot's character turnaround —
one generation that locks in every recurring landmark's look, so future
fables reference the same forest instead of a new one each time.

**Composition:** four-panel location reference sheet, one panel per landmark,
consistent style/palette/lighting across all panels (same idea as the
mascot's turnaround sheet, adapted for places instead of a character).
**Style:** classic fairy tale book illustration — same as `character-bible/style-guide.md`
**Aspect ratio:** 16:9 · **Resolution:** 2K

---

## Prompt

```
Four-panel location reference sheet, evenly spaced in a row, each panel clearly showing one distinct location from the same forest, consistent art style, palette, and lighting across all four panels so they clearly belong to the same world, classic fairy tale book illustration style, richly detailed painterly watercolor and gouache textures, delicate fine linework, warm whimsical magical atmosphere with soft glowing light, timeless illustrated-storybook charm, soft-edged rendering with gentle atmospheric depth, warm earthy colour palette — terracotta, marigold yellow, leaf green, deep indigo shadows, lush Himalayan-foothills-inspired jungle,

panel one: an ancient moss-covered stone well in a quiet sunlit forest clearing, dappled warm light, soft grass and wildflowers around the base,

panel two: an enormous ancient banyan tree at the heart of the forest, thick aerial roots hanging down like curtains, massive gnarled trunk, dappled light filtering through the huge canopy,

panel three: a wide open forest clearing surrounded by tall trees, soft grass, warm afternoon light, empty and inviting, the kind of place where animals could gather,

panel four: a clear winding river cutting through the forest, smooth stones along the bank, overhanging greenery, distant misty snow-capped mountains visible through a gap in the trees,

no characters, no animals, no people visible in any panel, empty environments only, sharp focus, high resolution, professional environment concept art quality, consistent single cohesive art style across all four panels, no text, no watermark, no logos, no frame borders, no photorealism, no flat vector, no cel-shading, no 3D render, no dark or moody colours, no dull or washed-out colours
```

## Notes

- **No characters in this reference** — it's a pure environment/location
  sheet. Characters (lion, rabbit, deer, mascot, etc.) get composited into
  these locations in each fable's actual scene generations, using this
  sheet as the `image_references` input for consistent background style.
- If a future fable needs a landmark not covered here (a river crossing, a
  mountain path, a royal courtyard for the Akbar-Birbal fables), generate an
  additional panel/sheet using the same style fragment and add it to
  `world-bible/` rather than inventing the look from scratch each time.

## Status

⬜ Not yet generated.