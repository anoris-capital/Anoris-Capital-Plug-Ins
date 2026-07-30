---
name: rules-grid-evaluation
description: Use this skill to evaluate extracted onboarding/KYC data against the firm's compliance rules grid to identify gaps or exceptions. Triggers include "run this against our rules grid", "check if this onboarding meets our requirements", or "flag any compliance gaps in this file".
---

# Rules Grid Evaluation

## Overview
Evaluates structured KYC/onboarding data (typically from the kyc-document-parsing skill) against the firm's defined compliance rules grid — the set of required fields, conditions, and thresholds an onboarding file must satisfy — and flags gaps or exceptions.

## When to use this skill
- Extracted onboarding data needs to be checked against the firm's specific compliance requirements.
- A user needs to know whether a file is ready for compliance sign-off or has open gaps.
- A user needs a documented rationale for why a file passed or failed specific rules-grid criteria.

## Inputs
- The extracted onboarding/KYC data (field-by-field, ideally from kyc-document-parsing).
- The firm's rules grid: required fields, conditional requirements (e.g., additional documentation triggered by jurisdiction or entity type), and any risk-based thresholds.

## Process
1. Map each extracted data field to its corresponding rules-grid requirement.
2. For each requirement, determine pass/fail/not-applicable based on the extracted data.
3. Apply conditional logic correctly — e.g., additional beneficial ownership documentation requirements that only trigger for certain entity types or high-risk jurisdictions.
4. Compile a clear list of any failed or incomplete requirements, each with a plain-language explanation of what's missing or non-compliant.
5. Note any requirements that couldn't be evaluated due to ambiguous or missing source data, distinct from a confirmed failure.
6. Summarize overall file status: fully compliant, compliant with noted exceptions, or gaps requiring remediation before proceeding.

## Output format
A rules-grid evaluation report: requirement, status (pass/fail/N/A/unable to evaluate), and explanation for any non-pass items, plus an overall file status summary.

## Notes / guardrails
- This tool applies the firm's stated rules mechanically and flags results for human compliance review — it does not substitute for a compliance officer's judgment or override on edge cases.
- Distinguish clearly between a confirmed rule failure and a case where source data was simply insufficient to evaluate.
