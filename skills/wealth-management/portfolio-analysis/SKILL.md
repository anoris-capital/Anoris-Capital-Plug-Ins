---
name: portfolio-analysis
description: Use this skill to analyze a client portfolio's composition, performance, and risk characteristics. Triggers include "analyze this portfolio", "what's our risk exposure here", or "check this portfolio's asset allocation".
---

# Portfolio Analysis

## Overview
Analyzes a portfolio's current composition (asset allocation, sector/geography exposure, concentration), performance (absolute and relative to benchmark), and risk characteristics (volatility, drawdown, factor exposures).

## When to use this skill
- A user wants to understand a portfolio's current allocation and whether it matches its target/policy allocation.
- A user wants performance attribution — what drove returns over a period.
- A user wants a risk read on a portfolio: concentration, volatility, correlation to the broader market.

## Inputs
- Current portfolio holdings with weights/values.
- Target/policy allocation, if one exists, for comparison.
- Performance history and a relevant benchmark for comparison.
- Risk tolerance or mandate constraints, if applicable.

## Process
1. Summarize current composition: asset class allocation, sector/geography breakdown, and top holdings/concentrations.
2. Compare current allocation to target/policy allocation and flag any meaningful drift.
3. Analyze performance over the relevant period: absolute return, relative to benchmark, and attribution (which holdings/sectors drove out- or under-performance).
4. Assess risk characteristics: concentration risk (single-name, sector, geography), volatility relative to benchmark, and any notable correlation/factor exposures.
5. Flag anything that looks inconsistent with the stated mandate or risk tolerance (e.g., a concentration that exceeds policy limits).
6. Where relevant, note rebalancing considerations to bring the portfolio back toward target allocation.

## Output format
A structured summary: current allocation vs. target, performance and attribution, key risk flags, and rebalancing considerations if applicable.

## Notes / guardrails
- Present risk/concentration flags clearly and separately from performance commentary — don't bury a mandate breach in a performance summary.
- This is analytical output for the advisor/PM to act on — not an automated trading or rebalancing instruction.
