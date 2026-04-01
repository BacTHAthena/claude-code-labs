# Game Leaderboard API

## Build & Test
- Install: `npm install`
- Start: `npm start`
- Test: `npm test`
- Lint: `npm run lint`
- Format: `npm run format`
- Seed data: `node src/utils/seed.js`

## Architecture
- src/server.js — Express entry, mounts routes
- src/routes/ — API endpoints (players, matches, leaderboard, seasons)
- src/models/ — Data classes (Player, Match, Season)
- src/services/ — Business logic (store, scoring, achievements, matchmaking)
- src/middleware/ — Validation and error handling
- config/settings.js — Game constants (points, ranks, achievements)

## Coding Conventions
- Strict equality (===), never loose (==)
- Single quotes, no semicolons (Prettier)
- Routes return JSON: `{ error: "message" }` for errors
- Game constants in config/settings.js, not hardcoded

## NEVER
- Do not modify data/*.json directly — use services/store.js
- Do not add dependencies without asking
- Do not expose stack traces in API responses

## Verification
1. `npm test` — all tests must pass
2. `npm run lint` — no errors
