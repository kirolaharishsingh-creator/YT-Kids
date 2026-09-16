# Shot List: The Banyan Deer's Offer

Each row = one AI generation. All prompts append the fixed style fragment
from `character-bible/style-guide.md`.

| # | Beat | Shot | Asset needed |
|---|------|------|--------------|
| 1 | Hook | Peacock mascot on branch, addressing camera, warm expression | ✅ **Reused from fable #1** — generic-talking clip `6a35ec14-57c1-4bba-8243-7e8be5f48e61`, no new generation. This fable's hook audio gets placed under the existing footage in editing. |
| 2 | Setup | Wide: two deer herds in a forest clearing, king's hunting party approaching in the distance, golden Banyan Deer standing apart | ✅ `ee8d28cb-3041-4662-be78-4ce5091673f9` |
| 3 | Turn (a) | Pregnant doe pleading before the Branch Deer's leader, who turns away | ✅ `4ffbe273-700f-4e08-9420-52c49e9ad248` (accepted with known limitations — see below) |
| 4 | Turn (b) | Doe approaching the golden Banyan Deer instead; he steps forward | New generation |
| 5 | Payoff (a) | King, blade raised, frozen at the sight of the golden deer kneeling calmly before him | New generation |
| 6 | Payoff (b) | Close on the king's expression shifting from confusion to awe | New generation |
| 7 | Moral | Peacock mascot again, same reference as shot 1 | ✅ **Reused from fable #1** — generic-talking clip `3abdf454-7684-460a-a2d2-7af777ae1fca`, no new generation. This fable's moral audio gets placed under the existing footage in editing. |

**Voiceover:** one continuous narration track per `scripts/banyan-deer.md`,
same voice/TTS setting as fable #1.

**Status:** ✅ character reference locked — ready to generate Shots 2–6
(the only shots this fable actually needs — mascot shots are fully
reused, see above).

**Character reference — locked.** ✅ **`Deer-King-Fable2`** Element (id
`4b1f663c-446c-4705-a985-4185a0eda381`) — golden Banyan Deer (natural
branching antlers, deep golden-amber fur) and the human King (simple gold
crown, red/gold royal robes), painterly storybook style, clean white
background. Locked generation `73afd901-e3c5-4199-b296-91dda007dab8`
(a text-cleanup edit of `029638c5`, removing stray on-image text). Took 2
full attempts plus one text-fix pass — see `character-reference-log.md`
in this folder for the iteration history. Feed this Element into Shots
2-6 via `<<<4b1f663c-446c-4705-a985-4185a0eda381>>>` for consistent
character design.

**Location consistency:** Shots 2–6 use the **`Neelvan-Forest`** Element
(id `e59c0df0-180e-4d97-9ca1-4ac2a550ef36`) — the same locked jungle
world-bible reference used throughout fable #1. Feed it in via the
`<<<e59c0df0-180e-4d97-9ca1-4ac2a550ef36>>>` placeholder syntax on every
generation, same as before.

### Shot 2 — Setup

✅ **Locked — generation `ee8d28cb-3041-4662-be78-4ce5091673f9`** (`seedream_v4_5`,
9:16, high quality, 1 credit). Took 2 attempts — first attempt hit the
same split-screen bug documented in fable #1's Shot 3: the `Deer-King-Fable2`
reference is itself a two-character side-by-side sheet (deer left, king
right), and this scene naturally splits into "deer content" vs. "king's
party," so the model pulled the reference's own layout directly into the
scene as a literal split-screen with a visible dividing line. Fixed with
the same "ignore reference composition/layout, use for character design
only" language that worked in fable #1. Final locked prompt below.

```
A single full immersive forest scene, NOT a reference sheet, NOT two separate character portraits, ignore any grid or side-by-side layout from reference images entirely — use references only for character design, fur colour, and art style, never for composition or framing, one continuous unbroken environment, one camera, one consistent depth of field, absolutely no vertical line, no seam, no border, no split screen, no diptych, no panel divide anywhere in the image. A wide forest clearing with two herds of deer gathered together in one natural group, each deer in a distinct individual pose (not mirrored, not duplicated), a golden-furred deer with natural branching antlers standing apart from the herds at a natural angle, calm and dignified, clearly distinct in color and bearing from the ordinary brown deer around him — this is the Banyan Deer. Far in the background, small silhouetted figures of a king's hunting party approaching on horseback along a path, non-threatening, no weapons drawn, part of the same continuous depth of field as the deer, not a separate panel. Dappled warm sunlight filtering through trees, classic fairy tale book illustration style, richly detailed painterly watercolor and gouache textures, delicate fine linework, warm whimsical magical atmosphere with soft glowing light, timeless illustrated-storybook charm, soft-edged rendering with gentle atmospheric depth, warm earthy colour palette — terracotta, marigold yellow, leaf green, deep indigo shadows, one clear location, minimal clutter, vertical 9:16 composition, sharp, high resolution, no photorealism, no flat vector, no cel-shading, no 3D render, no text, no watermark, no logos
```

