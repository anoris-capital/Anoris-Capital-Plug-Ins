---
name: gl-reconciliation
description: Use this skill to reconcile general ledger entries against source systems (fund administrator records, custodian statements, trading systems). Triggers include "reconcile the GL for this period", "check the GL against the admin statement", or "find breaks between the GL and custody".
---

# GL Reconciliation

## Overview
Reconciles the general ledger against independent source records (fund administrator NAV packages, custodian statements, trading blotters) to confirm balances match, and identifies any breaks for investigation.

## When to use this skill
- A period-end close requires the GL to be reconciled against admin/custodian records before finalizing.
- A user wants to confirm cash, position, or P&L balances tie out across systems.
- A user needs a reconciliation report showing matched and unmatched items.

## Inputs
- GL trial balance or relevant account detail for the period.
- Corresponding source records: fund administrator statement, custodian statement, trading system records.
- Prior period reconciliation status, if relevant, for continuity.

## Process
1. Identify the accounts/balances in scope for reconciliation (cash, positions, P&L, fees, etc.).
2. Match GL balances against the corresponding source record balance for each account.
3. Flag any variance as a break, and categorize the likely cause where identifiable (timing difference, booking error, FX/pricing difference, missing entry).
4. Quantify each break in currency terms and note whether it's within an acceptable tolerance threshold or requires investigation (route unresolved breaks to the break-tracing skill).
5. Summarize the reconciliation: total accounts reconciled, number and value of breaks, and overall reconciliation status (clean/breaks pending).
6. Note any recurring break patterns across periods that may indicate a systemic process issue rather than a one-off error.

## Output format
A reconciliation summary (accounts in scope, matched/unmatched, total break value) plus a detailed break listing (account, GL balance, source balance, variance, likely cause) for anything unresolved.

## Notes / guardrails
- Do not mark a reconciliation "clean" if unexplained variances remain, even small ones — flag them explicitly with their size and status.
- Distinguish confirmed root causes from hypotheses — label unconfirmed explanations as such.
