---
name: month-end-closer
description: End-to-end agent that handles accruals, roll-forwards, and variance commentary for month-end close. Triggers include "run our month-end close workflow" or "close the books for this period end to end".
---

# Month-End Closer

## Overview
An end-to-end workflow agent that runs the core month-end fund accounting close sequence: calculating accruals, building roll-forward schedules, and drafting variance commentary — chaining these into one close-ready package.

## When to use this skill
- A period-end close needs the standard accrual, roll-forward, and commentary steps run together.
- A user wants a consolidated close package rather than running each step separately and assembling manually.

## Process
1. Run the accruals workflow to calculate and true-up all relevant period accruals (management fees, performance fees, expenses, interest).
2. Run the roll-forwards workflow to build the NAV and/or investor capital account roll-forward for the period, incorporating the accruals just calculated.
3. Run the variance-commentary workflow to draft explanations for any significant period-over-period changes surfaced by the roll-forward.
4. Assemble the full close package: accrual schedule, roll-forward schedules (fund and investor level), and variance commentary, checked for internal consistency (e.g., the fee figures in the roll-forward should match the accrual schedule).
5. Flag anything that didn't tie out cleanly (route to gl-reconciliation/break-tracing) rather than presenting the close package as final if open items remain.

## Output format
A consolidated month-end close package: accrual schedule, roll-forward schedules, and variance commentary, with any unresolved items clearly flagged rather than glossed over.

## Notes / guardrails
- Internal consistency across the three components (accruals, roll-forwards, commentary) is the key check — the same figures should match everywhere they appear.
- This agent prepares the close package; final review and sign-off remain with fund accounting/controller staff.
