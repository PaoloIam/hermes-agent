---
name: referral-harvester
description: |
  After any warm client exchange, draft a natural referral ask so it
  actually gets sent instead of merely intended. Tracks asks per client to
  avoid over-asking. Load when Paolo reports a positive client interaction,
  a thank-you, a closed deal, or a glowing message.
version: 1.0.0
platforms: [linux, macos, windows]
metadata:
  hermes:
    tags: [real-estate, referrals, client-retention, outreach]
    category: real-estate
    related_skills: [closing-anniversary, open-house-followup]
---

# Referral Harvester

Referrals are asked for at the peak of goodwill or not at all. Paolo's
peak-goodwill moments — a thank-you text, a smooth closing, a solved
problem — are exactly when he's busiest, so the ask never happens. Your job:
catch the moment and put a ready-to-send ask in his hand.

## The trigger

Whenever Paolo shares a warm moment — a client's thank-you, a positive
review, a closing that went well, "the Smiths loved the apartment" — treat
it as a referral opportunity. Don't wait to be asked. Offer the draft in
the same reply.

## The ledger

`memories/referral-ledger.md` under the Hermes home: one line per ask —
date, client, occasion, sent?, outcome. Check it BEFORE drafting:

- Asked this client in the last 6 months → don't ask again; suggest a
  no-ask warm reply instead and say why you're holding back.
- Client already referred someone → the draft is a thank-you-for-referring
  note (gratitude compounds referrals better than repeat asks).

## The draft

Rules that make asks feel natural instead of needy:

- Anchor to the moment: reply to what just happened first, ask second.
- Ask for a *person*, not "anyone": "if a friend from the building is
  thinking about selling…" beats "if you know anyone."
- One sentence of ask, maximum. No incentives unless Paolo says so —
  incentive-led asks read as transactional and can raise compliance issues.
- Match the medium: if the goodwill arrived by text, the ask is
  text-length; email gets 3–4 sentences.

Output: the draft plus a one-line ledger note you've already recorded.
Nothing sends automatically.

## Self-improvement loop

1. Append one dated line to
   `memories/skill-learnings/referral-harvester.md`: occasion, whether the
   ask was sent, and — the metric — whether a referral eventually arrived.
2. Read the last 30 lines before drafting; evolve wording toward asks that
   produced actual referrals.
3. Lesson repeated 3+ times → surgical edit to THIS file + Changelog line.
   Edits persist across redeploys.

## Changelog

- 1.0.0 — initial version.
