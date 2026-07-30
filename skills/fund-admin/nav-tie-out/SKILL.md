---
name: nav-tie-out
description: Use this skill to tie out an internally calculated NAV against the fund administrator's official NAV records. Triggers include "tie out this month's NAV", "check our NAV against the admin's number", or "confirm the NAV before we release it".
---

# NAV Tie-Out

## Overview
Confirms that the fund's net asset value, as calculated internally, matches the fund administrator's official NAV package before it's released to investors — a critical control step in the fund reporting cycle.

## When to use this skill
- Before releasing monthly/quarterly NAV to investors, as a final control check.
- When an internal NAV calculation needs to be validated against the administrator's records.
- When investigating a reported discrepancy between internal and administrator NAV figures.

## Inputs
- Internally calculated NAV (from the fund's books and records).
- The fund administrator's official NAV package for the same period.
- Supporting detail for both (position-level valuations, cash balances, accrued fees/expenses) to enable a component-level comparison, not just a top-line check.

## Process
1. Compare the top-line NAV figure from internal records against the administrator's package — confirm whether they match within an acceptable tolerance.
2. If they don't match (or as a standard control even if they do), compare at the component level: position valuations, cash balances, accrued income/expenses, and fee accruals.
3. Identify which component(s) are driving any variance and quantify each.
4. Route any unresolved variance to the break-tracing skill for root-cause investigation.
5. Confirm sign-off status: NAV should not be released to investors until the tie-out is clean or any variance is explained and deemed immaterial per house policy.

## Output format
A tie-out summary: internal NAV vs. administrator NAV, component-level comparison, any variances identified with their size, and a clear statement of whether the NAV is cleared for release.

## Notes / guardrails
- This is a release-gating control — be explicit and unambiguous about whether the tie-out passed or has open items, since investor-facing NAV release depends on it.
- Do not clear a NAV for release with unexplained material variances outstanding.
