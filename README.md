# Open World Rivals — multiplayer prototype v0.1

A browser-based, third-person 3D multiplayer city prototype. Includes streets, buildings, wandering civilians, pursuing police, fists/pistol, health, wanted levels, knockouts, respawning, score, and WebSocket player synchronization.

## Run locally

Install Node.js 18 or newer. In this directory:

```bash
npm install
npm start
```

Visit http://localhost:3000 . Open two browser tabs or devices on the same accessible server to test multiplayer. The Three.js rendering library loads from a CDN, so clients need internet access.

## Publish

Deploy this Node.js project to a hosting provider that supports long-running Node servers and WebSockets, set start command to `npm start`, and share the HTTPS URL. On many providers, the PORT environment variable is set automatically.

## Controls

WASD / arrow keys to move, mouse to rotate the camera (click the scene to lock mouse), click or Space to attack, 1 for fists, 2 for pistol. Mobile includes a direction pad, turn buttons, weapon toggle, and attack.

## Prototype limitations

This is an early playable prototype, **not** a production-ready game. Buildings currently do not have physics collision, weapon effects are basic, combat hit checks are approximate, movement is not yet server-speed-validated against malicious clients, no persistent accounts or database, no sound, and NPCs are basic AI. Player positions and NPCs are synchronized at 20 Hz; client sends movement input at display refresh rate. PvP is enabled across the map. Production release should add anti-cheat, moderation, safe zones, privacy safeguards, persistence, and load testing.
