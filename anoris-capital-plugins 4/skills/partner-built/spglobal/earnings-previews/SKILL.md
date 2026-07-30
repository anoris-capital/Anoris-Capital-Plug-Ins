---
name: earnings-previews
description: Use this skill to draft earnings preview notes ahead of a company's scheduled results release, using S&P Global data. Triggers include "write an earnings preview for [company]", "what should we expect from this print", or "prep ahead of [company]'s earnings".
---

# Earnings Previews

## Overview
Drafts an earnings preview note ahead of a company's scheduled results, using S&P Global consensus estimates and historical data to frame what the market expects and the key things to watch for in the print.

## When to use this skill
- A covered company has an upcoming earnings date and a preview note is needed.
- A user wants a quick briefing on consensus expectations and key watch-items before a print.

## Inputs
- Company name/ticker and upcoming earnings date.
- Consensus estimates (revenue, EPS, and key segment/margin metrics) from S&P Global data.
- Prior-period results and guidance for context.
- Any specific watch-items relevant to the current thesis (a segment under pressure, a margin inflection expected, a stated guidance range to check against).

## Process
1. Pull current consensus estimates for the upcoming period (revenue, EPS, key segment metrics) from S&P Global data.
2. Recap the prior period's results and any guidance given at that time, to frame what the company itself has signaled to expect.
3. Identify the specific watch-items most relevant to the thesis — not just headline numbers, but the underlying drivers analysts and investors are likely focused on.
4. Note where consensus estimates have moved (up/down) since the prior print, as a signal of how sentiment has shifted heading into the release.
5. Frame the preview around clear, specific questions the print should answer, rather than just restating consensus numbers.

## Output format
A short preview note: consensus estimates snapshot, recap of prior guidance, key watch-items framed as specific questions, and context on how estimates have trended into the print.

## Notes / guardrails
- Clearly label consensus estimates as estimates, not confirmed figures.
- Keep the preview focused on a few genuinely important watch-items rather than a generic restatement of every metric.
