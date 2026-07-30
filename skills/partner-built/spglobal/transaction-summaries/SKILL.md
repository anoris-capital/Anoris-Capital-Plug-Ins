---
name: transaction-summaries
description: Use this skill to summarize M&A and capital markets transactions using S&P Global data. Triggers include "summarize this deal", "give me the details on this transaction", or "pull recent M&A activity in this sector".
---

# Transaction Summaries

## Overview
Summarizes M&A and capital markets transactions using S&P Global deal data: parties involved, deal terms, valuation multiples implied, and strategic rationale, either for a single transaction or a sector-wide activity scan.

## When to use this skill
- A user wants a clear summary of a specific announced or completed transaction.
- A user wants a scan of recent M&A/capital markets activity in a given sector for market-context purposes.

## Inputs
- Specific transaction (parties, announcement date) or sector/time-window for an activity scan.
- Level of detail needed (headline terms only vs. full deal structure and financing detail).

## Process
1. For a single transaction: pull deal terms (consideration type — cash/stock/mix, total value, implied multiples), parties, announcement/close dates, and stated strategic rationale.
2. Calculate implied valuation multiples (EV/EBITDA, EV/Revenue) for the target based on deal terms and available financials, for use as a precedent-transaction data point.
3. For a sector scan: compile recent transactions in the specified window with the same core fields (parties, date, value, implied multiple) in a consistent table format.
4. Note any regulatory or financing conditions attached to the deal that affect certainty of close, where disclosed.
5. Where relevant, connect the transaction(s) to broader sector context (is this part of a consolidation wave, a common buyer type, a recurring multiple range).

## Output format
For a single deal: a structured summary (parties, terms, implied multiples, rationale, status). For a sector scan: a table of recent transactions with consistent fields, usable as precedent-transaction input to other valuation work.

## Notes / guardrails
- Clearly distinguish announced vs. closed transactions, and note any pending regulatory/financing conditions affecting deal certainty.
- Implied multiples should be calculated transparently (show the inputs), not presented as a bare number.
