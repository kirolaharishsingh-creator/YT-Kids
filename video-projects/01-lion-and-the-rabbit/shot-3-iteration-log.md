# Shot 3 iteration log

| # | Job ID | Issue | Verdict |
|---|---|---|---|
| 1 | `4345b810-04b6-4a19-b9e7-feb40b424d44` | Background bled in the ancient well + an unplanned waterfall (not part of the locked world-bible) instead of matching Shot 2's plain clearing | Rejected |
| 2 | `b202d623-e1e4-4d80-9a83-6ac9042a844a` | Fixed the background, but produced a literal **split-screen**: a vertical white line bisecting the frame, lion on the left half, rabbit on the right half, lion's face itself cut in two at the seam | Rejected |
| 3 | `0c06c1ae-3213-4695-a4a7-25e67647ddd0` | Fixed both issues | **✅ Locked** |

## Root cause diagnosis

**Attempt 1's landmark bleed:** same multi-panel jungle reference sheet
issue documented in `shot-2-iteration-log.md` — fixed the same way, by
explicitly excluding named landmarks not wanted in this shot.

**Attempt 2's split-screen — a different root cause from Shot 2's seam.**
The `Lion-Rabbit-Fable1` element *is itself* a two-character reference
sheet — lion on the left, rabbit on the right, divided on a plain
background (see `character-reference-prompt.md`). Any shot whose own
composition is also "lion on one side, rabbit on the other" (i.e. exactly
this shot) gives the model a near-identical layout to copy from the
reference image itself, including its literal dividing line — text
instructions alone ("no split-screen") weren't strong enough to override
what the reference image visually showed. Shot 2 never hit this because it
had a whole group of animals, not a mirrored two-character pair, so the
reference's own layout was never a close match.

**Fix that worked:** explicit instruction that reference images inform
character design/style/colour ONLY, never composition or framing, plus
describing the two characters at different depths/angles in the same
integrated space rather than as a facing pair — broke the pull toward
recreating the reference sheet's layout.

**Takeaway for future shots:** any shot with *exactly* the lion + rabbit
and no other characters is at risk of this same split-screen pull from the
`Lion-Rabbit-Fable1` reference. Carry forward the "reference for style
only, not composition, characters at different depths not mirrored"
language whenever a shot is just the two of them (this applies to Shots
4-6 as well).
