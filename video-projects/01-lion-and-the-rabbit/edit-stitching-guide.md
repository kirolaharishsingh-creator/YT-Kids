# Edit / Stitching Guide: The Lion and the Rabbit

Everything needed to assemble the final video in any video editor (Premiere,
CapCut, DaVinci Resolve, etc.). All source clips are locked — this is a pure
assembly job, no more generation needed for the story itself.

**Total runtime: ~34s** (7 clips) — matches the 33.7s voiceover with ~0.3s
of slack to trim, ideally spread thinly across a couple of clips rather than
cut from one place, so no single beat feels rushed.

**Canvas: 1080×1920 (vertical 9:16)** — every clip is already this aspect
ratio, no reframing needed.

---

## Video track — clip sequence

Cut clips back-to-back in this exact order, no transitions between them
(hard cuts — matches the fairy-tale-book "page turn" pacing already built
into the pausing/beat structure):

| Order | Timecode | Shot | Source clip (video job ID) | Duration |
|---|---|---|---|---|
| 1 | 0:00–0:05 | 1 — Hook (mascot) | `6a35ec14-57c1-4bba-8243-7e8be5f48e61` | 5s |
| 2 | 0:05–0:11 | 2 — Setup | `9c1ca421-1493-4c03-9858-ccfdf7900328` | 6s |
| 3 | 0:11–0:17 | 3 — Trick (a) | `cf8c319d-16d7-465b-b464-c16435ad89f5` | 6s |
| 4 | 0:17–0:21 | 4 — Trick (b) | `26cff6df-ac7f-4a9f-8451-c127a2e74efc` | 4s |
| 5 | 0:21–0:25 | 5 — Payoff (a) | `b506c4b9-305e-4cfb-b4ea-281688786d0c` | 4s |
| 6 | 0:25–0:29 | 6 — Payoff (b) | `cff6aa5f-f39a-4573-a692-54746f204e0a` | 4s |
| 7 | 0:29–0:34 | 7 — Moral (mascot) | `3abdf454-7684-460a-a2d2-7af777ae1fca` | 5s |

Download each clip from its job (via Higgsfield's generation history, or
the result URLs already shared in this project's conversation history) and
place in your editor in this order.

---

## Audio track 1 — Voiceover (primary)

**Source:** job `3de96755-0356-4636-999c-dc82497a5fa1` (Isla voice, 33.7s)
— one continuous file, place starting at **0:00**, running under the whole
video. No splitting needed; the clip durations above were sized to match
this track's natural pacing, not the other way around.

Full text, for reference while trimming/aligning:
> "What happens when the forest's biggest bully picks on the wrong rabbit?
> Every animal had to send the lion food, or he'd hunt them all himself.
> Today, it was the rabbit's turn. Forgive me, said the rabbit. Another
> lion in this forest tried to stop me, and said he rules here now. The
> lion roared. Show me. The lion saw his rival, and leapt in to fight him.
> Moral of the story? Cleverness beats a bully every time."

If the voiceover runs ~0.3s shorter than the 34s of video, either trim that
sliver evenly off the end of Shot 6 (a static-ish ripple shot, least
noticeable place to lose a fraction of a second) or let Shot 7 hold half a
beat longer before the moral line starts — don't force a hard sync to the
frame, a little breathing room reads fine.

## Audio track 2 — Background music (pending)

**Status:** not yet finalized — see `docs/` for the evergreen-music search
in progress (targeting a Pixabay-sourced whimsical fairy-tale instrumental,
not yet locked). Once chosen:
- Place under the entire video, 0:00–0:34, looped/trimmed to fit
- **Duck the volume significantly under the voiceover** — the narration
  must stay clearly the dominant sound; music should be felt, not
  competing for attention
- No hard in/out cut — fade in over the first ~0.5s and fade out over the
  last ~0.5s so it doesn't clip abruptly

## Audio track 3 — Animal SFX (pending)

**Status:** not yet finalized — see the animal-SFX-pack discussion for
sourcing (cartoon/cute-toned lion roar, rabbit sound, etc.). Suggested
placement once sourced:
- A soft **lion roar** (playful/cartoon, not scary) around **0:17** (Shot 4,
  "The lion roared. Show me.") — sits right under the VO line naming it
- A **splash** sound around **0:25** (start of Shot 6, the well
  ripples/aftermath) — reinforces the implied jump without showing it
- Keep every SFX subtle and brief — these are accents under the narration
  and music, not competing elements. Skip anything for Shots 1-3, 5, 7 —
  adding SFX to every single beat gets busy fast for an 18-34s video.

---

## On-screen text overlays

Per `character-bible/style-guide.md`'s standing on-screen-text rule (title
early, moral repeated near the end):

| Text | Timing | Notes |
|---|---|---|
| "The Lion & the Rabbit 🐰🦁" | 0:00–0:05 (during Shot 1) | Small, consistent corner position (top or bottom — pick one and reuse every fable) |
| "Moral: Wit beats strength." | Final ~2-3s (roughly 0:31–0:34, during Shot 7) | Same position/font as the title card, for visual consistency |

Use the same font, size, and corner placement across every future fable —
this is meant to become a fixed channel template, not a per-video choice.

---

## Export settings

- Vertical 9:16, 1080×1920 minimum resolution
- Standard YouTube Shorts-safe export (H.264 MP4, matches every clip's
  native format)
- Keep the file under 3 minutes total (trivially true here at ~34s) so it
  still qualifies for the Shorts shelf per `docs/monetization-and-growth.md`'s
  dual-strategy — this video should be posted as an individual Short, and
  later bundled into a periodic multi-fable compilation once enough fables
  exist.
