---
name: options-valuation
description: Use this skill to value options using LSEG analytics and market data. Triggers include "value this option", "what's the theoretical price of this call/put", or "check implied volatility for this option".
---

# Options Valuation

## Overview
Values options (equity, index, FX, or rates options) using LSEG market data and standard option pricing models (Black-Scholes for European-style, binomial/other approaches for American-style where needed), and surfaces implied volatility and greeks.

## When to use this skill
- A user needs a theoretical value for a specific option contract.
- A user wants implied volatility or greeks (delta, gamma, vega, theta) for a position.
- A user wants to compare an option's market price to a model-derived theoretical value.

## Inputs
- Option terms: underlying, strike, expiration date, option type (call/put), style (European/American).
- Current underlying price and relevant risk-free rate and dividend yield (for equities) via LSEG.
- Volatility input: either a stated volatility assumption or implied volatility pulled from LSEG market data for the specific contract.

## Process
1. Confirm option terms and pull the current underlying price, risk-free rate, and dividend yield (if applicable) from LSEG.
2. Pull or confirm the volatility input — prefer market-implied volatility for the specific contract where available, and state clearly if a manual assumption is used instead.
3. Apply the appropriate pricing model given the option's style (Black-Scholes for European; adjust or use an alternative approach for American-style options with early-exercise value, especially for dividend-paying underlyings).
4. Calculate the theoretical price and the key greeks (delta, gamma, theta, vega, and rho if relevant).
5. If a market price is available, compare it to the theoretical value and note the implied volatility the market price is pricing in, versus the volatility input used.

## Output format
Theoretical option price, greeks, and (if applicable) a comparison to market price with the corresponding implied volatility, with all inputs used stated explicitly.

## Notes / guardrails
- State the volatility assumption/source explicitly — it's the single biggest driver of the output and often the least certain input.
- This is analytical valuation output, not a trading recommendation.
