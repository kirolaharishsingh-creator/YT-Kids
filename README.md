# YT Kids — Indian Folk Fable Shorts

This repository is the production workspace for a YouTube Shorts channel telling
classic Indian folk and moral fables (Panchatantra / Akbar-Birbal / Tenali Raman
style) as 15–20 second AI-generated videos.

**Why this niche (see `docs/monetization-and-growth.md` for the full reasoning):**
- No religious-figure depiction risk — these are folk/moral tales (clever animals,
  kings, wise fools), not deities.
- Each fable already compresses naturally into a hook + twist + one-line moral —
  a near-perfect fit for a 15–20 second format.
- Hundreds of these stories are public domain, well documented, and reusable —
  so output volume isn't blocked on original writing.
- General/family-audience framing, not toddler-only — avoids the YouTube "Made for
  Kids" ad-revenue penalty as long as content stays clearly aimed at a broad
  audience rather than pre-schoolers specifically.

## Folder structure

```
docs/             Brand positioning, monetization & growth plan, production standards
character-bible/  Visual style guide + reference briefs for consistent AI generation
world-bible/      Locked recurring locations (the forest and its landmarks) for consistency
scripts/          Finished and in-progress video scripts (narration + scene beats)
research/         Source notes per fable — original story, variants, the moral
video-projects/   Per-video folders tying together idea, script, shot list, status
footage/          Raw and organized AI-generated video clips
assets/           Reusable assets — music, sound effects, intro/outro, fonts, logo
thumbnails/       Thumbnail source files and exported thumbnail images
exports/          Final rendered videos, ready to upload
references/       Source material for each fable (public-domain texts, citations)
```

## Workflow

Each video moves through these stages in order:

1. **Pick a fable** — Note it in `video-projects/<fable-name>/idea.md`, including
   which moral it teaches and why it fits the channel right now.
2. **Research** — Confirm the story's original text/variants in `research/` and
   `references/`. Keep the retelling faithful to a real source, not invented.
3. **Script** — Write the 15–20 second narration + visual beats in
   `scripts/<fable-name>.md`. Every beat must be achievable as a single AI-generated
   shot (see `character-bible/style-guide.md` for consistency rules).
4. **Shot list** — Break the script into individual AI generation prompts (image
   and/or video) inside the video's `video-projects/` folder.
5. **Generate** — Produce the visuals/voiceover using the approved style guide and
   character references, so every fable looks like it belongs to the same channel.
6. **Edit** — Assemble generated clips, voiceover, and assets (`assets/`) into the
   final 15–20 second cut.
7. **Thumbnail** — Design and export into `thumbnails/`.
8. **Final export** — Render into `exports/`, ready to upload.

See `docs/monetization-and-growth.md` for the earnings model, YouTube Partner
Program thresholds, and the posting cadence needed to reach them, and
`docs/brand-positioning.md` for naming, tone, and what to avoid.

## Conventions

- Use one consistent slug per fable across `scripts/`, `research/`, and
  `video-projects/` (e.g. `thirsty-crow`).
- Keep the top-level structure flat — organize *within* each folder by fable name
  as the series grows.