**Takeaway for Shots 3-6:** any shot in this fable using the
`Deer-King-Fable2` reference should include this same "ignore reference
composition/layout" language proactively, not just shots that show both
characters together — the split-screen risk applies whenever the scene's
own content happens to divide into two distinct halves.

### Shot 3 — Turn (a)

✅ **Locked — generation `4ffbe273-700f-4e08-9420-52c49e9ad248`** (`seedream_v4_5`,
9:16, high quality, 1 credit). Took 3 attempts — see
`character-reference-log.md`-style history below. **Accepted with two
known limitations**, both explicitly approved rather than fixed:

1. **Landmark bleed:** the background pulled in the Great Banyan Tree
   (lanterns, vines) and a waterfall from the `Neelvan-Forest` multi-panel
   reference, instead of the plain clearing the prompt asked for. Root
   cause: `Neelvan-Forest` alone (not just `Deer-King-Fable2`) can bleed
   multiple panels together — the prompt for this shot didn't include the
   explicit landmark exclusions ("no waterfall, no banyan tree, no
   additional landmarks") that fixed this same issue in fable #1's Shot 3.
   **Add that exclusion language proactively to Shots 4-6's prompts.**
2. **Understated emotion:** neither deer's "pleading" or "dismissive"
   body language reads strongly at this framing/distance — both look
   fairly neutral/calm rather than actively imploring or refusing.

```
A single full immersive forest scene, NOT a reference sheet, NOT two separate character portraits, ignore any grid or side-by-side layout from reference images entirely — use references only for palette and art style, never for composition or framing, one continuous unbroken environment, one camera, one consistent depth of field, absolutely no vertical line, no seam, no border, no split screen, no diptych, no panel divide anywhere in the image, both characters exist together naturally in the same integrated space, sharing the same depth of field and lighting, not mirrored, not facing each other across a centerline divide. A pregnant doe, visibly rounded belly, ordinary brown fur, standing at a natural angle with an imploring, pleading posture, ears back, head slightly lowered. Facing her at a different angle and distance within the same continuous space, an older, senior-looking brown deer with large antlers denoting leadership — the Branch Deer's leader — turning his body away dismissively, unmoved expression, refusing her. Both deer clearly occupy the same forest ground, overlapping naturally in perspective the way two animals sharing a real physical space would. Dappled warm sunlight filtering through trees, classic fairy tale book illustration style, richly detailed painterly watercolor and gouache textures, delicate fine linework, warm whimsical magical atmosphere with soft glowing light, timeless illustrated-storybook charm, soft-edged rendering with gentle atmospheric depth, warm earthy colour palette — terracotta, marigold yellow, leaf green, deep indigo shadows, one clear location, minimal clutter, vertical 9:16 composition, sharp, high resolution, no photorealism, no flat vector, no cel-shading, no 3D render, no text, no watermark, no logos
```

**Note:** this locked version does NOT feed the `Deer-King-Fable2` Element
(neither deer here is the locked Banyan Deer or King) — only
`Neelvan-Forest`. This avoided the split-screen bug entirely (unlike an
earlier attempt that re-added `Deer-King-Fable2` and split again despite
much stronger anti-split-screen language, confirming that reference is a
strong enough visual pull that removing it is more reliable than
instructing around it whenever it isn't actually needed for character
identity).

**Lessons carried over from fable #1's production** (see
`video-projects/01-lion-and-the-rabbit/shot-2-iteration-log.md` and
`shot-3-iteration-log.md` for the full detail) — apply these to every
prompt for Shots 2–6:
- Include explicit anti-split-screen/anti-panel language ("single
  continuous unbroken scene, one camera, one consistent depth of field, no
  split screen, no panel divide, no dividing lines") on every shot, since
  the jungle reference sheet has multiple panels that can bleed together,
  and any shot with just two characters facing each other risks pulling a
  reference sheet's own side-by-side layout.
- When a shot needs multiple animals of the same species (e.g. two deer
  herds), describe each individual's pose separately rather than as a
  group, to avoid mirrored/duplicate-looking poses.
- Describe fear/tension/emotion with specific physical cues (ears back,
  tail tucked, hunched shoulders) rather than generic adjectives like
  "nervous," which tends to render as calm/neutral instead.
