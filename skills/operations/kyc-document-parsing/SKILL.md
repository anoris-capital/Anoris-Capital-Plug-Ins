---
name: kyc-document-parsing
description: Use this skill to extract structured data from KYC and client onboarding documents. Triggers include "parse this KYC packet", "extract the details from this onboarding document", or "pull the entity information from this subscription document".
---

# KYC Document Parsing

## Overview
Extracts structured data fields (entity information, beneficial ownership, identification documents, source-of-funds information) from KYC and onboarding documents so they can be evaluated against compliance requirements.

## When to use this skill
- A new client/investor onboarding packet needs its data extracted into a structured format.
- A user needs specific fields (entity name, jurisdiction, beneficial owners, ID numbers) pulled from a set of onboarding documents.
- A user needs onboarding documents checked for completeness before compliance review.

## Inputs
- The onboarding/KYC documents themselves (subscription documents, entity formation documents, beneficial ownership certifications, identification documents).
- The list of required fields per the firm's KYC standard/rules grid (to know what to extract and what "complete" looks like).

## Process
1. Identify the document type(s) provided (individual vs. entity onboarding, which jurisdiction's standard forms).
2. Extract the required structured fields: legal name, entity type/jurisdiction, registered address, beneficial ownership details (name, %, nationality), identification document details, source of funds/wealth narrative.
3. Cross-check extracted data for internal consistency (e.g., ownership percentages summing correctly, names matching across documents).
4. Flag missing required fields or documents explicitly rather than leaving gaps unnoted.
5. Flag anything that looks like a data quality issue (illegible scan, inconsistent name spelling across documents, expired ID) for human review.
6. Output the extracted data in a structured format ready for the rules-grid-evaluation skill or direct compliance review.

## Output format
A structured field-by-field extraction (field name, extracted value, source document), with a clear completeness flag section listing any missing or unclear items.

## Notes / guardrails
- Never fill in a missing field with an inferred or assumed value — mark it explicitly as missing/unclear.
- This tool extracts and organizes data; it does not make the compliance determination itself (that's the rules-grid-evaluation skill and, ultimately, compliance/legal judgment).
