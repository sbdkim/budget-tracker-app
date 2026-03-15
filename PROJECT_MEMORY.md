# Project Memory

## Product

- Track Budget is a local-first React project built for GitHub Pages.
- The app tracks income and expenses, stores data locally in the browser, and visualizes habits with simple charts under the Northline suite branding.

## Current Decisions

- Frontend stack: Vite, React, plain JavaScript, plain CSS.
- Persistence: browser `localStorage` under `budget-tracker:v1`.
- Charts: `Recharts` for category and monthly summaries.
- Scope: income + expense tracking, CRUD, filters, summary cards, and responsive layout.
- Public branding: page title and primary UI label use `Track Budget | Northline`, while the GitHub repo slug remains `budget-tracker-app` until the rename pass.

## Implementation Notes

- Transactions are the single source of truth in app state.
- Filters affect the transaction list, summary cards, and charts together.
- Categories are fixed in v1 to keep the app approachable for beginners.
