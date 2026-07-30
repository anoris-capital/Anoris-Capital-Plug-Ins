---
name: model-builder
description: End-to-end agent that builds DCF, LBO, three-statement, or comps models live in Excel. Triggers include "build this model directly in Excel for me" or "set up a live LBO model in a spreadsheet".
---

# Model Builder

## Overview
An end-to-end workflow agent that builds financial models (DCF, LBO, three-statement, trading comps) directly as live, formula-driven Excel workbooks rather than static output — so the user gets an editable, auditable model file, not just a description of one.

## When to use this skill
- A user needs an actual working spreadsheet, not just modeled output described in chat.
- A user wants a model built with live formulas so they can flex assumptions themselves afterward.

## Process
1. Confirm which model type is needed (dcf-model, lbo-model, three-statement-model, or trading-comps) and gather the required inputs per that skill's specification.
2. Build the workbook with a clear structure: a dedicated assumptions/inputs tab, calculation tabs, and a summary/output tab — never bury inputs inside formulas on calculation tabs.
3. Use live formulas (not hard-coded values) for everything derived from the assumptions, so changing an input flows through the whole model.
4. Include the relevant integrity checks for the model type (balance-sheet balance check for three-statement models, sources-and-uses tie-out for LBOs, sensitivity tables for DCFs).
5. Format the workbook cleanly: consistent number formatting, clearly labeled tabs, and inputs visually distinguished from formulas (e.g., by color convention) per standard modeling practice.
6. Deliver the finished workbook file along with a short summary of its structure and key outputs.

## Output format
A live Excel workbook file implementing the requested model, with a clearly separated assumptions tab, calculation tabs, and a summary output tab, plus a short narrative summary of the build.

## Notes / guardrails
- Inputs must be hard-coded values in a clearly labeled assumptions area; everything else should be a formula — this is the standard that makes a model actually usable and auditable.
- Include the relevant integrity/tie-out checks for the model type so errors are visible rather than hidden.
