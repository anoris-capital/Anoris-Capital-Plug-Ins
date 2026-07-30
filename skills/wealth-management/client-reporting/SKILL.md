---
name: client-reporting
description: Use this skill to generate client-facing performance and account reports for wealth management clients. Triggers include "generate this client's quarterly statement summary", "build our client reporting package", or "prepare the performance report for [client]".
---

# Client Reporting

## Overview
Generates client-facing reports summarizing account performance, holdings, transactions, and fees for a given reporting period, formatted for direct client delivery.

## When to use this skill
- A periodic (monthly/quarterly/annual) client report needs to be generated.
- A user needs an ad hoc performance summary for a client request.
- A user needs to verify a report's figures reconcile to the underlying account data before it goes out.

## Inputs
- Account holdings, transactions, and performance data for the reporting period.
- Fee schedule and any fees charged during the period.
- House report template/format conventions and required disclosures.

## Process
1. Pull account holdings, transactions, and performance figures for the reporting period from the source system.
2. Calculate period performance (time-weighted or money-weighted return as per house convention) and compare to the relevant benchmark.
3. Summarize transactions during the period (contributions, withdrawals, buys/sells) in client-friendly language.
4. Calculate and clearly disclose fees charged during the period.
5. Assemble the report in the house template format, including all required regulatory disclosures and disclaimers.
6. Cross-check all figures in the report against the source account data before finalizing — treat this like a QC pass, since these numbers go directly to clients.

## Output format
A client-ready report following house template conventions: performance summary, holdings detail, transaction summary, fee disclosure, and required regulatory disclaimers.

## Notes / guardrails
- Every figure in a client report must tie to source account data — this is a compliance-sensitive document, not a draft for internal discussion.
- Required disclosures/disclaimers must be present per house and regulatory policy; do not omit them for brevity.
