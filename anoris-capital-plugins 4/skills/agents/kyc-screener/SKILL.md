---
name: kyc-screener
description: End-to-end agent that parses onboarding documents, runs them through the compliance rules engine, and flags gaps. Triggers include "run this new client file through KYC end to end" or "screen this onboarding packet fully".
---

# KYC Screener

## Overview
An end-to-end workflow agent that takes a raw onboarding/KYC document packet, extracts the structured data, evaluates it against the firm's compliance rules grid, and produces a consolidated gap report — chaining document parsing and rules evaluation into one pass.

## When to use this skill
- A new client/investor file needs full KYC screening from raw documents to a compliance-ready gap report.
- A user wants the parsing and rules-evaluation steps run together rather than handled as separate manual steps.

## Process
1. Run the kyc-document-parsing workflow on the provided onboarding documents to extract structured data fields.
2. Run the rules-grid-evaluation workflow on the extracted data against the firm's compliance rules grid.
3. Consolidate the results into a single gap report: what was extracted, what passed, what failed, and what couldn't be evaluated due to missing/unclear source data.
4. Prioritize gaps by severity/blocking status — distinguish a hard compliance blocker from a minor documentation gap.
5. Present the consolidated report to the compliance reviewer for final sign-off, clearly marked as a screening aid rather than a final determination.

## Output format
A consolidated screening report: extracted data summary, rules-grid pass/fail results, and a prioritized gap list ready for compliance review and remediation follow-up.

## Notes / guardrails
- This agent screens and flags; final compliance determinations and approvals remain with the compliance officer.
- Never silently treat an "unable to evaluate" item as a pass — it must be flagged distinctly from a confirmed pass.
