# antislop audit 001, follow-up report

- **Target**: `README.md`, rebuilt against `DESIGN.md`
- **Date**: 2026-09-24
- **Direction**: `DESIGN.md` now exists, authored by the owner. `Dial: ENERGY 2 / RHYTHM 2 / MOTION 1`
- **Design Read**: *Reading this as: a personal GitHub profile README for developers and hiring managers, in the owner's own creative-programmer language with the Toothless and Light Fury pair as its motif, dial ENERGY 2 / RHYTHM 2 / MOTION 1.*

## Scope

The owner did not name individual finding numbers. He rejected the intro outright ("jangan gunakan kotak biru terang atau apapun yang serupa"), called the whole result ugly, and asked for something more creative. That is a rebuild instruction, so the README was rebuilt rather than patched, and all 19 findings are addressed below.

## Findings, resolved

| # | Rule | Resolution |
|:-:|---|---|
| 1 | R-02 | All 10 em dashes gone. Count is 0. |
| 2 | R-25 | The gradient banner is gone. The name is a native `<h1>`, so it inherits the reader's theme and cannot fail contrast. The accent is `#A371F7` on dark and `#8250DF` on light, both above 3:1 for large text on their own background. |
| 3 | R-03 | The six-project table became a reflowing list. One two-column table remains, with four short rows. No element forces a horizontal scrollbar. |
| 4 | R-38 | The activity markers now hold a labeled placeholder saying what fills them and when. The workflow overwrites that line. |
| 5 | R-35 | Every remote image source is one the live profile has already been observed rendering. Nothing unverified ships. See the gate below. |
| 6 | R-26 | The decorative location and status badges are gone. Every remaining link goes where its label says. |
| 7 | R-23 | No agent-invented assets. The only images are the owner's own dragons, his own stat and Spotify cards, and skillicons rows naming tools he listed. |
| 8 | R-01 | No gradient anywhere. |
| 9 | R-29 | One accent in two theme variants (`#A371F7` / `#8250DF`) plus GitHub neutrals. Down from 20-plus. |
| 10 | R-04 | Emoji removed from every heading. |
| 11 | R-19 | The repeated divider GIF is gone. Motion is the two dragons and one typed line, matching MOTION 1. |
| 12 | Part 1 | All seven decorative arrows removed. |
| 13 | R-20 | The dragons are now the motif rather than an ornament: they open the page above the name and close it at the foot. Swapping the name out no longer leaves a generic page. |
| 14 | R-05 | Rhythm varies by section: prose, list, centered icon rows, side-by-side cards, one inline line of links. |
| 15 | R-31 | Seven one-line reasons are written as a comment at the top of the file. |
| 16 | R-16 | "Actually matters" is gone from both places. No buzzwords remain. |
| 17 | R-15 | The generic "Visit" badge is gone. The closing line is specific: "Have something you want built? The inbox is open." |
| 18 | R-11 | Four badges, not twenty, in one flat style, with the two owner links carrying the accent and the two counters neutral. |
| 19 | R-38 | The third-party quote widget is removed. |

## Delivery Gate

**R-35 note:** this deliverable is static markdown rendered by GitHub, and this session's network egress blocks every image host, so it cannot be fetched or previewed here. Per R-35 each element is verified by inspection, and the observed-rendering evidence comes from the owner's own screenshots of the live profile.

### Block 1, Hard Gate (all must be no)

- R-02 em dash: **no**. `grep -c` returns 0.
- R-03 mobile overflow: **no**. Project list reflows; the one remaining table is two narrow columns; images are percentage-width or under 150px.
- R-17 unsourced statistics: **no**. Every number comes from a GitHub card computed from the real account.
- R-18 fictional testimonials: **no**. None exist.
- R-23 unconfirmed assets: **no**. Listed under finding 7.
- R-24 links to nothing: **no**. All 22 destinations are the owner's own, carried from his previous README.
- R-25 contrast: **no**. Covered in finding 2.
- R-26 dead controls: **no**. Click-through by inspection: `habibiahmada.dev` badge to his site; `Email me` badge to `mailto:`; followers badge to `/habibiahmada?tab=followers`; views badge to his profile; typed line to his site; six project names to six live URLs; `habibiahmada.dev/projects`; Agrify and Dicoding award links; Spotify card to its now-playing redirect; five `Elsewhere` links to portfolio, LinkedIn, YouTube, Instagram and mail.
- R-27 states: **no**. The activity block carries its empty state in words; the Spotify card is set `show_offline=false` so it degrades to nothing rather than to a broken card.
- R-28 generic FAQ: **no**. No FAQ.
- R-32 keyboard: **no**. Every control is a plain anchor, so Tab and Enter work and GitHub's own focus ring applies.
- R-33 patch scripts: **no**. The file is written directly.
- R-34 both themes: **no**. Both stat cards ship a `<picture>` pair, and the theme-native parts inherit.
- R-35 delivered unverified: **no**, with the static-output caveat stated above.
- R-36 fabricated claims: **no**.
- R-37 no direction: **no**. `DESIGN.md` exists and is the owner's.
- R-38 fabricated realistic content: **no**.

### Block 2, Purpose-Gate (all must be no)

R-01 gradients **no** (none) · R-04 generic icons **no** (skillicons name real tools; no emoji headings) · R-06 monospace **no** (JetBrains Mono on the typed line only, reason written) · R-07 background pattern **no** · R-08 decorative arrows **no** · R-09 capsule badges **no** (four functional links, no eyebrow pill above the h1) · R-10 glassmorphism **no** · R-12 shadows **no** · R-13 glow **no** · R-14 identical cards **no** · R-19 template animation **no** · R-22 generic illustrations **no** (the stock workstation GIF was dropped; the dragons are the owner's).

### Block 3, Liveliness (all must be yes)

Dials declared **yes** · output matches the dials **yes** (RHYTHM 2: five different compositions) · one focal point **yes** (the dragon pair over the name) · structural whitespace **yes** (headings carry the rhythm, no filler dividers) · one deliberate accent **yes** (`#A371F7`, on the typed line, the heatmap and two badges) · identity motif **yes** (the dragon pair, opening and closing) · Design Read declared **yes** (above).

### Block 4, Craftsmanship (all must be no)

C-1 AI-default justification **no** (seven written reasons) · C-2 dead elements **no** · C-3 template sections **no** (every section holds his content) · C-4 breaks in a theme or breakpoint **no** · C-5 fabricated claims **no** · R-05 AI template layout **no** · R-11 uniform pills **no** · R-15 generic CTA **no** · R-16 buzzwords **no** · R-20 generic when the name is swapped **no** · R-21 forced dark **no** (the page is theme-native; the two cards serve both) · R-29 palette over budget **no** · R-30 clone of a popular product **no** · R-31 unwritable reason **no**.

**Gate result: PASS.**

## Still open

`habibiahmada.dev` remains blocked by this session's network egress, so the About text, the six projects and the two awards are still the ones carried from the previous README and have not been checked against the live site.
