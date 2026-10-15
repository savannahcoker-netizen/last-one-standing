# LAST ONE STANDING

A browser-based, real-time party game for 2–8 people using six-character room codes. Five mini-games, synchronized server-side scores and timers, random funny names, and a final leaderboard.

## Run locally

Requires Node.js 18+.

```bash
npm install
npm start
```

Open http://localhost:3000 in two browser tabs to test. To test across two separate devices, deploy to a public host first or use a local network setup.

## Deploy

This project needs a **persistent Node.js server with WebSocket support**. A static-only upload to Netlify won't support the multiplayer server. Deploy as a Node web service (for example Render, Railway, or another Node-capable host). Use `npm install` as build command and `npm start` as start command. The server listens on the host-provided `PORT` variable.

After deployment, open the HTTPS URL on two devices, create a room on one, join by code on the other, play all five rounds, and confirm both devices show matching scores and the same winner.

## Notes

This is a first playable prototype. Rooms are stored in memory, so restarting the server clears rooms. Disconnecting during play removes a player. Rejoining an ongoing room is not yet supported. Public URL and successful two-device testing must be completed before submitting to Handshake.
