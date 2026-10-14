# Pigeon Clicker — Agent Instructions

## Mission

Build Pigeon Clicker, a funny, polished, browser-based
incremental game.

Players build their own pigeon empire while collectively
conquering the world.

The project is also made for a French YouTube dev video.
Prioritize impressive visible results and simple code.

## Stack

- React + TypeScript + Vite
- CSS with a lightweight styling approach
- Firebase Authentication (anonymous)
- Cloud Firestore for leaderboards and world progression
- Firebase Cloud Functions for trusted score updates
- GitHub Pages for static frontend hosting
- Vitest for game logic tests

## Product principles

- French UI, playful pigeon-themed writing.
- Desktop-first, fully responsive on mobile.
- Polished cartoon style, delightful interactions.
- Satisfying clicking, animations and number feedback.
- Keep dependencies and architecture lightweight.
- Prefer a working MVP over unnecessary abstractions.
- No advertising SDK in the initial MVP.

## Game rules

- Clicking generates pigeons.
- Upgrades increase pigeons per click or per second.
- Upgrades have escalating costs.
- Players have a spendable pigeon balance.
- Lifetime pigeon production never decreases.
- Leaderboard ranks players by lifetime production.
- Global conquest uses validated lifetime production.
- World stages: Paris, France, Europe, Earth, Moon.
- Local progress survives page refreshes.

## Architecture

- src/game/: pure game logic, economy and state.
- src/components/: UI and presentational components.
- src/styles/: styling and animations.
- src/services/: Firebase integrations.
- src/App.tsx: integration owned by the lead agent.
- functions/: server-side validation when needed.
- docs/: product decisions and task tracking.

Keep game logic independent of React and Firebase.
Use TypeScript types for shared contracts.

## Multi-agent workflow

The lead agent owns architecture and integration.

For substantial parallelizable tasks:

1. Define shared interfaces and file ownership first.
2. Delegate independent work to specialized subagents.
3. Give each agent a bounded scope and deliverable.
4. Avoid parallel edits to the same files.
5. Wait for agents and integrate their deliverables.
6. Run tests, lint and production build.
7. Report remaining risks and next steps.

Use the specialized ui, gameplay, firebase and qa
agents when their responsibilities match the task.

Do not spawn agents for trivial changes.

## Security

- Never commit private credentials or service keys.
- Use .env.example for configuration documentation.
- Firebase client config is public, not a secret.
- Enforce Firestore Security Rules.
- Never trust scores submitted by the browser.
- Never let the client directly write global totals.
- Batch score synchronization, never one write/click.
- Rate-limit backend actions where appropriate.
- Prevent obvious impossible score progressions.
- Avoid exposing personal data in public leaderboards.
- Require approval before enabling billable services.

## Development quality

- Favor small, testable modules.
- Test economy formulas and save/load behavior.
- Handle Firebase failures gracefully.
- Provide a playable local/demo mode without Firebase.
- Do not silently swallow errors.
- Keep the game functional during integration.
- Run available checks before finishing a task.

## Git and delivery

- Make focused, readable changes.
- Never overwrite unrelated user changes.
- Do not push or deploy without explicit approval.
- Maintain docs/TASKS.md for major implementation work.
- Explain what was built, tested and left unfinished.

## Definition of Done

A feature is complete when:

- It works as intended.
- It is usable on desktop and mobile.
- Its relevant tests pass.
- It does not break existing game behavior.
- The lead agent has validated the integration.
