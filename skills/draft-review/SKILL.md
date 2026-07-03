---
name: draft-review
description: |
  Self-review pass over any outbound draft (outreach, newsletter, email,
  follow-up) BEFORE Paolo sees it: facts, tone, compliance, and one
  would-I-reply test. Ported from gstack's /review and /qa concepts.
  Load whenever another skill or request produces text meant for a client
  or prospect.
version: 1.0.0
platforms: [linux, macos, windows]
metadata:
  hermes:
    tags: [review, qa, quality, compliance, outreach]
    category: operations
    related_skills: [safety-gate, buyer-matchmaker, open-house-followup]
---

# Draft Review

Every outbound draft gets reviewed by a harsher version of you before
Paolo sees it. He should never be your QA department.

## The pass — run silently, before presenting any draft

1. **Facts**: every number, address, price, date, and name in the draft is
   traceable to a source (Paolo said it, a file contains it, a search
   found it). Anything untraceable gets removed or flagged inline as
   `[verify: …]` — never silently kept.
2. **Identity**: reads like Paolo — short, warm, direct. Kill em-dash
   pileups, "I hope this finds you well", "just checking in", and anything
   a template farm would write.
3. **Compliance**: no steering, no discriminatory language (fair-housing
   basics), no promises about outcomes or valuations stated as fact, no
   poaching represented clients. One flag line if something is borderline.
4. **The reply test**: read it as the recipient. If the honest reaction is
   "delete", rewrite before presenting. If two rewrites still fail the
   test, present the best version WITH the concern stated — Paolo decides.
5. **One ask**: exactly one call-to-action per message. Two asks = a cut.

## Output convention

Present the final draft clean. Below it, at most two short lines:
`Review notes: <flags, if any>`. No notes if nothing flagged — silence is
the signal that the pass was clean, and the pass ALWAYS ran.

## Self-improvement loop

1. Append one dated line to `memories/skill-learnings/draft-review.md`:
   what was reviewed, what the pass caught, and — the metric — anything
   Paolo still had to correct after the pass.
2. Paolo's post-review corrections are review failures: each one becomes a
   named check in the pass above (surgical edit + Changelog line) so the
   same class of miss cannot recur.

## Changelog

- 1.0.0 — initial version, ported from gstack /review + /qa concepts.
