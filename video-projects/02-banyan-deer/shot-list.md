# Shot List: The Banyan Deer's Offer

Each row = one AI generation. All prompts append the fixed style fragment
from `character-bible/style-guide.md`.

| # | Beat | Shot | Asset needed |
|---|------|------|--------------|
| 1 | Hook | Peacock mascot on branch, addressing camera, warm expression | ✅ **Reused from fable #1** — generic-talking clip `6a35ec14-57c1-4bba-8243-7e8be5f48e61`, no new generation. This fable's hook audio gets placed under the existing footage in editing. |
| 2 | Setup | Wide: two deer herds in a forest clearing, king's hunting party approaching in the distance, golden Banyan Deer standing apart | New generation |
| 3 | Turn (a) | Pregnant doe pleading before the Branch Deer's leader, who turns away | New generation |
| 4 | Turn (b) | Doe approaching the golden Banyan Deer instead; he steps forward | New generation |
| 5 | Payoff (a) | King, blade raised, frozen at the sight of the golden deer kneeling calmly before him | New generation |
| 6 | Payoff (b) | Close on the king's expression shifting from confusion to awe | New generation |
| 7 | Moral | Peacock mascot again, same reference as shot 1 | ✅ **Reused from fable #1** — generic-talking clip `3abdf454-7684-460a-a2d2-7af777ae1fca`, no new generation. This fable's moral audio gets placed under the existing footage in editing. |

**Voiceover:** one continuous narration track per `scripts/banyan-deer.md`,
same voice/TTS setting as fable #1.

**Status:** ready to generate Shots 2–6 (the only shots this fable actually
needs — mascot shots are fully reused, see above). A fable-specific
character reference sheet (deer + king) should be generated and locked
first, same process as `video-projects/01-lion-and-the-rabbit/character-reference-prompt.md`.

**Location consistency:** Shots 2–6 use the **`Neelvan-Forest`** Element
(id `e59c0df0-180e-4d97-9ca1-4ac2a550ef36`) — the same locked jungle
world-bible reference used throughout fable #1. Feed it in via the
`<<<e59c0df0-180e-4d97-9ca1-4ac2a550ef36>>>` placeholder syntax on every
generation, same as before.

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
