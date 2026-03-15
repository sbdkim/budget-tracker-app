# Track Budget

A local-first React budget dashboard for tracking income, expenses, and category trends with the Northline visual system.

## Live Demo
Ready for GitHub Pages deployment from this repository using the included workflow in `.github/workflows/deploy-pages.yml`.

## Key Features
- Add, edit, and delete income or expense entries
- Filter transactions by type, category, and month
- Review total income, expenses, net balance, and top spending category
- Visualize category spending and monthly income-versus-expense trends
- Keep all data local in the browser with no backend required

## Tech Stack
- React 19
- Vite
- JavaScript
- CSS
- Recharts
- GitHub Pages

## Setup / Run Locally
```powershell
cd <repo-folder>
npm install
npm run dev
```

## Tests
```powershell
cd <repo-folder>
npm run test:run
```

## Deployment Notes
- The Vite base path is configurable via `PAGES_BASE` and currently defaults to the existing repo slug for safe deployment.
- The GitHub Actions workflow builds `dist/` and deploys it to GitHub Pages on pushes to `main`.
- The live Pages path is `https://sbdkim.github.io/track-budget/`.
- GitHub Pages builds should use `PAGES_BASE=/track-budget/`.

## Architecture
The app uses a single `transactions` state as its source of truth, derives summaries and charts from filtered data, and persists changes to `localStorage` under `budget-tracker:v1`.

## Privacy / Notes
This app does not send data to a server. Transactions stay in the current browser unless the user manually clears site storage.
