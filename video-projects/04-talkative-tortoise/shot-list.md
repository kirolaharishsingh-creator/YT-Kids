# Shot List: The Talkative Tortoise

Each row = one AI generation. All prompts append the fixed style fragment
from `character-bible/style-guide.md`.

| # | Beat | Shot | Asset needed |
|---|------|------|--------------|
| 1 | Hook | Peacock mascot on branch, addressing camera, warm expression | ✅ **Reused from fable #1** — generic-talking clip `6a35ec14-57c1-4bba-8243-7e8be5f48e61`, no new generation. |
| 2 | Setup | Dried, cracked pond; tortoise and two geese huddled, tortoise gesturing at a stick, geese wary | New generation |
| 3 | Turn | Tortoise airborne gripping a stick, a goose on each end, tiny village figures below pointing/laughing | New generation |
| 4 | Payoff | Close on tortoise's straining face opening his mouth, then cut to the stick falling / empty air — no impact shown | New generation |
| 5 | Moral | Peacock mascot again, same reference as shot 1 | ✅ **Reused from fable #1** — generic-talking clip `3abdf454-7684-460a-a2d2-7af777ae1fca`, no new generation. |

**Voiceover:** one continuous narration track per `scripts/talkative-tortoise.md`,
same voice/TTS setting as every prior fable. Confirm actual generated
duration against the ~18-20s target before locking animation durations.

**Status:** not yet started. Before generating Shots 2-4, first generate
and lock a fable-specific character reference sheet (tortoise + two geese),
same process as fable #1's `character-reference-prompt.md`.

**Location consistency:** Shot 2 (pond/drought) can use the **`Neelvan-Forest`**
Element (id `e59c0df0-180e-4d97-9ca1-4ac2a550ef36`) for a forest-adjacent
dried pond, consistent with the world-bible. **Shots 3-4 (aerial village
view) are new territory** — no village has been part of the locked
world-bible so far. Design it consistent with the established art style
(painterly watercolor, warm earthy palette) but expect this to need its
own small reference/lock pass, similar to how the lion+rabbit and jungle
references were locked before fable #1's story shots.

**Content-safety note:** Shot 4 must NOT depict impact or injury — cut to
stillness/empty air/silence the way fable #1 handled the lion's fall into
the well. This is a harder one to get right than prior fables' non-violence
notes since a mid-air fall is more inherently dramatic; lean on "the stick
falling, no tortoise visible, a few feathers or ripples of air" rather than
anything resembling a body in motion downward.

**Lessons carried over from fable #1's production** — apply to every
prompt for Shots 2-4:
- Explicit anti-split-screen/anti-panel language on every shot.
- Describe each animal's individual pose separately when multiple appear
  together (the two geese should not be mirrored duplicates of each other).
- Describe emotion/tension with specific physical cues rather than generic
  adjectives.

---

## Animation pass (planned, not yet generated)

Once Shots 2-4 are locked as stills, animate via Kling (`kling3_0`, sound
off), duration per shot matched to the actual voiceover's timing once
generated (not assumed in advance).
