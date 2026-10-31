# ReLEAF Booth Pitch Prep

Booth-floor prep dashboard for **GEMS Taiwan · ReLEAF**, iGEM 2026 Grand Jamboree —
Booth H-17, Biomanufacturing Village, Paris, 13–16 November 2026.

**Live:** https://timmy97-tw.github.io/releaf-booth-prep/

One self-contained `index.html`, no external requests, no build step. Same design
language as the [Paris dashboard](https://timmy97-tw.github.io/releaf-jamboree/).

## What is on it

| Section | What it does |
| --- | --- |
| **Open** | The 15-second open, word for word, broken into its four beats |
| **Playground** | Pick who is asking — eight audiences, each with what to lead with, what to have ready, and phrases you tick off as you land them |
| **Phrases** | The words to hit, in six groups. Tap for the sentence each belongs in; drill mode hides the phrases so you say them before you reveal them |
| **Results** | 37 numbers with where to point. Amber cards are the ones that cut against us — volunteer those |
| **Guard rails** | Do-not-claim list, the three pocket sentences, and the contradiction register: name it before a judge finds it |
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

Every phrase and number traces to a live wiki page or to the team's judging prep
record. The honesty rule the prep runs on is kept here too: no claim of a working
light switch, no validated field effect, no titre, and no price the pages agree on.

## Editing

Everything is in the script arrays near the bottom of `index.html`:

- `WHO` — the playground audiences
- `PHRASES` — the phrase groups
- `RES` — the results board (`[number, what it is, where, area, cuts-against-us]`)
- `CX` — the contradiction register
- `POOLS` — the randomizer roster

Commit to `main`; GitHub Pages serves it from the repository root.
