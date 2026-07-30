---
name: financial-planning
description: Use this skill to build financial planning scenarios and projections for wealth management clients — retirement funding, education funding, cash flow projections, and goal-based planning. Triggers include "build a retirement plan for this client", "project their cash flow to retirement", or "run a financial planning scenario".
---

# Financial Planning

## Overview
Builds goal-based financial planning projections for individual clients: retirement readiness, education funding, major purchase planning, and general long-term cash flow projections, incorporating assumptions the advisor and client agree on.

## When to use this skill
- A client needs a retirement readiness projection or update.
- A user wants to model a specific goal (education funding, home purchase, early retirement) against the client's current financial position.
- A user wants to stress-test a plan under different assumptions (market returns, savings rate, retirement age).

## Inputs
- Client's current financial position: assets, liabilities, income, expenses, savings rate.
- Goal(s) being planned for: target amount, target date, priority relative to other goals.
- Planning assumptions: expected investment return, inflation rate, life expectancy/planning horizon, Social Security or pension assumptions where relevant.
- Risk tolerance and any constraints (liquidity needs, tax considerations).

## Process
1. Establish the current financial position as the starting point: net worth, income, expenses, and current savings/contribution rate.
2. Define the goal(s) precisely: what, by when, and how much is needed (in today's dollars and inflation-adjusted).
3. Project forward using the agreed assumptions, showing whether the client is on track, ahead, or behind for each goal.
4. Identify the levers available if the plan shows a shortfall: increased savings rate, delayed goal timing, adjusted asset allocation, or reduced goal amount.
5. Stress-test the plan under at least one conservative scenario (lower returns, higher inflation, earlier retirement) to show sensitivity, not just a single base case.
6. Present the plan's key outputs clearly: probability/likelihood of meeting the goal (if using Monte Carlo or similar) or a base-case/downside comparison if using deterministic projections.

## Output format
A clear projection showing current trajectory vs. goal, the assumptions used, a sensitivity/stress-test view, and — if a shortfall exists — the specific levers available to close the gap.

## Notes / guardrails
- Always state assumptions explicitly (they drive the entire output) and show at least one sensitivity case, not just a single-point projection.
- This is planning/projection output to inform an advisor-client conversation, not a guarantee of future outcomes — avoid language implying certainty about market returns.
