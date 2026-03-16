# Track Budget

A local-first React budget dashboard for tracking income, expenses, and category trends in the browser.

## Live Demo
[https://sbdkim.github.io/track-budget/](https://sbdkim.github.io/track-budget/)

## Key Features
- Add, edit, and delete income or expense entries
- Filter transactions by type, category, and month
- Review total income, expenses, net balance, and top spending category
- Visualize category spending and monthly income-versus-expense trends
- Persist transaction data locally with no backend required

## Tech Stack
- React 19
- Vite
- JavaScript
- CSS
- Recharts
- GitHub Pages

## Setup / Run Locally
```powershell
npm install
npm run dev
```

## Tests
```powershell
npm run test:run
```

## Deployment Notes
- The GitHub Actions workflow in `.github/workflows/deploy-pages.yml` builds `dist/` and deploys to GitHub Pages on pushes to `main`.
- The Vite base path is configurable via `PAGES_BASE` and should be set to `/track-budget/` for Pages builds.
- The app can also be previewed locally with `npm run build` and `npm run preview`.

## Project Layout
- `src/` application code, state, and chart-driven dashboard UI
- `public/` static assets served by Vite
- `vite.config.js` build configuration, including Pages base-path support
- `PROJECT_MEMORY.md` project-specific implementation notes

## Notes
- All budget data stays in the current browser unless the user clears site storage.
- The app uses `localStorage` key `budget-tracker:v1` for persistence.
