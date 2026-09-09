# valerio-site — context for Claude Code

Valerio's personal "about me" landing page — bio, links to LinkedIn, email,
the "Worth Knowing" Substack, and the Alpha Intelligence portfolio site (see
the separate `alpha-intelligence` repo/project, which has its own CLAUDE.md
and much higher-stakes rules since it publishes real financial figures).

This site, by contrast, is low-stakes: a personal bio page. No live data, no
financial numbers, no backend. Normal care applies, not the extra
verification rituals `alpha-intelligence` needs.

## What's in the repo

- `index.html` — the entire site. One file: inline `<style>` in the `<head>`,
  content in `<body>`, one inline `<script>` for a decorative cursor
  "footprint trail" effect (only runs when `(hover: hover) and (pointer:
  fine)` matches and the user hasn't set `prefers-reduced-motion`).
- `index (1).html` — a stray duplicate from an early "Add files via upload"
  commit. It's an older, simpler draft (no footprint effect, no meta/OG
  tags, different `--paper` color). **Not live** — Vercel serves `index.html`
  at the root; this file has no route pointing to it. Don't edit it thinking
  it's the live page. Worth deleting in a dedicated cleanup, but confirm with
  Valerio first since it's a same-situation duplicate filename typo, not
  obviously safe to assume is garbage without asking.
- No `package.json`, no `vercel.json`, no build step. Vercel deploys this as
  a zero-config static site — editing `index.html` and pushing is the whole
  workflow.

## Design system — shared with alpha-intelligence

Same color palette and font as the `alpha-intelligence` portfolio site,
deliberately, since both are Valerio's public-facing pages:

- `--paper: #F7F1E3` (background), `--ink: #33322E` (text),
  `--muted: #8F8A7C`, `--accent: #6E8259` (sage green), `--hairline: #E6E1D4`
- Font: Raleway (Google Fonts), weights 300/400/500/600

If Valerio asks for a visual tweak on one site "to match the other," check
`alpha-intelligence/style.css` (or its `index.html`) for the current values
rather than guessing — the two have drifted before (e.g. `index (1).html`'s
stale `--paper: #FAF7F1` vs. the live `#F7F1E3`).

## Content notes

- Bio text, job/internship mentions, and link list are all real biographical
  facts (school, internship, newsletter, portfolio). Don't invent or embellish
  — if Valerio asks to add something like a new internship or credential,
  take the wording as given rather than expanding on it.
- The `mailto:` link and social links are real — treat changes to these as
  real contact info, not placeholder content.

## Before making changes

- Read the actual current `index.html` first — don't assume state from
  memory of past conversations.
- This is a public repo and a live personal site — anything pushed to `main`
  goes live via Vercel immediately, so short, reviewable commits are better
  than large rewrites.
