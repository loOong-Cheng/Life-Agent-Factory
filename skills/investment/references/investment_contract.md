# Investment Contract

Investment folder root:

`<USER_CONFIGURED_INVESTMENT_ROOT>`

Ask the user for this path before reading or editing files if it is not already known.

## Canonical File Types

Use the user's actual filenames when known. A typical folder contains:

- Portfolio overview: summarized holdings generated from the database.
- Portfolio database: source-of-truth holdings table.
- Price update workflow: rules for refreshing market data and writing snapshots.
- Price snapshot: dated generated report of price movement and portfolio changes.
- Holdings folder: one note per meaningful holding.
- Holding template: base schema for new holding research notes.

## Source-Of-Truth Rules

- The portfolio database is the source of truth for positions.
- Price snapshots are generated outputs and should not change quantities.
- Holding notes explain what the asset is, why it is held, risks, costs, evidence, and uncertainty.
- Manual holdings or private platform values must be supplied by the user.
- Never infer unreported positions, balances, platforms, or account details.

## Holding Note Schema

Preserve these frontmatter fields when present:

- `name`
- `code`
- `market`
- `type`
- `currency`
- `platform`
- `isin`
- `valor`
- `qty`
- `value`
- `record_date`
- `tags`

Useful note sections:

- snapshot
- basic information
- strategy or business
- asset allocation or holdings characteristics
- fees or costs
- performance
- risk indicators
- user's view or thesis
- data sources and links
- notes

## Price Snapshot Rules

- Read the configured workflow before fetching or calculating.
- Use only public or user-provided data sources.
- Report source, data date, reference value, latest value, change, and failures.
- Preserve original currencies unless the user's workflow defines conversion rules.
- Mark market holidays, stale values, missing values, manual inputs, and estimates.
- Do not modify portfolio database quantities during a price refresh.

## Financial Safety

- This skill supports organization, research synthesis, and reflection.
- It is not a financial advisor.
- Do not provide personalized buy, sell, hold, tax, legal, retirement, or suitability advice.
- Encourage professional advice for high-stakes, tax, legal, retirement, leverage, or complex product questions.
- Keep private financial data out of reusable/public artifacts.
