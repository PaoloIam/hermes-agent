---
name: open-house-followup
description: |
  Turn an open-house sign-in list into ranked, personalized follow-up
  messages within minutes. Load when Paolo sends a sign-in list (text or
  photo) or mentions he just finished an open house.
version: 1.0.0
platforms: [linux, macos, windows]
metadata:
  hermes:
    tags: [real-estate, open-house, follow-up, lead-gen, speed-to-lead]
    category: real-estate
    related_skills: [buyer-matchmaker, referral-harvester]
---

# Open-House Follow-Up

Speed of follow-up is where deals are won. Most agents follow up the next
day, exhausted, with a generic blast. Paolo's follow-ups go out the same
evening and sound like he remembers each person — because you do.

## Input

Paolo sends the sign-in list right after the open house — pasted text, a
forwarded form export, or a photo of the paper sheet. If a photo is
unreadable (vision may be limited on this deployment), say which lines you
could not read and ask him to type just those.

Also ask, once, in a single short message: "Anything memorable about
specific visitors?" His color ("couple with the golden retriever, asked
about the roof deck twice") is worth more than the form data.

## Output — the follow-up sheet

For each attendee, ranked by buying signal, strongest first:

```
#<rank> — <name> — signal: <hot/warm/cool>
  Why: <what marks them — asked about offers, second visit, has agent?, …>
  Text draft: <SMS-length, references something specific, one clear next step>
  Email draft: <3–5 sentences, same substance, slightly fuller>
```

Signals that rank someone hot: asked about offer deadlines or seller
motivation, second visit, no current agent, timeline language ("our lease
ends in October"). Already-represented visitors rank cool and their draft
is a polite one-liner — never try to poach; it backfires and it's a
professional-conduct issue.

Every draft names something real: the dog, the roof-deck question, the
school question. If you know nothing specific about an attendee, say so in
the sheet instead of writing filler — Paolo decides whether a generic note
is worth sending.

## After the sheet

- Any attendee who reads as an active buyer: offer to add them to the buyer
  roster (`buyer-matchmaker` skill owns that file). One question, not a form.
- Log which drafts Paolo sent and what came back.

## Self-improvement loop

1. Append one dated line to
   `memories/skill-learnings/open-house-followup.md`: attendee count, drafts
   sent, replies/showings that resulted, one adjustment for next time.
2. Read the last 30 lines before each run; the goal metric is replies, so
   evolve the drafts toward whatever wording earns them.
3. Lesson repeated 3+ times → surgical edit to THIS file + Changelog line.
   Edits persist across redeploys.

## Changelog

- 1.0.0 — initial version.
