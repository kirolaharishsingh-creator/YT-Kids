# Character reference iteration log: Deer + King

| # | Job ID | Issue | Verdict |
|---|---|---|---|
| 1 | `c18f5c52-a951-4092-8079-b9c2feb990cd` | Style mismatch — rendered as clean, glossy anime/JRPG-style digital illustration (smooth cel-shaded gradients, sparkle highlights) instead of the channel's painterly watercolor look. Also a stray pair of glasses appeared floating at the king's feet, likely bled in from the `Peacock-Mascot` reference (the mascot wears gold-rimmed reading glasses). Antlers rendered as stylized gold jewelry rather than natural antlers. | Rejected |
| 2 | `029638c5-7c31-463b-9d52-0c8ad180cd2d` | Fixed the style (matte painterly, no glossy anime look), fixed the antlers (natural), fixed the glasses (dropped the `Peacock-Mascot` reference entirely, kept only `Neelvan-Forest` for palette). New issue: baked-in text reading "Banyan Dear" (misspelled) appeared next to the deer. | Rejected (text defect only) |
| 3 | `73afd901-e3c5-4199-b296-91dda007dab8` | Text-removal edit of #2 ("remove text Banyan Dear. do not change anything else") — clean result, no text, style/antlers/no-glasses all held from #2. | **✅ Locked** |

## Root cause diagnosis

**Attempt 1's anime-style drift:** unclear exact cause, but the human
king character specifically drifted toward glossy digital/anime
rendering while the deer (animal) in the same image stayed reasonably
close to the intended painterly style. Suggests `seedream_v4_5` may have
a stronger default pull toward polished/anime rendering for human
figures than animal figures. Fix that worked: extremely explicit
anti-anime/anti-glossy language specifically targeting the human
character ("rendered with the same soft painterly linework... not
sharper or more polished than the deer").

**Attempt 1's floating glasses:** most likely bleed-through from the
`Peacock-Mascot` Element (which has gold-rimmed reading glasses as part
of its design) — feeding a character-style reference can pull literal
accessories from that reference, not just style. Fix: dropped the mascot
reference for this generation, relying on text description alone for
character design plus `Neelvan-Forest` for palette/lighting only.

**Attempt 2's stray text:** `seedream_v4_5` occasionally bakes in
readable (and here, misspelled) text/labels despite "no text" in the
prompt, similar to the general model behavior noted elsewhere in this
project. Fix that worked: a targeted follow-up edit generation
("remove text X, do not change anything else") rather than a full
regeneration — cheaper and preserves everything else that was already
correct, worth trying this approach first for future text-only defects
before redoing a whole generation from scratch.

## Takeaway for future fables

- Any fable introducing a **human character** should expect the same
  anime-drift risk and needs the same explicit "same painterly style as
  the animal, not more polished" language from the start, not as a fix
  after the fact.
- Consider **not** feeding the `Peacock-Mascot` Element into future
  character-reference generations unless the mascot itself appears in
  the shot — it's a source of unwanted accessory bleed-through, and
  `Neelvan-Forest` alone is enough for palette/lighting consistency.
- For text-only defects, try a targeted edit-in-place generation before
  a full regeneration.
