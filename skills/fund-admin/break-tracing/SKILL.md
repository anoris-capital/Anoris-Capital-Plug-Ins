---
name: break-tracing
description: Use this skill to trace a reconciliation break to its root cause. Triggers include "trace this break", "why doesn't this balance match", or "find the source of this discrepancy".
---

# Break Tracing

## Overview
Investigates an identified reconciliation break (from GL reconciliation or NAV tie-out) to determine its root cause — a timing difference, a booking error, a pricing/FX discrepancy, or a missing/duplicated entry — so it can be corrected and signed off.

## When to use this skill
- A break has been identified (via gl-reconciliation or nav-tie-out) and needs root-cause investigation.
- A user wants to understand why two records that should match don't.
- A user needs a documented explanation of a break for sign-off/audit purposes.

## Inputs
- The specific break: accounts/records involved, the variance amount, and the period it relates to.
- Access to underlying transaction detail from both sides of the discrepancy (GL entries, source system records, trade tickets, pricing sources).
- Historical context — has this break appeared before, and if so, how was it resolved.

## Process
1. Isolate the specific transactions or entries driving the variance rather than working at the account-balance level alone.
2. Check for common root causes in order of likelihood: timing differences (trade date vs. settlement date), duplicate or missing entries, pricing/FX rate discrepancies, incorrect account/category mapping, or manual booking errors.
3. Trace each side of the discrepancy back to its originating document (trade confirmation, invoice, statement line) to confirm which side is correct.
4. Determine the correcting action needed (which system needs the adjusting entry) and who owns making it.
5. Document the root cause and resolution clearly enough to support an audit trail and sign-off.
6. Note if the same root cause has recurred across periods — this may indicate a process fix is needed rather than a one-off correction.

## Output format
A break investigation summary: break description, root cause identified, supporting evidence/trace detail, corrective action needed, and owner. Flag if root cause could not be conclusively determined.

## Notes / guardrails
- Do not close out a break with an unconfirmed or speculative explanation — state clearly when root cause is confirmed vs. probable.
- Recommend the correcting entry and owner, but the actual GL posting/adjustment should go through the firm's normal approval process.
