# World Bible — The Forest Setting

Purpose: just like the mascot needs ONE locked character reference reused in
every video, the jungle where these stories happen needs ONE locked set of
location references — otherwise every fable's forest looks like a different
forest, and the channel never builds a recognizable "world."

## Name

**Working name: Neelvan** ("blue-forest" — Hindi/Sanskrit रूट, नीलवन) — evokes
the jewel-toned palette already locked into the mascot and overall style.
Easy to rename; used in scripts as e.g. "Deep in Neelvan, a lion ruled the
forest..." Change it if you want something else — it's a placeholder, not
locked the way the visual design is.

## What it is

A lush, painterly, Himalayan-foothills-inspired jungle — the same setting
every animal fable happens in, distinguished by a handful of **recurring
landmarks** that reappear across different videos, tying the whole channel
together visually. Not every fable uses every landmark — pick whichever
fits the story, but when a location repeats (e.g. "a forest clearing," "an
old well"), it should be *the same* clearing, *the same* well, not a new
one invented each time.

## Recurring landmarks

- **The Ancient Well** — a moss-covered stone well in a quiet clearing.
  Already used in fable #1 (Lion and the Rabbit).
- **The Great Banyan Tree** — an enormous, ancient banyan tree at the heart
  of the forest, aerial roots hanging like curtains, often where animals
  gather or take shelter. Ties naturally to fable #2 (Banyan Deer).
- **The Forest Clearing** — the general gathering spot / "town square" for
  animal councils and confrontations (used in fable #1's setup).
- **The Winding River** — a clear stream cutting through the forest, useful
  for future water-related fables (fish, crane, crocodile tales from the
  backlog).
- **Distant Mountains** — a consistent misty, snow-capped mountain backdrop
  visible from open areas, establishing the Himalayan-foothills feel.

Additional landmarks (a palace courtyard for the Akbar-Birbal/Tenali Raman
fables, a village for Gopal Bhar) are a separate "world" from the animal
forest and would get their own locked reference sheet later, using this same
method — not needed yet since the current backlog priority is animal fables.

## Style (inherits from `character-bible/style-guide.md`)

Same classic fairy tale book illustration style, same warm earthy palette
(terracotta, marigold yellow, leaf green, deep indigo shadows), same soft
painterly rendering — the forest and the mascot need to look like they
belong to the same show.

## How to use the locked reference

Whenever a fable's scene needs one of these landmarks, feed the locked
reference in as an `image_references` input on that shot's generation — same
technique as the mascot reference, applied to places instead of characters.
Three ways, in order of preference:
- **By Higgsfield Element (preferred):** search/select **`Neelvan-Forest`**
  (id `e59c0df0-180e-4d97-9ca1-4ac2a550ef36`, category: environment) in
  Higgsfield's element picker. Named and thumbnailed, so there's no risk of
  grabbing the wrong reference by mistake (a raw job ID mix-up already
  happened once with the mascot reference — this is exactly why Elements
  exist).
- **By Higgsfield job ID:** pass `e397fad4-d452-47c8-a77d-ae5050fbf224` as
  the media value with role `image_references`.
- **By file** (once uploaded to the repo): `world-bible/neelvan-location-sheet.png`.

## Status

✅ **Locked.** Generation `e397fad4-d452-47c8-a77d-ae5050fbf224`
(`seedream_v4_5`) — the four-panel sheet with the well + distant castle, the
great banyan tree, the meadow with mountains, and the river with waterfalls,
all with the warm lantern/firefly magical treatment. Reviewed and approved.
See `forest-location-sheet-prompt.md` for the full generation record.

⬜ Image file not yet in the repo — usable today via job ID reference above
regardless; upload `neelvan-location-sheet.png` here when convenient for a
visual record, not blocking.