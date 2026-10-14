# magic-chess

magic-chess is a lightweight browser chess app built for a kid-friendly experience. It supports:
- playing against a Stockfish bot
- pass-and-play local multiplayer
- a custom playful UI with a timed match flow

## Current project context

This repo is a small static web app with no backend or database. The game logic is driven in-browser using `chess.js`, the board UI is rendered with `chessboard.js`, and the bot uses a Stockfish worker loaded from the repo's `stockfish-worker.js` file.

The app was originally themed with a cheese/character style, but the current version uses a standard classical chess piece set from Lichess (`cburnett` SVGs). The piece assets are stored locally under `img/pieces/` and are intended to be a neutral, clean look that is easier for a child to understand without the custom cartoon style.

## Files

- `index.html` — main game UI, logic, timers, mode switching, board interactions
- `stockfish-worker.js` — loads the Stockfish engine for bot moves
- `img/pieces/` — local SVG chess piece assets
- `img/pieces-cheese/` — legacy cheese variant left behind in prior work, no longer used by the app

## Local run

Because this is a static site, you can run it from a local web server. For example:

```bash
npx --yes http-server -p 8000 .
```

Then open:

```text
http://localhost:8000
```

## Notes for future revisits

- This project is intentionally simple and client-side; it is not a production backend app.
- The piece theme was intentionally changed away from the cheese design to a more standard, less distracting look.
- If the app grows later, a natural next step would be splitting the JavaScript into modules and adding a build system, tests, or a richer UI.
- The repo is meant to stay easy to understand and easy to run in a browser without any install steps beyond a static local server.
