# Shot List: The Banyan Deer's Offer

Each row = one AI generation. All prompts append the fixed style fragment
from `character-bible/style-guide.md`.

| # | Beat | Shot | Asset needed |
|---|------|------|--------------|
| 1 | Hook | Peacock mascot on branch, addressing camera, warm expression | Reuse mascot-peacock-final.png as image_references |
| 2 | Setup | Wide: two deer herds in a forest clearing, king's hunting party approaching in the distance, golden Banyan Deer standing apart | New generation |
| 3 | Turn (a) | Pregnant doe pleading before the Branch Deer's leader, who turns away | New generation |
| 4 | Turn (b) | Doe approaching the golden Banyan Deer instead; he steps forward | New generation |
| 5 | Payoff (a) | King, blade raised, frozen at the sight of the golden deer kneeling calmly before him | New generation |
| 6 | Payoff (b) | Close on the king's expression shifting from confusion to awe | New generation |
| 7 | Moral | Peacock mascot again, same reference as shot 1 | Reuse mascot-peacock-final.png as image_references |

**Voiceover:** one continuous narration track per `scripts/banyan-deer.md`,
same voice/TTS setting as fable #1.

**Status:** mascot locked and reference image in repo
(`character-bible/mascot-peacock-final.png`) — ready to generate this
fable's remaining shots.

**Location consistency:** Shots 2–6 use the Forest Clearing and (implicitly,
where the deer herds gather near it) the Great Banyan Tree landmarks from
`world-bible/`. Once `neelvan-location-sheet.png` is generated and locked,
feed the relevant panel(s) in as `image_references` on these shots so this
fable's forest matches fable #1's and every future one.
