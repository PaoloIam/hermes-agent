---
name: weekly-scorecard
description: |
  Friday review: who was contacted, who went quiet, what's stalling in the
  pipeline, wins, and Monday's top five actions — plus a meta-review of all
  the other skills' learning logs with one concrete improvement proposal.
  Load when asked for the weekly review, or when a cron job runs this skill.
version: 1.0.0
platforms: [linux, macos, windows]
metadata:
  hermes:
    tags: [real-estate, review, pipeline, metrics, meta-improvement]
    category: real-estate
    related_skills: [buyer-matchmaker, expired-listing-hunter, voice-memo-logger]
---

# Weekly Scorecard

Forces the business to be managed by numbers without building a dashboard.
Runs Friday (or on demand). Two halves: the business review, and the
skill-fleet review — this skill is the improvement loop's supervisor.

## Sources — read, don't ask (mostly)

- `memories/buyer-roster.md` — active buyers, last-contact dates.
- `memories/client-book.md` — past-client touches.
- `memories/follow-ups.md` — what was due this week; done or overdue?
- `memories/referral-ledger.md` — asks made, referrals landed.
- `memories/skill-learnings/*.md` — every skill's log for the week.
- This week's conversation history, if searchable.

If the files are thin, ask Paolo at most THREE quick-fire questions
(deals in play? new leads? anything stalled?) — then build with what exists.
A scorecard from partial data beats an interrogation.

## Part 1 — the business scorecard

```
WEEK OF <dates>
Contacted: <n> people (<names, compressed>)
Went quiet: <buyers/clients with no touch in 14+ days — name + days>
Stalled: <deals with no state change in 2+ weeks + one-line why>
Wins: <replies, showings, offers, referrals — concrete only>
Dropped balls: <overdue follow-ups from follow-ups.md>
MONDAY TOP 5:
1–5. <specific actions with names — "call X about Y", never "do outreach">
```

Numbers honest, including zeros. A zero-contact week stated plainly is the
whole point of a scorecard.

## Part 2 — the fleet review (meta-improvement)

Read every `memories/skill-learnings/*.md`. For each active skill, one line:
used how often, produced what, what got sent/ignored. Then propose exactly
ONE improvement — the highest-value change to any single skill's SKILL.md,
stated as: "I want to change <skill>: <from what → to what> because <pattern
from its log>."

If Paolo approves, apply the edit to that skill file yourself (surgical
edit + Changelog line in the target skill) and log the change in
`memories/skill-learnings/weekly-scorecard.md`. One improvement per week,
compounding — that is the self-improvement loop working as designed.

## Self-improvement loop (own log)

1. Append one dated line to `memories/skill-learnings/weekly-scorecard.md`:
   scorecard delivered, which Monday-5 items got done by next Friday.
2. The metric is Monday-5 completion rate: if items keep rolling over,
   make them smaller and more specific.
3. Lesson repeated 3+ times → surgical edit to THIS file + Changelog line.

## Changelog

- 1.0.0 — initial version.
