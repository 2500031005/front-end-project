# Ledger — React Budget Planner 2.0

A React-powered upgrade of the original Ledger Budget Planner. The original budgeting workflows and browser data format are retained, while React provides the application shell, Three.js provides a subtle 3D financial atmosphere and currency-change coin animation, and Framer Motion adds interface motion.

## Stack
- React 19 + Vite
- Three.js (3D scene, floating coin model and currency-change money rain)
- Framer Motion (UI entrance and currency notification)
- Lucide React (available for new React UI elements)
- Existing HTML/CSS/JavaScript budget logic, charts, account flow and localStorage data

## Run locally
1. Install Node.js 20.19+ or 22.12+.
2. Open this folder in VS Code.
3. Run `npm install`.
4. Run `npm run dev`.
5. Open the local URL printed by Vite (normally http://localhost:5173).
6. Create an account or sign in. Existing browser-local accounts and financial records are retained because the original `auth.js` and `script.js` data keys are unchanged.

For a production build, run `npm run build`; preview it with `npm run preview`.

## Project structure
```
react-budget-planner/
├── index.html
├── login.html / signup.html
├── auth.js / script.js / style.css
├── src/
│   ├── main.jsx
│   ├── react-layer.css
│   └── legacy.html
├── package.json
└── README-LEGACY.md
```

## Currency animation
The selected currency remains the original app's setting. When the currency dropdown changes, the React/Three.js layer updates the large embossed coin and releases a short burst of matching coin tokens. The background scene is decorative and does not intercept clicks or block form interaction.

## Data and security note
This is a React frontend integration, not a server-backed backend. The existing account, transaction, budget and savings data continue to use browser `localStorage`. This is appropriate for a local academic/demo project, not secure multi-user production finance software. A real backend would require an API, database, server-side authentication and authorization.


## Dependency compatibility note
This project uses `vite` 7 with `@vitejs/plugin-react` 5, a compatible
pair. Do not change the plugin to `latest` while staying on Vite 7, because
newer plugin releases may require Vite 8 and trigger npm `ERESOLVE` errors.
