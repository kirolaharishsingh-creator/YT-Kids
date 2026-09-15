# Shot 2 iteration log

Kept for reference — 5 generations were needed to land Shot 2, each fixing
one issue while another regressed. Useful context for future shots/fables
that hit the same failure modes.

| # | Job ID | Seam? | Lion dominant? | Animals fearful? | Mirrored poses? | Verdict |
|---|---|---|---|---|---|---|
| 1 | (original, pre-log) | ❌ visible white line | ❌ sidelined by circle of animals | — | — | Rejected |
| 2 | `1031b04b-a63f-4733-be3b-2355b5d9198d` | ✅ fixed | ✅ fixed | ❌ calm/grazing, not afraid | ❌ duplicate mirrored pairs | Rejected |
| 3 | `6beaf4b2-9d01-43b1-87a0-f54cd7edef28` | ❌ seam came back, worse (literal two-panel split — giant banyan tree vs. misty path, joined by a visible vertical line) | ✅ | ✅ monkeys/birds read startled | ~partial improvement | Rejected |
| 4 | `2325a7b2-aca4-4762-a5b3-593cf372e051` | ✅ fixed again | ✅ | ❌ deer grazing-like, monkeys distracted by birds not the lion | ❌ deer mirrored, monkeys mirrored | Rejected |
| 5 | `ac8e275e-9005-4659-84f5-67688edfb0af` | ✅ | ✅ | ✅ deer crouched/tail tucked, monkey hunched/self-hugging, birds varied startled poses | ✅ (model rendered fewer animals — 1 deer + 1 monkey instead of 2 each — which incidentally killed the mirroring) | **✅ Locked** |

## Root cause diagnosis

**The seam:** `Neelvan-Forest` (world-bible jungle reference) is a multi-panel
location sheet (banyan tree / ancient well / forest clearing / river). When
fed in as an `image_references` input, the model sometimes pulls two
distinct panels into one generated image instead of blending them into a
single scene, leaving a visible seam/dividing line at the panel boundary.
Fix that worked: explicit prompt language forbidding split-screen/diptych/
multi-panel composition and demanding "one continuous camera view, one
consistent depth of field."

**Animals not reading as dominated/afraid:** generic words like "bowing
nervously" or "cowering" were not enough — the model defaulted to calm/
grazing poses. Fix that worked: describing each animal's specific physical
fear cues individually (ears pinned back, tail tucked, arms wrapped around
itself, crouched flat, wings half-raised to flee) rather than one group
adjective.

**Mirrored/duplicate poses:** feeding two of the same species (2 deer, 2
monkeys) tends to make the model render them as a mirrored pair. Giving
each individual instance its own distinct described pose ("on the left,
one deer... further left, a second deer...") was the fix attempted in #5,
though the model also resolved it by simply rendering fewer duplicate
animals than requested.

**Takeaway for Shots 3-6 and future fables:** when a shot needs multiple
animals of the same species, describe each one's pose individually rather
than as a group, and keep the "single continuous scene, no panels/seams"
language in every prompt that references the multi-panel jungle sheet.
