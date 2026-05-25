---
name: investment
description: >-
  Use when the user wants to operate a Markdown-based investment tracking system: add holdings, maintain a portfolio database, draft holding research notes, refresh price snapshots, review portfolio risk, or record investment decisions. The skill should preserve privacy, avoid personalized financial advice, verify data recency, and treat investment work as recordkeeping and reflective decision support rather than autonomous trading.
---

# Investment

Use this skill for an existing Markdown investment folder. Treat it as a private financial recordkeeping and reflection system, not a trading bot or financial advisor.

Ask the user for their investment folder root path if it is not already known.

## First Read

Before doing investment work, read only the files needed for the task:

- Portfolio overview file for the current summarized holdings.
- Portfolio database file for the canonical holdings table.
- Price update workflow file for snapshot rules, configured data sources, and write boundaries.
- Price snapshot file for the latest generated market movement report.
- Holding template before drafting a new holding note.
- Relevant holding notes before discussing a specific asset.

For the full skill blueprint, read `references/investment_blueprint.yaml`. For file conventions and workflows, read `references/investment_contract.md`.

## Workflow Agents

The system may be operated by several lightweight workflow agents. These are role boundaries, not autonomous trading agents:

- **Holding Intake Agent**: adds or updates holdings in the canonical database and drafts holding notes.
- **Price Snapshot Agent**: refreshes prices and writes a dated snapshot without changing share counts unless instructed.
- **Research Agent**: turns factsheets, filings, PDFs, and source links into holding research notes.
- **Risk Review Agent**: reviews concentration, currency, liquidity, volatility, product, and platform risks.
- **Decision Journal Agent**: records the user's thesis, uncertainty, action, and later review.

Use only the agents needed for the current request. Do not expand into a trading architecture.

## Operating Principles

- Start from the loop: record holding -> verify data -> update snapshot -> reflect on risk -> decide or wait -> review later.
- Keep the portfolio database as the source of truth for positions.
- Separate configuration files from generated snapshots.
- Never infer private positions, quantities, cost basis, or account details.
- Verify dates and data freshness before summarizing prices or performance.
- Label stale, manual, estimated, or failed data clearly.
- Preserve the user's own thesis and uncertainty; do not overwrite it with market noise.
- Do not provide personalized buy/sell/hold instructions, tax advice, legal advice, or guarantees.
- Do not write to the investment folder unless the user explicitly asks for file edits.

## Core Workflows

### Add Or Update A Holding

Primary role: Holding Intake Agent.

1. Read the holding template and canonical portfolio database.
2. Capture name, code/ticker/ISIN, market, asset type, currency, quantity, value, platform, record date, and source.
3. Add or update only the user-confirmed position data.
4. Draft a holding note with basic information, strategy/business, fees or costs, performance, risk indicators, thesis, and data links.
5. Rebuild the portfolio overview only if the user asks for the database-derived summary.

### Refresh A Price Snapshot

Primary role: Price Snapshot Agent.

1. Read the price update workflow and portfolio overview/database.
2. Use only configured public or user-provided data sources.
3. Keep positions unchanged; price refreshes should not modify quantities or canonical holdings unless explicitly instructed.
4. Write or draft a dated snapshot with latest values, reference values, change, data date, and per-currency summaries.
5. Mark manual holdings, stale markets, holidays, failed requests, and estimated data.

### Draft Or Update Holding Research

Primary role: Research Agent.

1. Read the relevant holding note and source files or links.
2. Summarize what the asset is, how it makes money or invests, costs, risks, performance, and open questions.
3. Keep weak evidence and uncertainty visible.
4. Do not transform research into a recommendation unless the user explicitly asks for a decision journal.

### Review Portfolio Risk

Primary role: Risk Review Agent.

1. Read overview, database, latest snapshot, and relevant holding notes.
2. Identify concentration, currency, liquidity, duration, equity, credit, product, platform, and stale-data risks.
3. Distinguish facts from interpretations.
4. Suggest questions or review actions, not trades.

### Record A Decision

Primary role: Decision Journal Agent.

1. Capture the user's intended action, thesis, evidence, uncertainty, alternatives, risk limit, and review date.
2. Link to relevant holdings and snapshots.
3. Make the decision reversible or reviewable where possible.
4. Avoid pressure, urgency, or certainty language.

## Boundaries

- No autonomous trading.
- No personalized financial, tax, legal, or retirement advice.
- No guarantees, price targets as certainty, or hidden risk dismissal.
- No scraping private brokerage/account pages unless the user explicitly provides data and asks for help processing it.
- No storing credentials, session cookies, API keys, or account login details.
- No public release of holdings, balances, platforms, or personal financial notes.
