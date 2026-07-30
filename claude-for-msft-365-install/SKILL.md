---
name: claude-for-msft-365-install
description: Use this skill to provision direct cloud access for the Claude for Microsoft 365 add-in. Triggers include "set up Claude for Microsoft 365", "provision the M365 add-in", or "walk through Azure admin consent for Claude".
---

# Claude for Microsoft 365 Install

## Overview
Walks an IT/admin user through provisioning direct cloud access (Vertex AI, Amazon Bedrock, or an LLM gateway) for the Claude for Microsoft 365 add-in: generating the customized manifest, completing Azure admin consent, and writing per-user configuration via Graph extension attributes.

## When to use this skill
- An admin is setting up the Claude for Microsoft 365 add-in for their organization for the first time.
- A user needs to regenerate or update the add-in manifest after a configuration change (e.g., switching cloud providers).
- A user needs help completing Azure AD admin consent for the add-in.

## Inputs
- Target cloud provider for direct access (Vertex AI, Bedrock, or a custom LLM gateway) and its connection details (project/region, credentials or gateway endpoint).
- Azure AD tenant details and admin access to grant consent.
- The set of users/groups the add-in should be provisioned for.

## Process
1. Confirm the target cloud provider and gather its connection details (API endpoint, authentication method, region/project as applicable).
2. Generate the customized add-in manifest embedding the chosen provider's connection configuration.
3. Walk the admin through the Azure AD admin consent flow for the add-in's required permissions.
4. Write per-user configuration via Microsoft Graph extension attributes so each provisioned user's client picks up the correct backend configuration.
5. Confirm successful provisioning for a test user before rolling out broadly.
6. Document the configuration (provider, tenant, scope of users) for future reference/troubleshooting.

## Output format
A generated manifest file, a completed admin-consent confirmation, and a summary of per-user configuration applied, plus a short setup record for IT documentation.

## Notes / guardrails
- Do not handle or store credentials/secrets in plain chat text — use the organization's standard secret-management approach when providing connection details.
- Admin consent is a privileged, org-wide action — confirm the requesting user has the appropriate admin rights before proceeding.
