---
name: accruals
description: Use this skill to calculate and book periodic accruals for fund administration close processes. Triggers include "calculate this period's accruals", "book the management fee accrual", or "true up accrued expenses for the month".
---

# Accruals

## Overview
Calculates periodic accruals (management fees, incentive/performance fees, fund expenses, interest income/expense) needed to properly state the fund's financials for a period, and prepares them for booking.

## When to use this skill
- A period-end close requires accruals to be calculated and booked.
- A user needs to true up an existing accrual against actual invoiced amounts.
- A user needs a schedule of all accrual types and their current balances for review.

## Inputs
- Fee schedules (management fee rate/basis, performance fee terms/hurdle) and the NAV/basis they apply to.
- Known recurring expenses (audit, legal, admin fees) and their typical accrual pattern.
- Actual invoices received during the period, for true-up against prior accruals.
- Interest rate and balance information for interest income/expense accruals, if applicable.

## Process
1. Identify all accrual categories relevant to the period: management fees, performance/incentive fees, fund operating expenses, interest income/expense, and any other recurring items.
2. Calculate each accrual per its governing terms (e.g., management fee = rate × NAV basis × period fraction; performance fee per the fund's specific waterfall/hurdle terms).
3. Compare current-period accruals against any actual invoices received and true up prior estimated accruals to actual amounts, noting the adjustment.
4. Summarize the full accrual schedule: category, basis/calculation, current period amount, cumulative balance.
5. Flag anything unusual: a fee calculation that deviates from the standard formula, an invoice that doesn't match the expected accrual, or a stale accrual that hasn't been trued up in some time.

## Output format
An accrual schedule by category showing the calculation basis, current-period amount, and running balance, with true-up adjustments called out separately from new-period accruals.

## Notes / guardrails
- Show the calculation, not just the result, so accruals can be independently checked against fee/expense agreements.
- Flag any accrual that hasn't been trued up against actual invoices in a while, since estimated accruals can drift from actuals over time.
