# 🤖 CLAUDE.md

Working notes for anyone (human or agent) changing this repo.

## What this is

11factor — *The Eleven Factors* — a serious parody of 12factor.net: principles
for building systems in a world where AI makes hard things easy and impossible
things hard. The factors are about the **intent behind systems**, not solely
technical practice. The site is a single static `index.html`: no build step, no
dependencies, no JavaScript. Keep it that way (factors VIII and IX apply to
this repo too).

## The one rule: AI authorship is always marked (🤖 / 👨)

This repo practices factor X on itself. Every piece of prose carries an
authorship marker so a reader — human or agent — can tell who wrote what, and
so a human can fence text off from AI rewriting.

- **🤖 — written by an LLM.** Always **visible**, immediately before the
  heading, paragraph, or section it applies to (`# 🤖 Title`, or a leading
  `🤖 ` on a paragraph). A 🤖 on a heading **cascades**: it marks that heading
  and everything beneath it, down to the next marker of the same-or-higher
  level or a human-certified block. One 🤖 on a document's top heading marks
  the whole document. On the website, the marker must render visibly on the
  page — never hide it in a comment.
- **No marker — ambiguous.** Could be either. Never *assume* AI authorship;
  when you genuinely don't know, leave it unmarked.
- **A person emoji (👨 / 👤 / 🧑 …) — certified human, off-limits.** The text
  was written or vetted by a person. **An LLM must not rewrite, rephrase,
  condense, or delete it.** You may add new 🤖 prose nearby, but the human's
  words are fixed. In HTML/Markdown the person marker may hide in a comment
  (`<!-- 👨 -->`) so it doesn't render; the 🤖 marker must **never** be hidden.

Transitions:

- An LLM writing new prose marks it 🤖.
- An LLM that substantially rewrites *unmarked* prose makes it 🤖.
- A human rewriting 🤖 text **removes the 🤖** (back to ambiguous), or adds
  their person marker to certify and lock it.
- An LLM that reaches a person-marked block hands off — leave it exactly as is.

Baseline: **everything in this repo was AI-written unless a block carries a
person marker.** Every Markdown file is stamped 🤖 at its top; the website
discloses it in its header and footer.

## Conventions

- **One page, zero dependencies.** No frameworks, no fonts fetched from
  anywhere, no analytics, no JavaScript unless a factor literally cannot be
  expressed without it (it can).
- **The Eleven mark is canonical.** `icon-{180,192,512}.png` are copies of the
  Eleven Messenger app icon (purple tile, white double-slash "11"). Reference
  these; never hand-roll a substitute glyph.
- The site supports light and dark via `prefers-color-scheme` — keep both
  working when touching styles.
- Deployed via GitHub Pages from `main` (root). Pushing to `main` publishes.
