---
name: closing-anniversary
description: |
  Send past clients a warm "one year in your home" note on their closing
  anniversary, with a soft market-value update. Past clients are where
  referrals live. Load when asked about anniversaries, or when a cron job
  runs this skill.
version: 1.0.0
platforms: [linux, macos, windows]
metadata:
  hermes:
    tags: [real-estate, client-retention, anniversaries, referrals]
    category: real-estate
    related_skills: [referral-harvester, voice-memo-logger]
---

# Closing Anniversary

A birthday note says "I remembered you." A closing-anniversary note says
"I remember the biggest purchase of your life, and I'm still watching out
for it." Cheap, compounding, almost nobody does it.

## The client book

Canonical file: `memories/client-book.md` under the Hermes home. One section
per past client:

```
## <Name(s)>
- property: <address>
- closed: <date> — <bought/sold> at <price>
- contact: <phone/email>
- personal: <kids, dog, renovation plans, anything human>
- last-touch: <date> — <what>
- referrals-given: <n>
```

Grow this file from every source: Paolo mentioning past deals, voice memos,
direct requests. When Paolo mentions a closing, add it without being asked
and confirm in one line.

## The run

When invoked (manually or by cron):

1. Scan the client book for closing anniversaries in the **next 7 days**.
2. For each, draft a note:
   - Lead with the milestone: "One year ago this week you got the keys to…"
   - One personal detail from the book if there is one.
   - Soft value line ONLY if you have real data (web search or Paolo's
     input): "similar units in the building have been trading around X."
     No data → no number. An invented valuation is worse than none.
   - Close with an open door, not a pitch: "If you ever want a fresh look
     at what it's worth, say the word."
3. Present all drafts in one message, dated by anniversary, ready to send.
4. Nothing sends automatically; Paolo owns the send.

If the client book is empty or thin, the run's output is instead a single
question: "Give me your last 5 closings (name, address, date) and I'll take
it from there."

## Self-improvement loop

1. Append one dated line to
   `memories/skill-learnings/closing-anniversary.md`: notes drafted, sent,
   any replies — especially replies that turned into valuation requests or
   referrals; that's the metric.
2. Read the last 30 lines before each run and evolve tone toward what earns
   replies.
3. Lesson repeated 3+ times → surgical edit to THIS file + Changelog line.
   Edits persist across redeploys.

## Changelog

- 1.0.0 — initial version.
