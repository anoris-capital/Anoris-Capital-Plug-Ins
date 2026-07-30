---
name: crm-integration
description: Use this skill to sync deal, contact, and pipeline data with the firm's CRM system. Triggers include "log this into the CRM", "update the pipeline tracker", or "pull our current deal pipeline from the CRM".
---

# CRM Integration

## Overview
Keeps deal and contact data synchronized with the firm's CRM — logging new contacts/companies, updating deal stage and status, and pulling current pipeline views for reporting or team review.

## When to use this skill
- A new company/contact needs to be logged into the CRM after initial outreach or a sourcing exercise.
- A deal's stage or status needs updating (e.g., moved from "initial contact" to "management meeting").
- A user wants a current pipeline view pulled from the CRM for an internal update or reporting.

## Inputs
- CRM connection/access (via the firm's connected CRM tool).
- The specific records to create/update: company, contact, deal stage, notes, next steps.
- For pipeline pulls: the filter criteria (e.g., by sector, by stage, by deal team).

## Process
1. Confirm the CRM connector is active; if not connected, direct the user to connect it rather than guessing at data.
2. For new records: create the company/contact entry with standard required fields (name, sector, source of introduction, initial stage).
3. For updates: locate the existing record and update stage/status/notes, preserving history rather than overwriting prior notes.
4. For pipeline pulls: query by the requested filter criteria and present a structured pipeline view (stage, company, deal team, last activity date).
5. Flag any records with stale activity (no update in an extended period) so they can be triaged.
6. Confirm changes were saved successfully and surface any records that failed to update.

## Output format
Confirmation of records created/updated, or a structured pipeline table for pull requests (company, stage, owner, last activity, next step).

## Notes / guardrails
- Never fabricate CRM data — if the connector isn't available or a record can't be found, say so rather than presenting placeholder data as real.
- Preserve historical notes/activity rather than overwriting them on update.
