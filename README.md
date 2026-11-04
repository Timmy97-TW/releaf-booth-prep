# ReLEAF Booth Pitch Prep

Booth-floor prep dashboard for **GEMS Taiwan · ReLEAF**, iGEM 2026 Grand Jamboree —
Booth H-17, Biomanufacturing Village, Paris, 13–16 November 2026.

**Live:** https://timmy97-tw.github.io/releaf-booth-prep/

One self-contained `index.html`, no external requests, no build step. Same design
language as the [Paris dashboard](https://timmy97-tw.github.io/releaf-jamboree/).

## What is on it

| Section | What it does |
| --- | --- |
| **Everyone's pitch** | All 25 drafts from the team's [pitch doc](https://docs.google.com/document/d/1DX1fNK8tTVr0ZvPVkddWckGXLdTQNUaYQbmf-ut_m78/edit?tab=t.1bizq2cu3t6h), word for word (snapshot of the 4 Nov night update), with notes in the margin: good lines, wording to trim, claims to check, and Timmy's own doc comments. Who still has no pitch (computed from the roster), an alphabetical at-a-glance table and keyword highlights by topic |
| **The merged pitch** | One ~3-minute pitch built from the best lines, each line credited to the scripts it came from, plus a five-sentence short cut |
| **Flag it or say it** | A quiz on 119 real lines from the margins: say it at the booth, or flag it for checking. Score, streak, and a best streak kept on the device |
| **Who answers** | Name randomizer for rehearsal and for the floor |

## The randomizer

Three pools: **Students** (31, on by default), **Student Advisors** (4) and
**Instructors** (6), both off until you switch them on. Names come from the
[team page](https://2026.igem.wiki/gems-taiwan/team).

- Tap any name to sit that person out, tap again to bring them back.
- Add anyone missing with the box at the bottom, into whichever pool you choose.
- **No repeats** is on by default: everyone speaks once before anyone repeats.
- Draw one, two or three at a time.
- Added names and sit-outs are kept in that browser only (`localStorage`), and
  **Reset everything** clears them.

## Where the content comes from

The pitches are the students' own text. The margin notes check each claim against
the wiki and the team's judging prep: no claim of a working light switch (green
raised activity at one time point, n = 2), no validated plant rescue, and plating
results described as what they are, not as a 72-hour containment case.

## Editing

Everything is in the script arrays near the bottom of `index.html`:

- `PITCH` — each script: paragraphs `p`, verdict `v`, steal line `st`, fix `fx`,
  and margin notes `m` as `[exact quote, type, comment]` (type `g` good, `a` trim,
  `r` check, `d` Timmy's doc comment). A note attaches to the first paragraph
  containing its quote. A draft nobody signed carries `un:1` and a short `ud`
  description, which the "Still to write their pitch" box lists underneath.
- `FULL`, `SHORT` — the merged pitch, each line `[text, [source scripts]]`
- `KW` — keyword groups and their patterns
- `POOLS` — the randomizer roster

Commit to `main`; GitHub Pages serves it from the repository root.
