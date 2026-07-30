---
name: fx-carry-trade-evaluation
description: Use this skill to evaluate FX carry trade opportunities using LSEG data. Triggers include "evaluate this carry trade", "what's the carry on [currency pair]", or "check funding vs. target currency yield differential".
---

# FX Carry Trade Evaluation

## Overview
Evaluates the attractiveness of an FX carry trade (borrowing in a low-yield funding currency to invest in a higher-yield target currency) using LSEG interest rate and FX data — calculating expected carry, adjusting for forward points, and flagging volatility/risk considerations.

## When to use this skill
- A user wants to assess a specific currency pair's carry trade opportunity.
- A user wants to compare carry opportunities across several currency pairs.

## Inputs
- Funding currency and target currency.
- Relevant interest rate data for both currencies (policy rates or money-market rates via LSEG).
- Current spot rate and forward points/rate for the pair.
- Holding period for the trade.

## Process
1. Pull the relevant interest rates for the funding and target currencies from LSEG.
2. Calculate the raw interest rate differential (carry) between the two currencies.
3. Pull the forward rate/forward points for the pair and calculate the covered interest rate parity implied return, to distinguish covered vs. uncovered carry.
4. Calculate expected carry return over the specified holding period, both before and after accounting for forward points.
5. Assess FX volatility for the pair (historical volatility from LSEG data) since carry trade risk is dominated by FX moves that can easily overwhelm the carry earned.
6. Present the carry opportunity alongside its volatility context so the risk/reward is clear, not just the raw yield differential.

## Output format
Interest rate differential, forward points, expected carry return over the holding period, and relevant FX volatility context, with a clear statement of the risk (FX move risk can exceed carry earned).

## Notes / guardrails
- Always present carry alongside volatility/risk context — a carry number in isolation is misleading given how FX-move risk dominates these trades.
- This is analytical output, not a trade recommendation or execution instruction.
