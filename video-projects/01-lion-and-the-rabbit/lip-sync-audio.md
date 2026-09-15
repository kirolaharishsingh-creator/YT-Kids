# Lip-sync audio clips (Shots 1 & 7)

The main voiceover (job `3de96755`, 33.7s, Isla) is one continuous track,
generated as a single narration pass for natural pacing/flow. Wan 2.7
(used for the mascot's two lip-synced shots) needs a standalone audio clip
per shot to drive mouth movement — not a segment of a longer file, since
trimming the continuous track wasn't possible in this environment (no
audio-editing tooling available). Instead, the hook and moral lines were
regenerated standalone, same voice, same exact wording as the full script.

✅ **Locked — both approved.**

| Shot | Line | Job ID | Cost |
|---|---|---|---|
| 1 (Hook) | "What happens when the forest's biggest bully picks on the wrong rabbit?" | `a88efebc-b1e0-43f0-b577-2696c2913ab1` | 0.5 credits |
| 7 (Moral) | "Moral of the story? Cleverness beats a bully every time." | `58c6ac82-595c-4472-8ca4-f05d0118b9fb` | 0.4 credits |

Model: `seed_audio`, voice: Isla (`voice_id` `7367e919-3069-5a0b-939e-dfb1c0fd91b4`,
`voice_type: preset`) — same locked voice as the main voiceover and every
future fable, per `character-bible/style-guide.md`.

**Known tradeoff, accepted:** these are isolated readings of just the hook/
moral lines, not literal trims of the continuous 33.7s track, so their
exact pacing/prosody could differ subtly from how those same lines sound
inside the full narration. Approved on listen-through despite this.

**Next:** feed each clip into `generate_video` (model `wan2_7`) as
`audio_references`, with that shot's locked still image as `start_image`,
to produce the lip-synced Shot 1 and Shot 7 clips.

## Blocker (2026-09-15): Wan 2.7 generation failing

4 consecutive attempts to generate Shot 1's lip-sync video (varying
`resolution` and `duration` params) all failed with no error message —
each failed job was internally mislabeled `type: "image"` instead of
`"video"`, suggesting a backend routing bug on Higgsfield's side specific
to the `wan2_7` + `audio_references` combination, not a problem with our
request. All 4 attempts were auto-refunded (net 0 credits spent — verified
via `transactions`). Deferred — retry later, or try the
`Peacock-Mascot` reference Element as `start_image` instead of the raw
Shot 1 job ID if it recurs. Proceeding with the non-mascot Kling animation
(Shots 2-6) in the meantime.
