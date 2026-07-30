---
name: three-statement-model
description: Use this skill to build or maintain an integrated three-statement financial model (income statement, balance sheet, cash flow statement) that ties together dynamically. Triggers include "build a three-statement model", "project the balance sheet", or "make sure this model ties out".
---

# Three-Statement Model

## Overview
Builds an integrated financial model in which the income statement, balance sheet, and cash flow statement are dynamically linked, so that a change in any one assumption flows correctly through all three statements and the balance sheet balances every period.

## When to use this skill
- A user needs a foundational operating model to feed into a DCF, LBO, or budgeting exercise.
- A user has disconnected or "hard-coded" statements that don't tie out and needs them properly linked.
- A user wants to project financial statements forward based on historical actuals and stated assumptions.

## Inputs
- Historical income statement, balance sheet, and cash flow statement (ideally 3+ years).
- Forecast assumptions: revenue growth, cost ratios, capex, depreciation schedule, working capital assumptions (days sales outstanding, days inventory, days payable), debt terms, dividend/buyback policy.
- Tax rate and any deferred tax considerations.

## Process
1. Project the income statement first: revenue → gross profit → operating expenses → EBIT → interest → tax → net income, driven by the stated assumptions.
2. Build the supporting schedules: working capital (linked to revenue/COGS via day-ratios), capex and depreciation (PP&E roll-forward), and debt (roll-forward with interest tied to the average or beginning balance).
3. Build the cash flow statement from the income statement and balance sheet changes: net income + D&A +/- working capital changes - capex +/- financing activities = net change in cash.
4. Build the balance sheet by rolling forward each line item (assets, liabilities, equity) using the corresponding schedule, with cash as the balancing plug tied to the cash flow statement's ending cash balance.
5. Confirm the balance sheet actually balances (assets = liabilities + equity) in every forecast period — this is the core integrity check of the model.
6. Add a circularity check/switch if using a cash sweep or interest-on-average-debt-balance (common source of circular references) so the model doesn't break.
7. Stress-test with at least one alternate scenario (e.g., lower growth, higher costs) to confirm the linkages hold under different assumptions.

## Output format
The three linked statements (historical + forecast periods), the supporting schedules (working capital, PP&E, debt), and an explicit balance-check row showing assets minus liabilities-and-equity equals zero in every period.

## Notes / guardrails
- The balance-check row is non-negotiable — never deliver a "three-statement model" where the balance sheet doesn't actually balance.
- Keep assumptions in a clearly separated input block, not buried in formulas, so the model is auditable and easy to update.
