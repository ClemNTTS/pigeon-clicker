# Pigeon Clicker — Game Design V1

## Concept

A humorous, community-driven incremental browser game.
Players produce pigeons and compete in a world leaderboard.
Everyone contributes to a shared conquest of the world.

## Visual direction

Cartoon 2D, friendly, silly and colorful.
Large animated central pigeon.
Readable counters and playful upgrade cards.
Responsive desktop and mobile layouts.

## Main screen

- Global conquest progress and current territory
- Main pigeon and personal pigeon counter
- Pigeons per click and per second
- Upgrade shop
- Top 10 worldwide leaderboard
- Current player's rank and nickname

## Economy

- Clicking produces pigeons.
- Automatic buildings produce pigeons per second.
- Upgrade costs increase after each purchase.
- Spending pigeons does not lower lifetime production.
- Avoid game-breaking integer overflow.

Starting upgrades:

- Bread Crumbs: +1 per click
- Magic Baguette: +5 per click
- Cozy Nest: +1 per second
- Park Grandma: +10 per second
- Pigeon Factory: +100 per second
- Mutation Lab: +1,000 per second

## Community conquest

Cumulative global targets (initial balancing):

- Paris: 10,000 pigeons
- France: 100,000 pigeons
- Europe: 1,000,000 pigeons
- Earth: 10,000,000 pigeons
- Moon: 100,000,000 pigeons

Targets can be rebalanced before public release.
Progress is shared between all players.

## Leaderboard

- Anonymous Firebase authentication
- Editable public nickname
- Rank by validated lifetime pigeons
- Display top 10 players
- Show personal rank when available
- Protect against basic score manipulation

## MVP requirements

- Playable without Firebase configuration
- Game progress persists after refresh
- Responsive and visually satisfying
- Shop with escalating prices
- Passive income
- World conquest progress UI
- Firebase leaderboard integration
- GitHub Pages deployment workflow

## Future features

- Google AdSense integration
- New territories and achievements
- Special pigeon skins
- Community events
- Additional analytics

## Non-goals for V1

- Multiplayer combat
- Trading
- Payment systems
- Player messaging
- Complex account registration
