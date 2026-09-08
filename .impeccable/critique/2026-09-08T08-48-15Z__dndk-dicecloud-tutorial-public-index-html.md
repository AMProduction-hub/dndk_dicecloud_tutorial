---
target: dndk_dicecloud_tutorial index page
total_score: 14
p0_count: 3
p1_count: 2
timestamp: 2026-09-08T08-48-15Z
slug: dndk-dicecloud-tutorial-public-index-html
---
# Design Critique: DnD-K DiceCloud Tutorial (index page)

Method: dual-agent (A: design review · B: detector + static evidence)

## Design Health Score — Nielsen Heuristics (A scores /10 raw, normalized to 0-4)

| # | Heuristic | Score | Key Issue |
|---|-----------|-------|-----------|
| 1 | Visibility of System Status | 1 | TOC scroll-spy targets height-0 headings inside collapsed callouts; no step progress |
| 2 | Match System / Real World | 2 | English chrome (Search, TOC, "4 min read") for Indonesian audience; note/pencil icon on chapters |
| 3 | User Control and Freedom | 1 | No expand-all, no back-to-top, TOC jumps broken by collapse |
| 4 | Consistency and Standards | 1 | Three numbering systems (chapters 1-2, steps 1-7, class types 1-3); mixed image syntax/alts |
| 5 | Error Prevention | 2 | Critical "don't subscribe 5e2014" warning buried mid-paragraph |
| 6 | Recognition Rather Than Recall | 1 | Entire tutorial hidden behind two collapsed boxes; chapters not headings |
| 7 | Flexibility and Efficiency | 1 | No working deep links into collapsed content; search lands on hidden text |
| 8 | Aesthetic and Minimalist Design | 1 | Empty Explorer, one-node Graph, KaTeX CSS w/o math; content hidden while chrome shouts |
| 9 | Error Recovery | 2 | Broken TOC jump is an unrecoverable dead-end; users think site glitched |
| 10 | Help and Documentation | 2 | No scope/prereqs/time framing; "4 min read" for 30+ screenshots is a lie |
| **Total** | | **14/40** | **Poor — major UX overhaul required** |

## Anti-Patterns Verdict

**LLM assessment**: Not AI slop — template slop. Site is branded "Quartz 5", page title is literally `_index`, footer links to Quartz's own GitHub/Discord, default fonts/palette, empty custom.scss. Looks like a half-configured wiki, not DnD-K's tutorial.

**Deterministic scan**: 0 findings (exit 0) on both index.html and 404.html. The detector targets app-UI slop patterns; this page's failures are structural/navigational, not decorative. Clean scan is real, not skipped.

**Browser visualization**: Skipped — no Playwright/Puppeteer available in environment.

## Overall Impression

Content is fine; the restructure hid 100% of the tutorial behind two collapsed note-boxes while every navigation system on the page points at invisible content. The TOC lists steps inside a closed box — clicking "3. Species" scrolls to a zero-height heading and shows nothing. On mobile (where the TOC is hidden) there is zero navigation. Biggest opportunity: make the steps real, visible structure and strip the dead chrome.

## What's Working

1. The class-type explanations (Martial/Caster/Half-Caster) are genuinely good teaching — dense but the page's best moment.
2. Two-chapter grouping was a sound instinct; the decision point of "account vs character" is the right split.
3. Strong finish: the sharing step gives a concrete payoff; journey ends better than it begins.

## Priority Issues

- **[P0] TOC is a trap**: TOC entries point to height-0 headings inside collapsed callouts; clicking scrolls to nothing. Also callout fold is a div with no button/ARIA/keyboard semantics. Fix: make chapters/steps real headings (always visible) or split into pages; collapse nothing by default.
- **[P0] Page identity is `_index` / "Quartz 5"**: title tag, og:title, article-title all say `_index`; link previews in WhatsApp/Discord say "_index — Quartz 5". Fix: frontmatter title, pageTitle in quartz.config.yaml, replace footer links, locale id-ID.
- **[P0] Two linked screenshots 404**: `screenshot-2026-09-07-225221-2.png` and `screenshot-2026-09-07-225957-6.png` referenced but missing in public/ (unsuffixed versions exist). Broken images in production. Fix: re-point or re-export.
- **[P1] Mobile has zero navigation + 3.8MB eager images**: right sidebar hidden on mobile, Explorer empty; 32 PNGs, no loading="lazy", width="auto" height="auto" (invalid, CLS). Fix: lazy-load, real dimensions, visible step headings as the mobile nav.
- **[P1] Dead chrome crowds out content**: empty Explorer, one-node Graph View, KaTeX assets with no math, Reader mode, footer links to Quartz's Discord. Fix: disable graph/explorer/backlinks/latex for a single-page site.
- **[P2] Three numbering systems**: chapters 1-2, steps 1-7, class types 1-3. Fix: one flat "Langkah 1..N" flow, chapters as unnumbered phase labels.
- **[P2] Critical warning buried**: "jangan campur 5e2014/5e2024" is a mid-sentence clause. Fix: own uncollapsed [!warning] callout at the subscribe step.
- **[P3] A11y**: no skip-link, no main/nav landmarks, h1->h3 skip, duplicate h1, filename placeholder alts, collapsed content stays in a11y tree.

## Persona Red Flags

**Jordan (first-timer, desktop)**: biggest text on page is `_index` (assumes broken link); reads collapsed note-boxes as side-notes (pencil icon trains this); clicks "3. Species" in TOC, page scrolls to nothing, concludes site is broken — most damaging interaction; never finds the 14px chevron; fold div never receives keyboard focus.

**Casey (mobile, one hand, 4G)**: TOC hidden on mobile = zero navigation; hamburger opens empty Explorer; expanding chapter 2 starts 32 full-res desktop screenshots (3.8MB, no lazy) fighting for bandwidth; desktop-UI screenshots unreadable at phone width, no tap-to-zoom; light-mode screenshots strobe against dark mode; English chrome adds "am I on the right site?" every visit.

## Minor Observations

- hard-line-breaks fuses text+image into single <p> blocks with <br/> — kills CSS step spacing
- Screenshot variants loose at vault root, not in an assets folder
- Typos: "Dungeon's & Dragon's", menunjukan/ditunjukan, English "content" mid-sentence
- analytics: plausible with no domain configured
- Collapse animation 0.1s — 30-image chapter jumps, doesn't unfold
- Collapsed callout content remains in accessibility tree (height:0 != hidden) — screen readers get a different page than sighted users

## Questions to Consider

1. TOC promises steps 1-7 while layout hides them in a closed box — which of the two systems (callout chapters vs heading TOC) are you willing to delete?
2. What did hiding the entire tutorial buy you? What evidence says a beginner clicks a 14px chevron?
3. When does DnD-K's identity replace the template's — and what is this page's identity right now?
