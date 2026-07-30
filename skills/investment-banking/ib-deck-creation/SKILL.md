---
name: ib-deck-creation
description: Use this skill to draft and format investment banking pitch decks and client presentation materials. Triggers include "build a pitch deck for [client]", "put together a deal update deck", or "format this into a banker deck".
---

# Deck Creation (Investment Banking)

## Overview
Drafts and formats banker-style presentation materials — pitch books, deal update decks, board materials — following standard IB deck conventions: executive summary up front, clear section structure, consistent formatting, and appendix-level supporting detail.

## When to use this skill
- A user needs a new pitch deck built from underlying analysis (comps, financial analysis, market data).
- A user has rough content/bullet points that need to be structured into a polished deck.
- A user needs an existing deck reformatted to house style or updated with new figures.

## Inputs
- Purpose of the deck (new business pitch, deal update, board materials, financing proposal) and audience.
- Underlying content/analysis to include (financial analysis, comps, market data, transaction structure).
- House style/template conventions (branding, color palette, font, standard disclaimer/footnote language) if available.

## Process
1. Confirm the deck's purpose and audience — this determines structure (e.g., a new-business pitch leads with credentials and market context; a deal update leads with status and next steps).
2. Draft the structure first as a slide-by-slide outline before building content, so the narrative flow is confirmed up front.
3. Lead with an executive summary slide that states the key message/ask in a few bullets.
4. Build body sections with one clear takeaway per slide (a slide title should be a sentence-level claim, not just a topic label, per standard banker convention).
5. Push detailed backup data (full model outputs, detailed comps tables) to an appendix, keeping body slides focused on the key numbers/conclusions.
6. Apply consistent formatting throughout: number formatting, chart styles, color usage, footnote/source conventions.
7. Run a final consistency pass (or hand off to the deck-qc skill) before considering the deck final.

## Output format
A structured slide deck (or slide-by-slide content plan if building outside a native tool) with an executive summary, clearly organized body sections, and an appendix for supporting detail.

## Notes / guardrails
- Slide titles should state a conclusion/takeaway, not just describe the topic — this is a core banker-deck convention.
- Keep body slides focused; route dense supporting data to the appendix.
- Pair with the deck-qc skill for a final numerical/formatting check before the deck is sent.
