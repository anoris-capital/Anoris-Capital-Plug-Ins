---
name: deck-qc
description: Use this skill to quality-check a financial or client deck before it goes out — catching formatting errors, formula/number inconsistencies, broken links between slides and supporting models, and typos. Triggers include "QC this deck", "check this presentation before I send it", or "proofread this pitch book".
---

# Deck QC

## Overview
Performs a structured quality-control pass on a financial presentation (pitch deck, board deck, IC memo deck) to catch the kinds of errors that are common and costly in finance decks: numbers that don't tie to the source model, inconsistent formatting, stale data, and typos.

## When to use this skill
- A deck is about to go to a client, committee, or external counterparty and needs a final check.
- A user has updated a model and needs to confirm every number and chart in the deck reflects the update.
- A user wants a second pass specifically for consistency and error-catching, separate from content/narrative review.

## Inputs
- The deck itself (or exported slide content) and, where available, the underlying model(s)/data sources it's built from.
- Any house style guide (fonts, number formatting, color palette, footnote/disclaimer conventions) to check against.

## Process
1. Cross-check every hard number in the deck against its source model or data file — flag any mismatch, even small rounding differences that suggest a stale link.
2. Check internal consistency: does the same metric (e.g., revenue, EBITDA margin) match across every slide it appears on?
3. Check formatting consistency: consistent number formatting (decimals, $ vs. %, units in millions vs. billions stated clearly), consistent fonts/colors/logo usage, consistent footnote and source citation style.
4. Check dates and "as of" labels — flag anything that looks stale relative to the rest of the deck.
5. Spell-check and grammar-check all text, including chart labels and footnotes, which are often missed in review.
6. Check slide-to-slide logical flow — does the narrative sequence make sense, and are transitions/agenda references accurate (e.g., a table of contents that doesn't match actual slide order)?
7. Compile findings as a punch list organized by slide number, categorized by severity (must-fix numerical error vs. minor formatting nit).

## Output format
A slide-by-slide punch list of issues found, with severity flags, so the user can triage before send. For numerical discrepancies, show both the deck value and the source-model value side by side.

## Notes / guardrails
- Numerical/data discrepancies are always high severity — surface these first, separate from cosmetic issues.
- This is a QC pass, not a content/strategy review — flag content concerns separately if noticed, but don't let them distract from the core error-catching job.
