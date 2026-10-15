# LAST ONE STANDING — Arcade + WHO’S WHO?

Browser-based, real-time multiplayer party game for 2–8 players. No account required.

## Game modes
- **Arcade**: Color Panic, Pick Your Poison, Don't Tap!, Brain Freeze, Double or Nothing.
- **WHO’S WHO?**: Secret code names, trivia, anonymous bluffing, identity matching, and final unmasking.

## Run locally
```bash
npm install
npm start
```
Open http://localhost:3000 on your device. For real multiplayer testing, use a public HTTPS test deployment, then open the same URL on at least two phones and join with the six-character room code.

## Deploy on Render
Use the included `render.yaml` or create a Node web service with `npm install` as build command and `npm start` as start command. The server listens on `PORT` and serves WebSockets on the same host. `/health` returns JSON. **Test a preview deployment first.**

## Important limitations
This is a playable beta, not a production-audited service. Room data lives in server memory; server restarts erase rooms. Disconnecting during a game removes the player; reconnection to an ongoing room is not yet supported. Only use one Render instance (no shared room database). Names and text are unmoderated. There is no user login, chat, or payments. Avoid sharing private information in player names.

## QA checklist
1. Run `npm install`, `npm start`, and verify `/health`.
2. Two different browsers: create room, join room, host starts.
3. Play all five Arcade rounds; confirm results and final winner.
4. Play WHO’S WHO? with distinct real names; verify masks, trivia, bluffing, guesses, reveal.
5. Try invalid room codes, duplicate real names, leaving midway, Play Again.
6. Check narrow iPhone screens and slow connections.
7. Do not replace the existing live Render service until the test passes.
