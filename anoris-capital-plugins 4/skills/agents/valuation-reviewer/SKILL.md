---
name: valuation-reviewer
description: End-to-end agent that ingests GP valuation packages, runs the firm's valuation template, and stages LP reporting. Triggers include "process this quarter's GP valuation packages" or "run our valuation review workflow for this fund".
---

# Valuation Reviewer

## Overview
An end-to-end workflow agent that takes incoming general partner (GP) valuation packages for portfolio positions, runs them through the firm's standard valuation template/policy, and stages the resulting output for LP (limited partner) reporting.

## When to use this skill
- Quarterly valuation packages have come in from underlying GPs/fund managers and need to be processed against house valuation policy.
- A user needs valuation output staged and ready to feed into LP reporting materials.

## Process
1. Ingest each GP valuation package and extract the reported valuation, methodology used, and key supporting inputs (comps used, multiples applied, DCF assumptions, etc., as disclosed).
2. Run the firm's standard valuation template/policy check against each reported valuation — confirming methodology consistency with house policy and flagging any GP valuation that deviates materially from what the house approach would suggest.
3. Flag any position where the valuation methodology, comps set, or key assumption looks like an outlier relative to the GP's own prior periods or relative to peer funds holding similar assets.
4. Compile a consolidated position-by-position valuation summary, noting any items requiring further diligence before being accepted for reporting.
5. Stage the reviewed and accepted valuations into the format needed for LP reporting, clearly distinguishing GP-reported figures from any house-adjusted figures.

## Output format
A position-by-position valuation review summary (GP-reported value, methodology, house-policy check result, flags) and a staged dataset ready to feed LP reporting materials.

## Notes / guardrails
- Clearly distinguish GP-reported valuations from any internally adjusted figures — do not blend them without labeling.
- Flagged outliers require investment team/valuation committee review before being accepted into LP reporting — this agent stages and flags, it does not finalize valuations.
