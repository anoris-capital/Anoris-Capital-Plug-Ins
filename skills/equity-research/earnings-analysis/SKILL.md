---
name: earnings-analysis
description: Use this skill to analyze a company's quarterly earnings release and call transcript against expectations. Triggers include "analyze this earnings report", "how did [company] do vs. estimates", or "summarize the earnings call".
---

# Earnings Analysis

## Overview
Analyzes a quarterly earnings release (press release, financial statements, call transcript) against consensus/prior expectations, extracting the key beats/misses, guidance changes, and management commentary that matter for the investment thesis.

## When to use this skill
- A company just reported earnings and a user needs a fast, structured read on the results.
- A user wants earnings-call commentary distilled into the key quotes/takeaways relevant to the thesis.
- A user needs to compare actual results to consensus estimates and prior guidance.

## Inputs
- The earnings release, financial statements, and/or call transcript.
- Consensus estimates or prior guidance to compare against, where available.
- The existing investment thesis or key watch-items for the name, if relevant, so the analysis can be targeted.

## Process
1. Extract headline results: revenue, EPS, and key segment/margin metrics vs. consensus and vs. prior-year.
2. Identify beats and misses, and — more importantly — why: one-time items, mix shift, volume vs. price, cost inflation/deflation, etc.
3. Compare updated guidance (if given) to prior guidance and to consensus, flagging any raise/cut/reiterate and its magnitude.
4. Scan the call transcript/Q&A for management commentary on the specific watch-items relevant to the thesis (demand trends, margin trajectory, capital allocation, competitive dynamics).
5. Note any change in tone or new disclosure (new segment reporting, new risk factor, change in capital allocation policy) that could be a leading indicator.
6. Synthesize into a clear "what changed and why it matters" summary rather than a restatement of the press release.

## Output format
A structured summary: (1) headline numbers vs. expectations, (2) guidance changes, (3) key management commentary/quotes on watch-items, (4) an overall read on whether the print was a positive, negative, or neutral update to the thesis and why.

## Notes / guardrails
- Distinguish reported facts from analytical interpretation of what they mean.
- Flag when data needed for a full comparison (e.g., consensus estimates) wasn't available, rather than guessing at a number.
