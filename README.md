# Copenhagen Rental Evaluator

A lean comparison tool for rental options in Copenhagen. Open `index.html` in any modern browser. There is no build step and no server, and your inputs stay in the browser's local storage.

It assumes every option you enter has **already passed your non-negotiables** (area, size, pets, and so on). It does not ask you to restate them. It compares what is left on what each place really costs you.

## What you enter

**Once:** your monthly take-home salary, optionally your other monthly costs, and how long you plan to stay.

**Per option, all quick numbers:** rent, utilities (0 if included), deposit, lease length (0 if open-ended), furnished or not, commute minutes, transport cost, and the value of any perks included (gym, internet, laundry).

A collapsed "Fine-tune" section holds the few assumptions behind the maths (commute days, value of commute time, cost to furnish, notice period). The defaults are sensible, so you can ignore it.

## What you get

- **One verdict:** the best-value option and its all-in monthly cost.
- **One chart:** the real monthly cost of each option, split into rent and utilities, commute, and set-up.
- **One table:** all-in cost, rent and utilities as a share of take-home with a sustainability label, money left each month, move-in cash and lease length.
- **A short list of things to double-check,** such as a deposit above three months' rent or a lease longer than your stay.

## How it is calculated

All-in monthly cost = rent + utilities − included perks + transport + value of commute time + furnishing spread over the months you are committed. The deposit is refundable, so it appears as move-in cash and not as a cost.

Sustainability looks at rent and utilities as a share of take-home: comfortable up to 30%, stretched up to 40%, not sustainable above that or when monthly costs exceed take-home. These are rules of thumb. Options that are not sustainable rank last.

Amounts are DKK and the sample data is illustrative. Check each lease for the real terms.
