# Ashan — React learning platform

A responsive React + Vite redesign of the uploaded Ashan concept. It includes interest-based lesson selection, XP progress, an interactive school-to-career roadmap, career cards, light/dark mode, and the Guru AI chat panel.

## Requirements
- Node.js 18+
- An OpenAI API key to enable generated AI replies (optional for browsing the UI)

## Run locally

```bash
npm install
cp .env.example .env
# Add your own OPENAI_API_KEY to .env if you want live AI responses
```

Open two terminals in this folder:

Terminal 1 — frontend:
```bash
npm run dev
```

Terminal 2 — AI server:
```bash
npm run server
```

Open the Vite URL printed in terminal 1 (usually http://localhost:5173).

## How the AI assistant works
- React sends a message to `POST /api/chat`.
- Express keeps the API key server-side and calls the OpenAI Responses API.
- Without a configured key/server, the UI falls back to a small local demo reply. The frontend does not contain the API key.
- Set `OPENAI_MODEL` in `.env` to another model available to your account if needed.

## Important notes
- This is a prototype. Authentication, per-user chat history, rate limiting, moderation, privacy notices, analytics consent, and production hosting still need to be added before a public launch.
- Career and exam information is illustrative; verify current eligibility with official institutions.
- Google Fonts are loaded by CSS in a normal browser with internet access; the rest of the app does not require external images.
