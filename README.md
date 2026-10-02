# Copenhagen Rental Evaluator

A single-page dashboard for comparing rental options in Copenhagen against your own budget. Open `index.html` in any modern browser. There is no build step and no server. Everything runs locally, and your inputs are kept in the browser's local storage.

## What it compares

| Factor | What you enter | How it is used |
|---|---|---|
| Rent and utilities | Rent, heating and water, electricity, other fees | Monthly cash cost and housing share of income |
| Deposit | Deposit, prepaid rent, one-off fees | Move-in cash; the return you give up on tied-up cash |
| Duration | Fixed term or open-ended, notice period, your planned stay | Months you are committed; spreads one-off costs; lease-fit score |
| Furniture | Furnished, partly or unfurnished, cost to furnish, resale value | Furniture you must buy and its net cost |
| Services | A price list of services you care about (gym, internet, laundry…) and which options include them | Adds the cost of wanted services an option lacks, so options are compared like for like |
| Commute | Minutes one way, transport cost, days a week | Transport cost, commute hours and an optional time value |
| Take-home salary | Salary, other income, fixed costs, savings goal, cash available | Sustainability: housing share, monthly surplus, move-in cash gap |

## What you get

- A best-fit verdict with a weighted 0 to 100 score. You set the weights.
- Monthly cost breakdown per option.
- A sustainability chart showing how take-home is used, against comfort and ceiling thresholds for housing share (30% and 40% by default, both editable).
- Cumulative cash out of pocket over the commitment, so you can see where a cheaper rent overtakes a costly move-in.
- A scorecard heatmap and a full comparison table.
- A "Things to check" list covering stretched budgets, move-in cash above your savings, deposits above three months' rent, and leases that are shorter or longer than your stay.
- Light and dark themes, a table view for every chart, and JSON export and import.

The "How the numbers are calculated" section at the bottom of the dashboard sets out every formula and scoring rule.

## Notes

- Amounts are DKK. The sample data is illustrative; use the data menu to start blank.
- Results are estimates built from what you enter. Check each lease for the real terms.
