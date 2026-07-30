---
name: market-researcher
description: End-to-end agent that takes a sector or theme and produces an industry overview, competitive landscape, peer comps, and an ideas shortlist. Triggers include "research this sector for me end to end" or "give me a full market map on [theme]".
---

# Market Researcher

## Overview
An end-to-end workflow agent that takes a sector or investment theme as input and produces a full research package: industry overview, competitive landscape mapping, peer trading comps, and a shortlist of specific investment ideas that fit the theme.

## When to use this skill
- A user wants to explore a new sector or theme from scratch and needs the full research arc, not just one piece of it.
- A user needs an ideas shortlist grounded in an actual landscape/comps analysis, not just a list of names.

## Process
1. Define the sector/theme scope clearly (sub-sectors included/excluded, geography, company size range).
2. Build an industry overview: market size, growth drivers, structural trends, regulatory context.
3. Run the competitive-analysis workflow to map the competitive landscape — key players, how they're positioned relative to each other.
4. Run the trading-comps workflow across the identified players to add a valuation lens to the landscape.
5. Synthesize an ideas shortlist: specific companies (public or private, depending on scope) that screen attractively against the theme, each with a short rationale.
6. Present the full package together: overview → landscape → comps → shortlist, so the ideas are traceable back to the underlying research rather than appearing unsupported.

## Output format
A structured research package: industry overview narrative, competitive landscape map/table, comps table, and a prioritized ideas shortlist with rationale for each name.

## Notes / guardrails
- Every shortlisted idea should have a stated rationale traceable to the landscape/comps work, not just an assertion.
- Flag sectors/themes where public data is thin (e.g., early-stage or highly private markets) since the research package will necessarily be less complete.
