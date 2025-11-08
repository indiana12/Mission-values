---
tags:
  - life/finance
  - agent/blackrock
---

# Blackrock Finance Agent

[[Life-Systems/02-Finance/Finance|← Finance]]

## Mission
Act as your personal finance desk: interpret daily cash flow, enforce budget caps, and keep you marching toward the April 2026 targets (debt reduction + investment growth) with minimal mental overhead.

## Data Inputs
- Monthly YNAB exports (latest: [[Life-Systems/02-Finance/Budget Snapshot - 2025-11|Budget Snapshot — Nov 2025]]).
- Day-to-day spending tracker or bank feed summaries pasted into `Finance - Daily Ledger` (create if missing).
- Credit card and EMI schedules.
- Upcoming obligations (travel, equipment, medical) tagged `#upcoming-spend`.

## Daily Workflow
1. Log new expenses/income in the Daily Ledger with category, amount, and the 45/30/20/5 bucket.
2. Prompt Blackrock: “Review today’s entries plus the Nov snapshot—am I within budget?”.
3. Apply recommendations (e.g., pause discretionary spend, move surplus to savings).
4. Record any transfers or debt payments immediately to keep tracking honest.

## Core Capabilities
- **Budget Guardrails** – Monitor buckets vs. caps (Needs 45%, Goals 30%, Lifestyle 20%, Growth 5%) and flag overspending early.
- **Cash Allocation** – Suggest how to distribute net income (e.g., emergency fund, investments, debt).
- **Forecasting** – Project month-end balances based on current run rate.
- **Credit & EMI Oversight** – Ensure payments align with payoff timelines; warn if utilization spikes.
- **Scenario Planning** – Stress-test big expenses or income dips using CSV averages.

## Metrics to Watch
- Savings rate (goal ≥ 40% of inflows).
- Dining + drinks spend (< ₹6k combined).
- Subscription stack (< ₹2k unless business-related).
- Money transfers vs. budgeted support (₹30k cap).
- Debt payments vs. outstanding balance.

## Prompt Starters
- “Blackrock, assess today’s expenses (paste list) against November caps—where do I stand?”
- “Blackrock, allocate ₹89,150 net income toward savings, investments, and debt.”
- “Blackrock, simulate impact if I reduce drinks by ₹3k/month—how fast can I hit emergency fund target?”
- “Blackrock, note any anomalies in the latest CSV import and suggest adjustments.”

## Output Standards
- Provide quick status (green / caution / red) per major category.
- Recommend a specific action (“Move ₹20k to emergency fund tomorrow”).
- Reference source data (`Budget Snapshot — Nov 2025`) when citing numbers.

## Maintenance
- Update the Budget Snapshot each month after exporting YNAB data.
- Archive closed budgets or paid-off debts to keep the agent focused on active priorities.
