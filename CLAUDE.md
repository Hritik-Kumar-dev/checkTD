# react-todo

Single-page todo app built with React 19 and Vite. Todos persist in `localStorage` under the key `react-todos`.

## Layout

- `src/App.jsx` — all UI and state: add, toggle, delete, filters (all / active / completed), clear completed
- `src/App.css` — component styles
- `src/main.jsx` — React root mount
- `src/index.css` — global styles
- `vite.config.js` — Vite + `@vitejs/plugin-react`

## Commands

```sh
npm install
npm run dev      # dev server (default http://localhost:5173)
npm run build    # production build to dist/
npm run preview  # serve dist/
npm run lint     # oxlint (or: npx oxlint src/)
```

## Conventions

- Keep todo logic in `App.jsx` unless the app grows enough to split components
- Todo shape: `{ id, text, completed, createdAt }` — preserve this for localStorage compatibility
- Use functional updates or immutable array ops when changing `todos` state

## Verification

After changes, run `npm run build` and smoke-test in the browser: add a todo, toggle complete, switch filters, delete, and reload to confirm persistence.
