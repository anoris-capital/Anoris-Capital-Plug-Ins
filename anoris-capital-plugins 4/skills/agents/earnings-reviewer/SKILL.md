---
name: earnings-reviewer
description: End-to-end agent that takes an earnings call and filings and produces a model update plus a draft research note. Triggers include "process this earnings release end to end" or "update our model and draft the note off this print".
---

# Earnings Reviewer

## Overview
An end-to-end workflow agent that takes a company's new earnings release and filings, analyzes the results, updates the underlying financial model with actuals and any revised guidance, and drafts a research note summarizing the update.

## When to use this skill
- A covered company just reported and the full workflow (analysis → model update → note draft) needs to run, not just the analysis step.
- A user wants the model and the note kept in sync automatically off a new print rather than updating each manually.

## Process
1. Run the earnings-analysis workflow on the new release/transcript to extract results vs. expectations and updated guidance.
2. Update the three-statement-model (and DCF/comps outputs downstream of it, if maintained) with actuals for the reported period and revised forward assumptions based on new guidance.
3. Re-run valuation outputs affected by the model update (e.g., dcf-model, trading-comps) so the price target/valuation view reflects the new numbers.
4. Draft a research note summarizing: what happened, what changed in the model/estimates, and whether the update changes the thesis, rating, or price target.
5. Present the updated model, the valuation outputs, and the draft note together so the user can review consistency across all three before anything is finalized or published.

## Output format
An updated model (or clear summary of what changed in it), updated valuation output, and a draft research note ready for analyst review.

## Notes / guardrails
- Flag any assumption changes made to the model as a result of the earnings update explicitly, so the analyst can confirm before the note is finalized.
- Do not publish or finalize a note automatically — this agent prepares a draft for human review and sign-off.
