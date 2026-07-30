---
name: gl-reconciler
description: End-to-end agent that finds GL reconciliation breaks, traces their root cause, and routes them for sign-off. Triggers include "run the full GL reconciliation for this period" or "reconcile and resolve breaks for month-end".
---

# GL Reconciler

## Overview
An end-to-end workflow agent that runs the full reconciliation cycle: identifies breaks between the GL and source systems, investigates root cause for each, and routes resolved/unresolved items for the appropriate sign-off — rather than requiring each step to be run separately.

## When to use this skill
- A period-end close requires a full reconciliation cycle run start to finish.
- A user wants breaks not just identified but investigated and routed, in one pass.

## Process
1. Run the gl-reconciliation workflow to identify all breaks between the GL and source records for the period.
2. For each break identified, run the break-tracing workflow to determine root cause where possible.
3. Categorize each break by resolution status: resolved with a clear corrective action identified, or unresolved/needs further investigation.
4. Route resolved breaks with their proposed corrective entries to the appropriate owner for approval/posting.
5. Escalate unresolved breaks clearly, with whatever partial investigation detail is available, rather than letting them sit unflagged.
6. Produce a period-end reconciliation summary: total breaks found, resolved vs. outstanding, and sign-off status.

## Output format
A full reconciliation report: break listing with root cause and resolution status for each, a routing/owner assignment for open items, and an overall period sign-off status.

## Notes / guardrails
- Unresolved breaks must be clearly escalated, not quietly left in a report for someone to notice later.
- Proposed corrective entries require human approval before posting — this agent prepares and routes, it does not post GL entries itself.
