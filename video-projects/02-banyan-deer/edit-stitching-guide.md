# Edit / Stitching Guide: The Banyan Deer's Offer

Everything needed to assemble the final video. All 7 clips are locked —
this is a pure assembly job, no more generation needed for the story
itself.

**Total runtime: 30 seconds** (7 clips, fixed duration plan — unlike
fable #1, shot durations here were set first and the voiceover is fit to
them during editing, not the other way around).

**Canvas: 1080×1920 (vertical 9:16)** — every clip is already this aspect
ratio, no reframing needed.

---

## Video track — clip sequence

Cut clips back-to-back in this exact order, no transitions (hard cuts,
matching the channel's established pacing):

| Order | Timecode | Shot | Source clip (video job ID) | Duration |
|---|---|---|---|---|
| 1 | 0:00–0:05 | 1 — Hook (mascot) | `6a35ec14-57c1-4bba-8243-7e8be5f48e61` *(reused from fable #1)* | 5s |
| 2 | 0:05–0:09 | 2 — Setup | `8d8e2eac-8fa9-45a8-b52a-c9f58638d1e0` | 4s |
| 3 | 0:09–0:13 | 3 — Turn (a) | `e4d7a06c-ef42-410b-98de-0c793fba9241` | 4s |
| 4 | 0:13–0:17 | 4 — Turn (b) | `755b9992-5098-4a50-8a6f-99b3cfaefb93` | 4s |
| 5 | 0:17–0:21 | 5 — Payoff (a) | `27d0b442-0706-40cf-a02e-35aff15bc038` | 4s |
| 6 | 0:21–0:25 | 6 — Payoff (b) | `ed7e4acd-9b4d-427c-b587-f7e1b22f1be6` | 4s |
| 7 | 0:25–0:30 | 7 — Moral (mascot) | `3abdf454-7684-460a-a2d2-7af777ae1fca` *(reused from fable #1)* | 5s |

Download each clip from its job (via Higgsfield's generation history) and
place in your editor in this order.

---

## Audio track 1 — Voiceover (not yet finalized)

**Status:** the script was trimmed (78 → ~40 words) but the voiceover
hasn't been regenerated to confirm its actual spoken duration — see
`scripts/banyan-deer.md`'s Length note. Since the 30s video timeline is
now fixed (unlike fable #1, where shots were sized to match an
already-generated voiceover), the voiceover needs to be **fit to this
30s timeline during editing** rather than dictating it:

- If the voiceover generates shorter than 30s: fine, leave brief natural
  pauses/breathing room between beats rather than stretching the audio
  unnaturally.
- If it generates longer than 30s: either trim pauses in the audio, speed
  it up slightly (small `speech_rate` adjustment on regeneration), or
  extend a shot's hold time by a fraction of a second — small overflow is
  easier to absorb here than in fable #1's case since each shot only
  needs to flex slightly, not by seconds.

**Approximate per-beat placement** (once generated), based on the trimmed
script's narration text:

| Beat | Shots | Approx. timecode | Narration |
|---|---|---|---|
| Hook | 1 | 0:00–0:05 | "Would you die to save a stranger?" |
| Setup | 2 | 0:05–0:09 | "The deer struck a deal: one sent to the king each day." |
| Turn | 3–4 | 0:09–0:17 | "When a mother-to-be was chosen, her leader refused to help. The Banyan Deer took her place." |
| Payoff | 5–6 | 0:17–0:25 | "The king couldn't kill the noblest deer in the forest." |
| Moral | 7 | 0:25–0:30 | "He spared every animal in the forest. Moral of the story? Mercy answered with mercy makes a real leader." |

**To do before final export:** generate the voiceover (Isla voice, same
as every prior fable), listen through, and adjust pacing/pauses in the
edit so it lines up with the beats above.

## Audio track 2 — Background music (pending)

**Status:** not yet finalized — same evergreen-music search as fable #1,
not yet locked (targeting a whimsical fairy-tale instrumental). Once
chosen, place under the entire video 0:00–0:30, ducked significantly
under the voiceover, with a short fade in/out at the very start/end.

## Audio track 3 — Animal/ambient SFX (pending)

**Status:** not yet sourced. Suggested placement once available:
- A soft **hoofbeat/rustle** around 0:13 (Shot 4, the moment the Banyan
  Deer steps forward) — reinforces his resolve
- A brief **sword-unsheathing or metallic shimmer** around 0:17 (Shot 5,
  the king's raised blade) — subtle, not violent-sounding
- Keep it sparse — 2 accents across 30s is plenty, same "don't overdo it"
  principle as fable #1's guide.

---

## On-screen text overlays

Per `character-bible/style-guide.md`'s standing on-screen-text rule:

| Text | Timing | Notes |
|---|---|---|
| "The Banyan Deer's Offer 🦌" | 0:00–0:05 (during Shot 1) | Same corner position/font as fable #1's title card |
| "Moral: A true leader gives before he takes." | Final ~2-3s (roughly 0:27–0:30, during Shot 7) | Same position/font as the title card |

Use the exact same font, size, and corner placement as fable #1's title
card — this is a fixed channel template now, applied consistently across
every fable, not decided per-video.

---

## Known limitations, carried over from production (for editing awareness)

- **Shot 3** has two accepted limitations: landmark bleed (a banyan tree
  and waterfall appear in the background despite the plain-clearing
  prompt) and understated pleading/dismissive body language. Not a
  reshoot — noted here in case the cut needs a slightly longer hold or a
  different trim point to compensate for the softer emotional read.
- **Shot 5**'s sword has a glowing motion-trail effect, slightly more
  visually prominent than intended, though no violence is depicted.
- **Shot 6** leans marginally more polished/digital-painting than the
  flatter storybook style elsewhere — subtle at normal viewing size.

None of these require redoing the shots; flagged here purely so editing
choices (cut timing, whether to add a vignette/color grade pass) can
account for them if it helps visual consistency in the final cut.

---

## Export settings

- Vertical 9:16, 1080×1920 minimum resolution
- Standard YouTube Shorts-safe export (H.264 MP4)
- Under 3 minutes total (trivially true at 30s) — qualifies for the
  Shorts shelf per `docs/monetization-and-growth.md`'s dual-strategy;
  post as an individual Short, later bundle into a periodic compilation
  alongside fable #1 once enough fables exist.
