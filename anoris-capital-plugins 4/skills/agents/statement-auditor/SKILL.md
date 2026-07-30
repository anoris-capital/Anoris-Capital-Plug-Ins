---
name: statement-auditor
description: End-to-end agent that audits pre-generated LP statements before distribution. Triggers include "audit these LP statements before we send them" or "do a final check on this quarter's investor statements".
---

# Statement Auditor

## Overview
An end-to-end workflow agent that performs a final, comprehensive audit of pre-generated LP (limited partner) statements before they're distributed to investors — checking figures tie to source records, formatting is consistent, and required disclosures are present.

## When to use this skill
- LP statements have been generated for a reporting period and need a final audit pass before distribution.
- A user wants a second, independent check on investor-facing statements given the high cost of errors in this document type.

## Process
1. Cross-check every figure on each LP statement against the underlying source records (roll-forward schedules, NAV tie-out results, accrual schedules) — treat any discrepancy as a blocking issue.
2. Confirm each investor's capital account statement ties to the fund-level roll-forward per their ownership percentage.
3. Check formatting and template consistency across all statements (same period, same fund) — inconsistent formatting across investor statements is a red flag for a template or data-pull error.
4. Confirm all required disclosures, disclaimers, and fee transparency language are present per house policy and any applicable regulatory requirement.
5. Compile an audit exceptions list — any statement with a discrepancy or missing element — and hold those out from the distribution-ready batch.
6. Confirm the remaining batch is clean and ready for distribution, explicitly separating "ready to send" from "needs correction."

## Output format
An audit report: statements checked, any exceptions found (with detail), and a clear final status per statement (ready to distribute / needs correction).

## Notes / guardrails
- This is the last control point before investor-facing documents go out — treat any unresolved discrepancy as blocking, not a minor note.
- Do not clear a statement with an unexplained numerical discrepancy, however small.
