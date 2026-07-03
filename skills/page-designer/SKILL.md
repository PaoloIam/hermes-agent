---
name: page-designer
description: |
  Produce polished single-file HTML: listing one-pagers, Brevo email
  layouts, open-house flyers, simple lead-capture pages. Ported from
  gstack's /design-html and /design-shotgun concepts. Load when Paolo asks
  for a page, flyer, email design, or anything visual.
version: 1.0.0
platforms: [linux, macos, windows]
metadata:
  hermes:
    tags: [design, html, email, marketing, real-estate]
    category: real-estate
    related_skills: [draft-review, buyer-matchmaker]
---

# Page Designer

Real-estate marketing lives and dies on presentation. You produce
single-file HTML that looks professionally designed, not
developer-designed.

## Model routing

Paolo's saved preference: design/UX work runs on the GLM lane when it is
configured. Honor it when the session/model routing allows; the output
rules below apply regardless of which model renders them.

## The shotgun rule (from gstack /design-shotgun)

For anything Paolo will show to clients, produce **three visually distinct
variants** in one pass — e.g. editorial-serif, modern-minimal, bold-color —
and tell him to pick. One variant only when he asks for "quick".

## Output rules

- **One self-contained file** per variant: inline CSS, no external
  scripts, no CDN fonts (system font stacks). Save under
  `workspace/design/<project>/` and tell Paolo the exact paths.
- **Email layouts (Brevo)**: table-based structure, inline styles, 600px
  max width, alt text on every image slot, works with images blocked.
  Modern CSS that breaks in email clients is a defect, not a style choice.
- **Pages/flyers**: mobile-first, print-clean for flyers (no dark full-bleed
  backgrounds that murder toner), one clear call-to-action.
- **Placeholders, never fake facts**: photos as clearly-labeled slots,
  prices/addresses only from real data. `[PHOTO: living room]` is
  professional; an invented price is a liability.
- Fair-housing basics apply to marketing copy — draft-review's compliance
  check runs on all copy inside the design.

## Iteration

Paolo gives feedback in civilian words ("make it feel more expensive").
Translate: more whitespace, fewer colors, larger serif display type,
smaller body text, no exclamation marks. Never reply with CSS jargon —
show the revised file.

## Self-improvement loop

1. Append one dated line to `memories/skill-learnings/page-designer.md`:
   what was built, which variant Paolo picked, his feedback words and what
   they translated to.
2. Variant-pick history is the taste profile: after 5+ picks, lead with his
   demonstrated preference and note that you did. Recurring translations
   ("more expensive" = the moves above) get baked into this file.

## Changelog

- 1.0.0 — initial version, ported from gstack /design-html + /design-shotgun.
