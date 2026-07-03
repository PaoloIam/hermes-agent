---
name: expired-listing-hunter
description: |
  Produce a ranked outreach sheet for listings that expired or were
  withdrawn in Paolo's farm area, with a personalized opener per owner.
  The warmest cold leads that exist; consistency wins them. Load when
  asked to hunt expireds, or when a cron job runs this skill.
version: 1.0.0
platforms: [linux, macos, windows]
metadata:
  hermes:
    tags: [real-estate, expired-listings, outreach, lead-gen, prospecting]
    category: real-estate
    related_skills: [buyer-matchmaker, weekly-scorecard]
---

# Expired-Listing Hunter

An expired listing is an owner who already decided to sell and got let down.
Your job: find them, understand why the listing died, and hand Paolo a sheet
he can start calling from in the next ten minutes.

## Getting the data (in this order)

1. If Paolo pasted or forwarded a list of expired/withdrawn listings, use it.
2. If the web tool is available, search for expired and withdrawn listings in
   Paolo's farm area (ask him once for the area and remember it in
   `memories/farm-area.md`; reuse it forever after).
3. If neither works, reply with exactly what you need: "Forward me today's
   expired/withdrawn alert from your MLS and I'll build the sheet." Do not
   fabricate listings. Ever. An invented address on a call sheet destroys
   the whole system's credibility.

## The sheet

For each listing, one block, ranked best-first:

```
#<rank> — <address>
  Was asking: <price> (<days on market> DOM, <n> price cuts)
  Why it likely died: <overpriced / bad photos / timing / stale — one line>
  Owner angle: <what matters to this owner, best guess>
  Opener: <≤3 sentences, specific to THIS property, no template smell>
  Caution: <anything — relisted with another broker, litigation, unknown owner>
```

Ranking: likelihood of relisting soon (recent expiry, multiple cuts = motivated)
beats absolute price. Five great blocks beat twenty mediocre ones — cap at 10.

## Rules

- The opener must reference a concrete fact about the property. "I noticed
  your listing expired" is banned as an opening line — every agent says it.
- Flag any listing that already relisted with another brokerage: it goes in
  a "do not call" note, not the sheet.
- Respect do-not-call basics: these are drafts for Paolo, who owns compliance;
  remind him once per sheet, in one short line, not a lecture.

## Self-improvement loop

1. Append one dated line to
   `memories/skill-learnings/expired-listing-hunter.md`: sheet size, which
   openers Paolo actually used, any owner responses he reported.
2. Read the last 30 lines before each run and adapt the ranking and opener
   style to what got responses.
3. Lesson repeated 3+ times → edit THIS file surgically and add a Changelog
   line. Your edits survive redeploys (sync skips user-modified skills).

## Changelog

- 1.0.0 — initial version.
