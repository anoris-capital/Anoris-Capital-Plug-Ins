---
name: roll-forwards
description: Use this skill to build capital account and NAV roll-forward schedules for fund reporting. Triggers include "build the capital roll-forward", "roll forward NAV for this period", or "update the investor capital account schedule".
---

# Roll-Forwards

## Overview
Builds roll-forward schedules that walk a balance (fund NAV, an individual investor's capital account) from its beginning-of-period value to its end-of-period value through all the activity that occurred — contributions, distributions, P&L, fees.

## When to use this skill
- A period-end close or investor reporting cycle requires a NAV or capital account roll-forward.
- A user needs to reconcile why a balance changed from one period to the next, broken into its components.
- A user needs individual investor capital account statements built from fund-level activity.

## Inputs
- Beginning-of-period balance (fund NAV or investor capital account balance).
- All activity during the period: contributions/subscriptions, distributions/redemptions, realized and unrealized P&L, management and performance fees, fund expenses.
- Investor-level allocation percentages/ownership, if building investor-level roll-forwards.

## Process
1. Establish the beginning balance for the period (should tie to the prior period's ending balance — flag if it doesn't).
2. Lay out each roll-forward component in a standard order: beginning balance, plus contributions, less distributions, plus/minus P&L (realized and unrealized), less fees and expenses, equals ending balance.
3. For investor-level roll-forwards, allocate fund-level P&L and fees pro-rata (or per the specific allocation methodology in the fund's governing documents) to each investor's capital account.
4. Confirm the sum of all investor-level ending balances ties to the fund-level ending NAV.
5. Flag any component that looks unusual relative to prior periods (e.g., an unexpectedly large expense allocation) for review before finalizing.

## Output format
A roll-forward schedule showing beginning balance through each component to ending balance, at the fund level and/or investor level as requested, with a tie-out check confirming investor-level sums match the fund total.

## Notes / guardrails
- Always include the tie-out check between investor-level roll-forwards and the fund-level total — this is the core integrity check of the schedule.
- Follow the fund's actual governing-document allocation methodology for P&L/fee allocation rather than assuming simple pro-rata if the terms specify otherwise.
