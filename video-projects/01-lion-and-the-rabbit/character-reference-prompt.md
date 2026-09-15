# Lion & Rabbit Reference — Generation Prompt

**Purpose:** a clean, isolated reference for this fable's two characters, so
Shots 2–6 stay visually consistent with each other. Unlike the mascot and
jungle, this is fable-specific — not reused in future videos (each fable has
its own throwaway cast per `character-bible/style-guide.md`).

**Style-matching approach:** feed BOTH locked references in as
`image_references` together, so this generation is anchored to the whole
established world, not just the text description. **Use the Higgsfield
Elements by name (preferred) — this is what went wrong on attempt 1, where
the wrong mascot job ID got attached by mistake:**
- **`Peacock-Mascot`** Element (id `0a34bbe6-8903-42b3-b56d-28b076ccfc6b`) —
  anchors the character-rendering style (painterly detail, expressive faces,
  fur/feather treatment). **Do NOT use job `8da7e0b2` — that was the
  rejected cinematic-3D mascot candidate and is almost certainly why attempt
  1 came out as a 3D render.**
- **`Neelvan-Forest`** Element (id `e59c0df0-180e-4d97-9ca1-4ac2a550ef36`) —
  anchors the palette, lighting, and magical atmosphere

**Model:** `seedream_v4_5` (same as both locked references)
**Aspect ratio:** 16:9 (not 9:16 — this is a pure reference sheet, never
shown directly, only fed into other generations; a side-by-side "lion left,
rabbit right" layout wants a wide frame, same reasoning as why the mascot
turnaround and jungle sheet are both 16:9. 9:16 was an earlier mistake here,
carried over by pattern-matching the final video's vertical format when it
didn't apply.)
**Quality:** high
**Cost:** 1 credit (confirmed via preflight; multiple references don't add cost)

---

## Prompt

**Note on background bleed:** feeding the jungle image in as a reference
carries real risk of the model pulling its literal scenery (trees, well,
river) into this background, not just its palette/lighting. The prompt below
explicitly instructs both references to inform style/palette/mood only, not
background content — this needed to be stated directly rather than assumed.

**Attempt 1 rejected — 3D render, not painterly.** First generation (below,
kept for record) came back as a glossy 3D CGI render (Pixar/DreamWorks-style
— specular highlights, rounded toy-like proportions) despite explicitly
saying "no 3D render." Text negatives alone weren't enough to override the
model's pull toward a polished 3D look, likely reinforced by the reference
images' own rendered quality. Attempt 2 below front-loads painterly-specific
positive language (watercolor bleed, visible brushwork, matte hand-painted
finish) rather than relying on negatives alone, since telling a model what
something ISN'T tends to be weaker than showing it what it IS.

### Attempt 2 (current — use this one)

```
Two-character reference sheet, side by side on a solid plain white or neutral studio background, hand-painted storybook illustration, visible watercolor brush strokes and paper texture, soft matte painted finish, flat gouache colour blocking with painterly edges, absolutely not a 3D render, not CGI, not glossy, not plastic-looking, no specular highlights, no rendered materials, absolutely no forest, no trees, no well, no scenery, no environmental elements from any reference image — reference images are for character rendering style, colour palette, and lighting mood ONLY, not for background content and not for 3D rendering quality, a majestic golden-maned lion standing tall and imposing on the left, proud and slightly arrogant expression, not smiling warmly, amber-gold fur painted with visible brushwork, a darker rich mane, a small clever brown rabbit sitting calmly and alertly on the right, soft brown fur painted with visible brushwork, bright attentive eyes, composed and unbothered expression rather than frightened, both characters facing forward, full body clearly visible, no clothing, no accessories, no props, classic fairy tale book illustration style like a children's storybook page, delicate fine linework, warm whimsical magical atmosphere with soft glowing light, timeless illustrated-storybook charm, soft-edged painterly rendering with gentle atmospheric depth, warm earthy colour palette — terracotta, marigold yellow, leaf green, deep indigo shadows, single clean reference sheet, sharp focus, high resolution, no photorealism, no flat vector, no cel-shading, no dark or moody colours, no dull or washed-out colours, no text, no watermark, no logos, no frame borders
```

### Attempt 1 (rejected, kept for record)

```
Two-character reference sheet, side by side on a solid plain white or neutral studio background, absolutely no forest, no trees, no well, no scenery, no environmental elements from any reference image — reference images are for character rendering style, colour palette, and lighting mood ONLY, not for background content, a majestic golden-maned lion standing tall and imposing on the left, arrogant proud posture, amber-gold fur with a darker rich mane, expressive face capable of showing both arrogance and sudden fury, a small clever brown rabbit sitting calmly and alertly on the right, soft brown fur, bright attentive eyes, composed and unbothered expression rather than frightened, both characters facing forward, full body clearly visible, no clothing, no accessories, no props, classic fairy tale book illustration style, richly detailed painterly watercolor and gouache textures, delicate fine linework, warm whimsical magical atmosphere with soft glowing light, timeless illustrated-storybook charm, soft-edged rendering with gentle atmospheric depth, warm earthy colour palette — terracotta, marigold yellow, leaf green, deep indigo shadows, single clean reference sheet, sharp focus, high resolution, no photorealism, no flat vector, no cel-shading, no 3D render, no dark or moody colours, no dull or washed-out colours, no text, no watermark, no logos, no frame borders
```

## Status

⚠️ **Attempt 1 rejected** — came back as a 3D render instead of painterly
illustration; background bleed was successfully avoided though. Attempt 2
above strengthens painterly-specific positive language. Regenerate with
Attempt 2 and review against the locked mascot and jungle before using as
the `image_references` input for Shots 2–6 in `shot-list.md`.