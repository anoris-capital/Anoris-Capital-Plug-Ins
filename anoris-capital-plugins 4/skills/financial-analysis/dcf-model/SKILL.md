---
name: dcf-model
description: Use this skill to build, update, or sanity-check a discounted cash flow (DCF) valuation model for a company. Triggers include requests to "build a DCF", "value this company", "project free cash flow", or "update the DCF for [ticker]".
---

# DCF Model

## Overview
Builds a discounted cash flow valuation: projects unlevered free cash flow over an explicit forecast period, discounts it at the weighted average cost of capital (WACC), and derives a terminal value to arrive at enterprise and equity value per share.

## When to use this skill
- A user asks for a company valuation, intrinsic value estimate, or price target grounded in cash flow projections.
- A user wants to stress-test a valuation under different growth, margin, or discount-rate assumptions.
- A user provides historical financials (10-K/10-Q, model tab, or data pull) and wants a forward projection built from them.

## Inputs
- Historical financial statements (revenue, EBITDA, D&A, capex, net working capital) for at least 3-5 years.
- Forecast assumptions: revenue growth rate(s), margin trajectory, tax rate, capex as % of revenue, NWC as % of revenue.
- Capital structure inputs for WACC: cost of equity (via CAPM — risk-free rate, beta, equity risk premium), cost of debt, target capital structure, tax rate.
- Terminal value method preference: Gordon Growth (perpetuity growth rate) or Exit Multiple (EV/EBITDA).
- Shares outstanding, net debt, and any non-operating adjustments (minority interest, preferred, investments) for the equity bridge.

## Process
1. Confirm the forecast horizon (typically 5-10 years) and whether the request is a quick sanity-check model or a full build.
2. Build the unlevered free cash flow bridge: EBIT × (1 - tax rate) + D&A - capex - Δ NWC.
3. Calculate WACC from the capital structure and cost-of-capital inputs; state the formula and each input explicitly rather than asserting a final number.
4. Discount each year's FCF to present value using the WACC.
5. Calculate terminal value using both Gordon Growth and Exit Multiple methods where possible, and reconcile the implied multiples/growth rates against each other as a cross-check.
6. Sum discounted FCFs + discounted terminal value to get enterprise value; bridge to equity value (subtract net debt, minority interest, preferred; add investments/cash as applicable); divide by diluted shares outstanding for value per share.
7. Run a sensitivity table (WACC vs. terminal growth rate, or WACC vs. exit multiple) to show a valuation range rather than a single point estimate.
8. Flag any assumption that materially drives the output (e.g., terminal growth rate near or above long-run GDP growth, WACC below peer averages) so the user can sanity-check it.

## Output format
Present the model as: (1) a summary valuation range and per-share value, (2) the FCF build table by year, (3) the WACC calculation with each input shown, (4) the terminal value cross-check, (5) the sensitivity table. If building in Excel, keep inputs in a clearly labeled assumptions block separate from formulas so the model is auditable.

## Notes / guardrails
- Never present a DCF output as a single "correct" number — always show the sensitivity range.
- Clearly label all assumptions as assumptions, not facts, especially long-term growth and margin assumptions.
- This is analytical output, not investment advice — do not phrase results as a buy/sell recommendation.
