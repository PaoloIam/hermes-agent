---
name: voice-memo-logger
description: |
  Turn Paolo's after-showing voice notes (or typed brain-dumps) into
  structured client records, roster updates, and scheduled follow-ups.
  Kills the evening admin pile. Load when a voice note arrives or Paolo
  dumps unstructured notes about clients, showings, or deals.
version: 1.0.0
platforms: [linux, macos, windows]
metadata:
  hermes:
    tags: [real-estate, notes, crm, voice, follow-up, admin]
    category: real-estate
    related_skills: [buyer-matchmaker, closing-anniversary, weekly-scorecard]
---

# Voice-Memo Logger

Paolo talks; you file. He sends a voice note from the car after a showing —
or types a messy brain-dump — and thirty seconds later everything is where
it belongs and tomorrow's follow-ups exist.

## Input

- A Telegram voice note: work from the transcript if the platform provides
  one. If no transcript is available on this deployment, say so once and
  ask him to type it — never pretend you heard something.
- Typed stream-of-consciousness: same treatment, no transcription needed.

## What you extract

From each memo, pull every one of these that appears:

1. **Client facts** → update `memories/buyer-roster.md` (active buyers) or
   `memories/client-book.md` (past clients). New person → new entry.
2. **Property feedback** — what they loved/hated. Goes in the client's
   notes; it's tomorrow's matching data.
3. **Commitments Paolo made** ("I told them I'd send comps by Friday") →
   follow-up list.
4. **Deal state changes** ("they want to offer", "they're out") → status
   update in the roster.
5. **Anything human** — dog's name, baby on the way. Small facts win deals.

## The follow-up list

`memories/follow-ups.md` under the Hermes home: one line each —
`<due date> | <who> | <what> | logged <date>`. Add every commitment with a
concrete date (Paolo said "Friday" → put the actual date). When a due item
comes up in ANY later conversation, surface it without being asked.

## Confirm back

End every run with a compact echo, not a wall:

```
Filed: <n> updates on <names>.
Follow-ups added: <due-date — what>, …
Anything I got wrong?
```

One correction round is expected — apply it silently.

## Self-improvement loop

1. Append one dated line to
   `memories/skill-learnings/voice-memo-logger.md`: what was filed, what
   Paolo corrected. Corrections are the metric — drive them to zero.
2. Read the last 30 lines before each run; if the same field keeps getting
   corrected, change how you extract it.
3. Lesson repeated 3+ times → surgical edit to THIS file + Changelog line.
   Edits persist across redeploys.

## Changelog

- 1.0.0 — initial version.
