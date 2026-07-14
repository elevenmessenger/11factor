# 🤖 AI-authorship markers — specification, version 1.0

This is the Marker Specification referenced by Condition 3 of the GAI
Licence (`LICENSE`): the convention for marking material written by
generative AI. It is versioned; the licence names the version that binds
it. The canonical copy travels with the Software as this file and is also
published at https://11factor.org/gai-licence. (A friendlier working-notes
form of the same convention lives in `CLAUDE.md § Who wrote this` — this
file is the one the licence points at.)

## The marker

- **🤖 marks AI-written material.** The marker is always **visible** in the
  rendered or source form — never hidden in a comment — and sits immediately
  before the heading, paragraph, or section it applies to (`# 🤖 Title`, or
  a leading `🤖 ` on a paragraph; in code, a `🤖` in the comment block that
  heads a file or section).
- **Plain-text fallback:** where the emoji cannot survive — ASCII-only
  pipelines, encodings, or tooling — the string `[AI]` in the same position
  is an equivalent marker. The canonical files themselves stay UTF-8 with
  the emoji form.
- **A marker on a heading cascades:** it covers that heading and everything
  beneath it — sub-headings, paragraphs, lists — down to the next marker of
  the same-or-higher level or a human-certified block. One 🤖 on a
  document's top heading marks the whole document.

## What the absence of a marker means

Nothing. Unmarked material is **ambiguous** — it could be human- or
AI-written. The absence of a marker is never a claim of human authorship;
only an affirmative statement is.

## Human certification

A person emoji (👨 / 👤 / 🧑 …) marks material written or vetted by a
person. In HTML or Markdown the person marker may be hidden in a comment
(`<!-- 👨 -->`) so it doesn't render; the 🤖 marker must never be hidden.

## Preserving and removing markers (what Condition 3 binds)

- Copies and Derivative Works in source form **preserve** the markers they
  carry on material the markers still accurately describe.
- A marker **may be removed** where a human has substantially rewritten the
  material it marks — the marker described the old text, not the new.
- New AI-written material in a Derivative Work **should** be marked the same
  way; what Condition 3 *requires* is narrower: AI-written material must not
  be affirmatively presented as human-written.
- **Compiled or minified artifacts** need not carry markers.

## Versioning

Changes to this specification bump its version number; the GAI Licence
binds the version it names, and the version history is published alongside
the licence's at https://11factor.org/gai-licence.
