---
name: lbo-model
description: Use this skill to build a leveraged buyout (LBO) model to assess whether a company is an attractive private-equity acquisition target and what returns a financial sponsor could expect. Triggers include "build an LBO", "what IRR could a sponsor get on this deal", or "model a buyout of [company]".
---

# LBO Model

## Overview
Models a leveraged buyout: sets an entry valuation and capital structure (debt + equity), projects operating performance and debt paydown over a hold period, and calculates sponsor returns (IRR and MOIC) at a range of exit assumptions.

## When to use this skill
- A user wants to assess whether a company could support a leveraged acquisition and what returns it might generate.
- A user wants to test how leverage, entry multiple, or operational improvement assumptions affect returns.
- A user is prepping for a PE process (auction, take-private, add-on) and needs a base-case return model.

## Inputs
- Entry assumptions: purchase price/entry multiple (EV/EBITDA), transaction fees, and sources & uses of funds.
- Capital structure: leverage level (Debt/EBITDA), tranche structure (senior debt, subordinated debt, mezzanine), interest rates, and mandatory amortization schedules.
- Operating projections: revenue growth, margin trajectory, capex, and working capital needs over the hold period (typically 3-7 years).
- Exit assumptions: hold period and exit multiple (often assumed equal to or below entry multiple as a conservative base case).
- Any planned operational value-creation levers (cost cuts, pricing, add-on M&A) the sponsor is underwriting to.

## Process
1. Build the sources & uses table: uses = purchase price + fees + refinanced debt; sources = new debt tranches + sponsor equity (the plug).
2. Project the operating model (revenue through EBITDA through unlevered free cash flow) over the hold period.
3. Build the debt schedule: apply mandatory amortization and cash sweep (excess FCF paying down debt) tranche by tranche, calculating interest expense on the outstanding balance each period.
4. Roll forward to exit-year EBITDA and apply the exit multiple to get exit enterprise value; subtract remaining net debt to get exit equity value.
5. Calculate sponsor returns: IRR and multiple on invested capital (MOIC) based on initial equity check and exit equity proceeds.
6. Sensitize returns across entry multiple, exit multiple, leverage level, and hold period to show a return range, not a single output.
7. Flag credit risk: minimum cash covenant headroom, interest coverage ratio, and whether leverage assumptions look aggressive relative to the company's cash flow stability.

## Output format
Present: (1) sources & uses, (2) summary base-case returns (IRR/MOIC) with a sensitivity grid, (3) the debt paydown schedule, (4) key credit metrics by year, (5) a short narrative on what has to go right (or wrong) for the deal to hit target returns.

## Notes / guardrails
- Always show a return sensitivity range, not a single IRR figure.
- Be explicit about leverage assumptions and covenant risk — do not understate downside/credit risk in a base case.
- This is analytical modeling output, not a recommendation to execute a transaction.
