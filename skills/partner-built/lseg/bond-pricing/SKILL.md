---
name: bond-pricing
description: Use this skill to price bonds using LSEG market data and analytics. Triggers include "price this bond", "what's the fair value of this bond issue", or "calculate yield to maturity for this bond".
---

# Bond Pricing

## Overview
Prices fixed income securities using LSEG market data (yields, spreads, benchmark curves) — calculating clean/dirty price, yield to maturity/worst, and spread to benchmark for a given bond.

## When to use this skill
- A user needs a bond priced or its yield calculated given its terms and current market data.
- A user wants to check a bond's spread to the relevant benchmark curve (Treasury, swap, or sector curve).

## Inputs
- Bond terms: coupon rate, coupon frequency, maturity date, day-count convention, and any embedded options (call/put features).
- Current market data via LSEG: relevant benchmark yield curve, credit spread data for the issuer/sector/rating.
- Settlement date for the pricing calculation.

## Process
1. Confirm the bond's cash flow schedule from its terms (coupon amount and dates through maturity).
2. Pull the relevant benchmark curve and credit spread from LSEG data for the issuer's sector/rating.
3. Calculate the discount rate (benchmark yield + spread) and discount the bond's cash flows to present value for the clean price.
4. Add accrued interest since the last coupon date to get the dirty (full) price.
5. Calculate yield to maturity (and yield to worst if the bond has call features) by solving for the discount rate that equates the cash flows to the given price, if pricing in the other direction.
6. Present the spread to benchmark alongside the price/yield so the result can be assessed in relative-value terms, not just in isolation.

## Output format
Clean price, dirty price, yield to maturity (and yield to worst if applicable), and spread to the relevant benchmark, with the underlying curve/spread data sourced clearly noted.

## Notes / guardrails
- State the benchmark curve and spread assumptions used explicitly, since they drive the entire calculation.
- Flag illiquid issues or stale market data where LSEG pricing confidence is lower.
