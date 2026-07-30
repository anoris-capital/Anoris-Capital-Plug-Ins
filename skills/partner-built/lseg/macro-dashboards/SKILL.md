---
name: macro-dashboards
description: Use this skill to build macro dashboards using LSEG financial data and analytics. Triggers include "build a macro dashboard for [region/theme]", "put together a rates and FX overview", or "track these macro indicators for me".
---

# Macro Dashboards

## Overview
Builds consolidated macro dashboards pulling together key indicators (rates, FX, inflation, growth data, commodity prices) from LSEG into a single, organized view for ongoing monitoring or a specific briefing.

## When to use this skill
- A user wants an ongoing or one-time consolidated view of macro indicators for a region or theme.
- A user needs a dashboard built for recurring monitoring (e.g., a weekly macro update) rather than a one-off analysis.

## Inputs
- Scope: region(s), theme (e.g., rates and inflation, FX and trade, growth indicators), and the specific series to include.
- Update cadence, if this is meant to be a recurring dashboard rather than a one-time pull.
- Any specific benchmark/comparison periods desired (vs. prior month, prior year).

## Process
1. Define the specific indicators in scope (e.g., policy rates, key yield curve points, CPI/inflation prints, GDP growth, PMI data, major FX pairs, key commodity prices) based on the requested theme.
2. Pull current values for each indicator from LSEG, along with the relevant comparison period value (prior month/quarter/year) for context.
3. Organize the dashboard logically by category (rates, FX, growth/inflation, commodities) rather than as an undifferentiated list.
4. Highlight any indicator showing a notable recent move or divergence from trend, so the dashboard surfaces what's changed, not just static levels.
5. If built as a recurring dashboard, note the data vintage/as-of date clearly each time it's refreshed.

## Output format
A categorized dashboard of current indicator levels with period-over-period comparison, and a short set of highlights calling out notable recent moves.

## Notes / guardrails
- Always label the as-of date/time for the data, since macro dashboards are only useful if their vintage is clear.
- Present indicator moves factually; avoid stating a single causal explanation for a macro move unless it's well-supported.
