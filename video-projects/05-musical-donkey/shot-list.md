# Shot List: The Musical Donkey

Each row = one AI generation. All prompts append the fixed style fragment
from `character-bible/style-guide.md`.

| # | Beat | Shot | Asset needed |
|---|------|------|--------------|
| 1 | Hook | Peacock mascot on branch, addressing camera, warm expression | ✅ **Reused from fable #1** — generic-talking clip `6a35ec14-57c1-4bba-8243-7e8be5f48e61`, no new generation. |
| 2 | Setup | Donkey and jackal in a moonlit vegetable field at night, donkey lifting head toward the moon, delighted | New generation |
| 3 | Turn | Jackal gesturing urgently for quiet; donkey braying mid-performance, eyes closed | New generation |
| 4 | Payoff | Farmhouse lights on, farmers with sticks rushing in the background; cut to donkey trudging off with a wooden mortar around his neck, no beating shown | New generation |
| 5 | Moral | Peacock mascot again, same reference as shot 1 | ✅ **Reused from fable #1** — generic-talking clip `3abdf454-7684-460a-a2d2-7af777ae1fca`, no new generation. |

**Voiceover:** one continuous narration track per `scripts/musical-donkey.md`,
same voice/TTS setting as every prior fable. Confirm actual generated
duration against the ~18-20s target before locking animation durations.

**Status:** not yet started. Before generating Shots 2-4, first generate
and lock a fable-specific character reference sheet (donkey + jackal), same
process as fable #1's `character-reference-prompt.md`.

**Location consistency:** a moonlit farm/vegetable field at night — new
territory, not yet part of the locked world-bible (same situation as
fable #4's village). Design consistent with the established art style
(painterly watercolor, warm earthy palette, though this one leans into
night/moonlight rather than daytime) but expect this to need its own
small reference/lock pass.

**Content-safety note:** Shot 4 must NOT depict the beating. Cut from
"farmers rushing in" directly to the aftermath (donkey with the mortar
around his neck, dejected) — same non-graphic treatment established across
prior fables.

**Lessons carried over from fable #1's production** — apply to every
prompt for Shots 2-4:
- Explicit anti-split-screen/anti-panel language on every shot.
- Describe each character's individual pose/expression distinctly rather
  than generically.
- Describe emotion/tension with specific physical cues rather than generic
  adjectives.

---

## Animation pass (planned, not yet generated)

Once Shots 2-4 are locked as stills, animate via Kling (`kling3_0`, sound
off), duration per shot matched to the actual voiceover's timing once
generated (not assumed in advance).
