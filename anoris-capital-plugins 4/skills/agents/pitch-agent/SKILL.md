---
name: pitch-agent
description: End-to-end agent that takes a company/deal thesis through comps, precedent transactions, and an LBO, and assembles the output into a branded pitch deck. Triggers include "build me a full pitch for [company]" or "run the whole pitch workflow end to end".
---

# Pitch Agent

## Overview
An end-to-end workflow agent that chains together the individual analytical skills — trading comps, precedent transactions analysis, and an LBO model — and assembles the results into a branded, client-ready pitch deck, rather than requiring each step to be run and handed off manually.

## When to use this skill
- A user wants a full pitch built from scratch given just a target company/thesis, without managing each analytical step individually.
- A user needs a fast turnaround on a complete pitch package (analysis + deck) rather than piecemeal outputs.

## Process
1. Confirm the target company, the pitch purpose/angle, and the audience.
2. Run the trading-comps workflow to establish public market valuation context.
3. Pull or build precedent transaction comparables for the sector, where available, to add an M&A-multiple perspective.
4. Run the lbo-model workflow to assess sponsor-return feasibility if relevant to the pitch angle.
5. Feed all outputs into the ib-deck-creation workflow, building a structured deck: executive summary, valuation summary (comps + precedents + LBO triangulation), and appendix-level detail for each analysis.
6. Run the deck-qc workflow as a final pass before presenting the completed deck to the user.
7. Present the assembled deck along with the underlying analysis so the user can verify every number before it goes to a client.

## Output format
A complete, formatted pitch deck plus the underlying analytical detail (comps table, precedent transaction table, LBO summary) as backup, with a final QC pass already applied.

## Notes / guardrails
- This agent orchestrates the underlying skills — always surface the individual analytical outputs (not just the final deck) so the user can verify the work.
- Flag any step where data was insufficient to complete a full analysis (e.g., thin precedent transaction set) rather than silently producing a weaker output without comment.
