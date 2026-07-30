---
name: company-tearsheets
description: Use this skill to generate company tearsheets from S&P Global data. Triggers include "pull a tearsheet on [company]", "give me a quick company snapshot", or "build a one-page overview of this business".
---

# Company Tearsheets

## Overview
Generates a concise one-page company tearsheet using S&P Global data: business description, key financials, valuation multiples, ownership/analyst coverage snapshot, and recent notable events.

## When to use this skill
- A user needs a fast, standardized company snapshot ahead of a meeting or initial screen.
- A user wants a quick-reference overview of a company without a full deep-dive report.

## Inputs
- Company name/ticker.
- Any specific focus area to emphasize (financials, valuation, ownership) if the user wants the tearsheet weighted toward a particular angle.

## Process
1. Pull core company data from S&P Global: business description, sector/industry classification, key executives.
2. Pull key financial metrics: revenue, EBITDA, net income, and margins for the most recent periods, plus a short historical trend.
3. Pull valuation data: current trading multiples (EV/EBITDA, P/E) and how they compare to sector averages if available.
4. Pull ownership/analyst snapshot: major shareholders, analyst rating distribution/consensus target if covered.
5. Note any recent notable events (M&A activity, major announcements, leadership changes) from available data.
6. Assemble into a single, standardized one-page format so tearsheets are easy to compare across companies.

## Output format
A one-page tearsheet: business description, key financials table, valuation snapshot, ownership/coverage summary, and recent notable events — in a consistent format across companies.

## Notes / guardrails
- Keep it to a true one-page snapshot — route anything requiring more depth to a fuller analysis (e.g., competitive-analysis or initiating-coverage-report).
- Note the data as-of date since tearsheets are meant for quick reference and can go stale.
