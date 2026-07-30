---
name: research-workflow
description: Use this skill to manage equity research publishing workflows — coverage calendars, note pipelines, and publication tracking. Triggers include "what's on our research calendar", "track our note pipeline", or "when is our next update due for [company]".
---

# Research Workflow

## Overview
Manages the operational side of equity research publishing: tracking which names are due for updates (earnings, events, periodic reviews), the status of notes in progress, and the publishing calendar.

## When to use this skill
- A research team needs to track what's coming up (earnings dates, upcoming events) across covered names.
- A user wants to know the status of notes currently in progress (draft, in review, ready to publish).
- A user needs a coverage calendar built or updated.

## Inputs
- List of covered names and their next known catalysts (earnings dates, investor days, product launches, regulatory decisions).
- Current status of any notes/reports in progress.
- Publishing cadence conventions (e.g., earnings notes within 24 hours of results, periodic deep-dives on a set schedule).

## Process
1. Build/maintain a coverage calendar listing each covered name and its next known catalyst date.
2. Track note pipeline status per name: not started, drafting, in internal review, ready to publish, published.
3. Flag upcoming catalysts that don't yet have a note started, prioritized by proximity to the event.
4. Flag notes that have been sitting in review or draft status longer than the house norm, so they don't slip.
5. Summarize the pipeline in a status view suitable for a team stand-up or weekly planning check-in.

## Output format
A coverage calendar (name, next catalyst, date) and a note-pipeline status tracker (name, note type, status, owner, target publish date), with at-risk items flagged separately.

## Notes / guardrails
- This tool organizes workflow and deadlines — it does not draft the analytical content itself (use earnings-analysis or initiating-coverage-report for that).
- Flag stale or slipping items rather than letting them go unnoticed.
