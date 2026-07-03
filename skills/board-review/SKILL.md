---
name: board-review
description: |
  Pressure-test a business decision from three seats — CEO, head of
  marketing, compliance officer — then give one merged recommendation.
  Ported from gstack's /office-hours and /plan-*-review concepts. Load
  when Paolo floats a plan, pricing, spend, pivot, or "should I…?"
version: 1.0.0
platforms: [linux, macos, windows]
metadata:
  hermes:
    tags: [strategy, decision-review, critique, business]
    category: real-estate
    related_skills: [weekly-scorecard, safety-gate]
---

# Board Review

Solo operators have no one to argue with before committing. This skill is
the argument. When Paolo floats a decision — new farm area, ad spend, a
fee change, a partnership, a big listing pitch — convene the board.

## The three seats

Run each seat honestly and independently; they are allowed to disagree:

1. **CEO seat** — return on Paolo's TIME above all. Does this compound or
   distract? What is the opportunity cost against the current pipeline
   (read `memories/follow-ups.md` and the roster — ground it in his real
   book of business, not generic advice)?
2. **Marketing seat** — who actually sees this and what do they feel?
   Differentiation or noise? What would make it 10x more visible for the
   same effort?
3. **Compliance seat** — licensing, fair housing, advertising rules,
   commission disclosure, data handling. This seat can only flag, in plain
   words, and rates each flag: blocker / needs-a-check / cosmetic.

## Output format

```
BOARD REVIEW: <decision in one line>
CEO: <3–5 sentences, ends with FOR / AGAINST / FOR-IF>
Marketing: <3–5 sentences, ends with FOR / AGAINST / FOR-IF>
Compliance: <flags with severity, or "no flags">
MERGED CALL: <one paragraph: the recommendation, the single biggest risk,
and the cheapest possible test to run before committing fully>
```

Rules: the seats must not all agree by default — if the vote is unanimous,
say explicitly why no seat found a real objection. The merged call always
includes the cheapest reversible test (gstack's canary idea): before the
big commitment, what 1-week, near-free version proves or kills the idea?

## Self-improvement loop

1. Append one dated line to `memories/skill-learnings/board-review.md`:
   the decision, the merged call, what Paolo actually did.
2. The metric is calibration: revisit past calls when outcomes become
   known (weekly-scorecard surfaces them) and note where a seat was
   systematically wrong — then sharpen that seat's brief with a surgical
   edit + Changelog line.

## Changelog

- 1.0.0 — initial version, ported from gstack /office-hours + plan-review concepts.
