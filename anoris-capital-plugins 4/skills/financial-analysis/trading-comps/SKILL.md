---
name: trading-comps
description: Use this skill to build a public trading comparables ("comps") analysis for a target company. Triggers include "build comps for [company]", "what multiple should this trade at", or "find comparable public companies".
---

# Trading Comps

## Overview
Builds a public trading comparables set: identifies a peer group, pulls trading multiples (EV/Revenue, EV/EBITDA, P/E, etc.), and benchmarks the target company against peer medians/means to inform valuation.

## When to use this skill
- A user wants to know what multiple a company should trade at relative to peers.
- A user wants a peer set identified and benchmarked for a pitch, memo, or valuation cross-check.
- A user wants to sanity-check a DCF or LBO output against public market pricing.

## Inputs
- Target company name/ticker and a description of its business (sector, sub-sector, business model, geography, size).
- Preferred multiples to focus on (EV/Revenue, EV/EBITDA, EV/EBIT, P/E, P/B — sector-dependent).
- Data source availability (e.g., S&P Global, LSEG, or figures the user provides directly).
- Any explicit peers the user wants included or excluded.

## Process
1. Define the peer set: same sector/sub-sector, similar business model, comparable size (market cap/revenue), similar growth and margin profile, similar geography where relevant. Aim for 6-12 names; note where the set is thin.
2. Pull or request: market cap, enterprise value, LTM and forward revenue/EBITDA/EPS, growth rates, and margins for each peer.
3. Calculate the relevant multiples for each peer and for the target.
4. Compute peer group median, mean, and quartile range for each multiple.
5. Benchmark the target against the peer set — note whether it screens cheap/expensive and why (growth, margin, scale, quality differences that justify a premium or discount).
6. Apply the peer multiple range to the target's own metrics to derive an implied valuation range.
7. Flag outliers in the peer set (unusually high/low multiples) and explain whether to exclude them or note them as context.

## Output format
A comps table (peers as rows, key metrics and multiples as columns) with summary statistics (median/mean/quartiles) and a short narrative on where the target screens relative to peers and why. Include an implied valuation range derived from the peer multiples.

## Notes / guardrails
- State peer selection criteria explicitly so the analysis is reproducible and defensible.
- Multiples analysis is a relative valuation tool, not a standalone recommendation — pair with DCF or other methods when possible.
- Watch for stale or non-comparable data (different fiscal year ends, one-time items distorting margins) and flag it.
