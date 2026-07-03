---
name: buyer-matchmaker
description: |
  Maintain a living roster of active buyers (budget, areas, must-haves,
  timeline) and, whenever new inventory or a price drop appears, instantly
  identify which buyers it fits and draft the "I found something for you"
  outreach. Load when Paolo shares a listing, a price change, or asks who
  fits a property.
version: 1.0.0
platforms: [linux, macos, windows]
metadata:
  hermes:
    tags: [real-estate, buyers, matching, outreach, lead-gen]
    category: real-estate
    related_skills: [voice-memo-logger, weekly-scorecard]
---

# Buyer Matchmaker

Turn market noise into same-day outreach. You own two jobs: keep the buyer
roster current, and match inventory to buyers the moment it appears.

## The roster

Canonical file: `memories/buyer-roster.md` under the Hermes home
(`/opt/data/memories/buyer-roster.md` on this deployment). One section per
buyer:

```
## <Name>
- contact: <phone/email/telegram>
- budget: <min>–<max>
- areas: <neighborhoods, in priority order>
- must-haves: <hard requirements — beds, outdoor space, pet policy…>
- nice-to-haves: <soft preferences>
- financing: <cash / pre-approved amount / status unknown>
- timeline: <now / 3mo / browsing>
- status: active | paused | closed
- last-contact: <date> — <what happened>
- notes: <anything else>
```

Whenever Paolo mentions a new buyer or new facts about one (in any
conversation, not just this skill), update the roster. If a required field is
unknown, ask Paolo at most two short questions — never interrogate.

## Matching, when inventory appears

Paolo will forward a listing, mention a price drop, or paste a new-development
tidbit. Then:

1. Extract the property facts: price, area, beds/baths, key features,
   what changed (new / price cut / back on market).
2. Score every **active** buyer:
   - Hard filters first: budget (allow 5% stretch above stated max), area.
   - Then must-haves: a missing must-have disqualifies unless Paolo has
     flagged it as flexible.
   - Rank the survivors by: timeline urgency, nice-to-have overlap, and how
     long since last contact (a match is also a touchpoint).
3. Reply with the **top 3 at most**: buyer name, one-line why-it-fits,
   one-line risk ("20k over her ceiling").
4. For the best match, draft the outreach message ready to send: short,
   personal, references something specific the buyer told Paolo, no
   sales-brochure tone. Offer drafts for #2 and #3 only if Paolo asks.
5. Never contact anyone yourself. Everything goes through Paolo.

If web search is available, verify the listing is still active before
drafting; a dead-link send burns trust.

## Self-improvement loop

Every run ends with a learning pass:

1. Append one dated line to `memories/skill-learnings/buyer-matchmaker.md`:
   what you matched, whether Paolo sent the draft, any reply/outcome he
   reported, one thing to do differently.
2. Before every run, read the last 30 lines of that file and apply them.
3. When the same lesson shows up 3+ times, bake it in: surgically edit THIS
   file (`skills/buyer-matchmaker/SKILL.md` under the Hermes home) and add a
   Changelog line. Your edits persist across redeploys — bundled-skill sync
   skips user-modified skills.
4. Messages that got replies are the most valuable data this skill owns:
   record the winning wording verbatim.

## Changelog

- 1.0.0 — initial version.
