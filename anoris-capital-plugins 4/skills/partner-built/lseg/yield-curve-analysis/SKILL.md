---
name: yield-curve-analysis
description: Use this skill to analyze and visualize yield curves using LSEG data. Triggers include "show me the current yield curve", "how has the curve shifted", or "analyze the curve shape for [market]".
---

# Yield Curve Analysis

## Overview
Pulls and analyzes yield curve data via LSEG for a given market (government, swap, or credit curve), examining level, shape, and changes over time to inform rate-view or relative-value analysis.

## When to use this skill
- A user wants a current snapshot of a yield curve and its shape (normal, flat, inverted).
- A user wants to understand how a curve has shifted over a period (parallel shift, steepening, flattening).
- A user needs curve data as an input to another analysis (e.g., bond-pricing or macro-dashboards).

## Inputs
- The specific curve requested (e.g., U.S. Treasury, a specific sovereign curve, a swap curve, or a credit curve for a sector/rating).
- The comparison period, if analyzing change over time (e.g., current vs. 3 months ago, vs. 1 year ago).

## Process
1. Pull the current curve data points across the relevant tenor range from LSEG.
2. Characterize the curve shape: normal (upward-sloping), flat, or inverted, and at which points along the curve any inversion occurs.
3. If a comparison period is requested, pull the historical curve for that date and calculate the change at each tenor point.
4. Characterize the type of shift: parallel (level shift across all tenors), steepening (long end rising/falling more than short end), or flattening (the reverse).
5. Connect the curve shape/shift to its typical macro interpretation (e.g., inversion often read as a recession-risk signal, steepening often read as growth/inflation expectations shifting) while being clear this is a general market heuristic, not a certain prediction.

## Output format
A curve snapshot (rates by tenor) and, if requested, a comparison table/chart showing the shift by tenor, plus a short description of the curve's shape and change.

## Notes / guardrails
- Curve-shape interpretations (recession signal, growth signal) are general market heuristics, not forecasts — present them as such, not as certainties.
- Note the data date/time clearly since curves move daily.
