---
name: meeting-prep-agent
description: End-to-end agent that assembles a full briefing pack before a client meeting. Triggers include "prep me for my meeting with [client]" or "build my briefing pack for tomorrow's call".
---

# Meeting Prep Agent

## Overview
An end-to-end workflow agent that assembles a complete briefing pack ahead of a client meeting: client/market intelligence, relevant portfolio or deal status, and a suggested agenda/talking points, pulling from calendar, CRM, and portfolio/deal data where connected.

## When to use this skill
- A client meeting is coming up and the user wants a single, complete briefing pack rather than assembling pieces manually.
- A user wants meeting prep automated ahead of recurring client touchpoints.

## Process
1. Identify the meeting: who it's with, when, and its stated purpose (from calendar context if available, or as provided by the user).
2. Run the client-market-insights workflow to pull recent news/developments on the client or counterparty.
3. Pull relevant internal context: current portfolio/account status (for wealth management), deal/relationship status (for banking/PE), or CRM notes from the last interaction.
4. Identify open items or follow-ups from the last meeting/interaction that should be addressed.
5. Assemble a suggested agenda and talking points based on the above, prioritized by what's most relevant/time-sensitive.
6. Present the full pack: client/market brief, internal status summary, open follow-ups, and suggested agenda.

## Output format
A single briefing pack document: meeting context, client/market intelligence summary, internal status recap, outstanding follow-ups, and a suggested agenda/talking points list.

## Notes / guardrails
- Clearly label information pulled from external/public sources vs. internal systems (CRM, portfolio data) so the user knows provenance.
- If a needed data source (CRM, calendar, portfolio system) isn't connected, say so rather than silently omitting that section.
