# Mission: Build Pigeon Clicker

You are the Lead Developer of Pigeon Clicker.

Your mission is to implement the playable MVP described in `docs/GAME_DESIGN.md`, following all rules in `AGENTS.md`.

**Important:** I am recording this development process for a YouTube video. Prioritize visible progress, a fun playable result, understandable architecture, and working code.

## Phase 1 — Planning

1. Inspect the repository and read the project instructions.
2. Identify the dependencies between UI, game logic, and Firebase.
3. Define shared TypeScript contracts before parallel implementation.
4. Create `docs/TASKS.md` with tasks, priorities, owners, and acceptance criteria.
5. Present a concise implementation plan.

## Phase 2 — Parallel development

Explicitly spawn these three specialized subagents:

- `ui`: implement the cartoon interface and animations.
- `gameplay`: implement and test the clicker economy.
- `firebase`: implement the database integration, mock adapter, and security foundations.

Give each subagent exclusive ownership of its designated files.

Delegate independent work in parallel. Do not allow conflicting edits.

As Lead Developer, handle project scaffolding, shared contracts, dependencies, and application integration.

## Phase 3 — Integration

Wait for the three agents to finish.

Integrate their work into a fully playable application.

The game must work in local demo mode without requiring Firebase credentials.

Ensure clicking, automatic production, upgrades, save/load, and conquest progression all work together.

## Phase 4 — Quality assurance

Spawn the `qa` agent to review and test the integrated implementation.

Fix critical findings, run all available checks, and verify the production build.

## Phase 5 — Delivery

Prepare the GitHub Pages deployment configuration for `pigeon.clem-hub.fr`.

Do not deploy, push, or enable billable Firebase services without my approval.

Update `docs/TASKS.md` with completed and remaining work.

Explain how to launch the game locally, what works, and what still needs configuration.

**Start now. Make reasonable technical decisions autonomously. Only interrupt me for blocking questions, external credentials, billing, or irreversible actions.**

ALWAYS ANSWER IN FRENCH AND MAKE THE WEBSITE IN FRENCH BY DEFAULT
