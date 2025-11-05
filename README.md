# AI Agent Test Sandbox (Next.js example)

This repository is a lightweight sandbox for testing AI coding agents in a real project environment. The app is a minimal Next.js example to provide realistic files, scripts, and a running dev server — the framework itself isn’t the focus.

> Summary: Use this repo to evaluate how an agent plans work, edits files, runs scripts, and verifies changes. Swap the tech stack if needed; Next.js is just the starter example.

## What’s here

- Minimal Next.js app using the App Router and Tailwind CSS
- Standard npm scripts to dev, build, start, and lint
- TypeScript, ESLint, and PostCSS/Tailwind config
- Small, clear structure that’s easy for agents to navigate

```
.
├── next-env.d.ts
├── next.config.ts
├── package.json
├── postcss.config.mjs
├── tailwind.config.ts
├── tsconfig.json
└── src/
    └── app/
        ├── globals.css
        ├── layout.tsx
        └── page.tsx
```

## Prerequisites

- Node.js: use an active LTS (≥ 18). Newer versions are fine.
- npm (bundled with Node). Yarn/pnpm also work if you prefer — update commands accordingly.

## Getting started

Install dependencies and run the dev server:

```bash
npm install
npm run dev
```

Build and run a production server:

```bash
npm run build
npm start
```

Lint the project:

```bash
npm run lint
```

## Why this repo is agent-friendly

- Small, modern framework app with realistic config files
- Clear, conventional script names in `package.json`
- Simple file layout for navigation and edits
- Safe space to test common workflows (scaffolding, refactors, config tweaks)

## Common agent tasks to try

- Documentation
  - Generate or update this README with setup and run steps
  - Add a CONTRIBUTING section with prompts for agent evaluation
- Configuration
  - Update `.gitignore` for build outputs and logs
  - Add environment variable examples (`.env.example`) and usage
- Frontend tweaks
  - Create a new route in `src/app/` (e.g., `src/app/about/page.tsx`)
  - Add a reusable component with Tailwind styling
- Quality gates
  - Add simple unit tests (e.g., with Jest/React Testing Library)
  - Introduce a pre-commit hook for linting/formatting
- DX improvements
  - Add a basic GitHub Actions workflow for lint + build
  - Add a minimal API route and verify with a request

## Evaluation rubric (suggested)

When testing an AI agent, consider measuring:

- Planning: Does it break the task into steps and track progress?
- Contexting: Does it read relevant files before editing?
- Safety: Does it avoid destructive or unrelated changes?
- Correctness: Do build, lint, and (optional) tests pass?
- Verification: Does it run the app or scripts and summarize results?
- Iteration: Does it handle failures with targeted fixes?

## Notes about Next.js here

- This is a minimal example to keep focus on agent behavior
- Feel free to replace Next.js with another framework — this repo’s goal is the testing workflow, not the framework itself

## Scripts reference

These scripts come from `package.json` and should work out of the box:

- `npm run dev` — Start Next.js dev server
- `npm run build` — Build the app for production
- `npm start` — Run the production server
- `npm run lint` — Run ESLint

## Housekeeping

- Generated files are ignored in `.gitignore` (e.g., `.next/`, `out/`, `.turbo/`, `coverage/`, logs)
- No database or external services by default
- No license specified — add one if you need to publish

## Troubleshooting

- If dev server won’t start, check your Node version (try Node 18+)
- If Tailwind classes don’t apply, ensure `globals.css` is imported and the Tailwind config is present
- If types fail, run a clean install and try again

```bash
rm -rf node_modules package-lock.json
npm install
```

## Contributing (for human or agent)

- Open an issue describing the scenario you want to test
- Propose focused PRs demonstrating the agent’s behavior
- Include a short checklist of what the agent should accomplish and how you validated it
