# Shot List: The Blue Jackal

Each row = one AI generation. All prompts append the fixed style fragment
from `character-bible/style-guide.md`.

| # | Beat | Shot | Asset needed |
|---|------|------|--------------|
| 1 | Hook | Peacock mascot on branch, addressing camera, warm expression | ✅ **Reused from fable #1** — generic-talking clip `6a35ec14-57c1-4bba-8243-7e8be5f48e61`, no new generation. |
| 2 | Setup | Blue jackal freshly dyed, forest animals (deer, monkey, bird) gathered around, wide-eyed and awed | New generation |
| 3 | Turn | Blue jackal seated on a raised rock/mound like a throne, animals bowing/attending him | New generation |
| 4 | Payoff | Night scene: blue jackal howling along with distant ordinary jackals, nearby animals reacting with dawning realization | New generation |
| 5 | Moral | Peacock mascot again, same reference as shot 1 | ✅ **Reused from fable #1** — generic-talking clip `3abdf454-7684-460a-a2d2-7af777ae1fca`, no new generation. |

**Note:** this fable only needs 3 new story shots (2-4), one fewer than
fable #1/#2's 5, since the "Turn" and "Payoff" beats compress more
naturally into single images here (no second location/well-approach
transition needed).

**Voiceover:** one continuous narration track per `scripts/blue-jackal.md`,
same voice/TTS setting as every prior fable. Keep an eye on actual
generated duration against the ~18-20s target (see the "Length discipline"
note in the script) before locking the animation-duration plan below.

**Status:** not yet started. Before generating Shots 2-4, first generate
and lock a fable-specific character reference sheet (blue jackal + a
generic forest-animal "subject" or two), same process as fable #1's
`character-reference-prompt.md`.

**Location consistency:** all shots use the **`Neelvan-Forest`** Element
(id `e59c0df0-180e-4d97-9ca1-4ac2a550ef36`) — feed it in via the
`<<<e59c0df0-180e-4d97-9ca1-4ac2a550ef36>>>` placeholder syntax, same as
prior fables. Single forest-clearing location throughout, no second
location needed.

**Lessons carried over from fable #1's production** (see
`video-projects/01-lion-and-the-rabbit/shot-2-iteration-log.md` and
`shot-3-iteration-log.md`) — apply to every prompt for Shots 2-4:
- Explicit anti-split-screen/anti-panel language on every shot ("single
  continuous unbroken scene, one camera, one consistent depth of field, no
  split screen, no panel divide, no dividing lines").
- Describe each animal's individual pose separately when multiple animals
  of similar type appear together, to avoid mirrored/duplicate-looking
  poses.
- Describe emotion (awe, realization) with specific physical cues rather
  than generic adjectives, which tend to render flat/neutral otherwise.

---

## Animation pass (planned, not yet generated)

Once Shots 2-4 are locked as stills, animate via Kling (`kling3_0`, sound
off), same as fable #1's Shots 2-6 — duration per shot to be matched to
the actual voiceover's timing once generated, not assumed in advance
(this is exactly what fable #1's process got wrong initially, assuming a
uniform duration before checking the real voiceover length).
