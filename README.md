# Tide — Water Intake Logger

A single-file web app that tracks daily water intake with an AI hydration coach and smart reminders.

## Features

- **Tide glass visual** — animated water level shows progress toward your daily goal
- **Quick-add buttons** — Glass (150ml), Cup (250ml), Can (330ml), Bottle (500ml), or custom amount
- **Daily log** — every entry with timestamp, deletable
- **7-day history chart** — see your pace across the week
- **Adjustable goal** — set your own daily ml target
- **AI Tide Coach** — analyzes your pace, gaps between drinks, and time of day to give a short, specific nudge
- **Smart reminders** — AI plans a reminder schedule for the rest of your day and delivers them as in-app toast messages
- **AI record** — a running log of every insight and reminder the AI has generated
- **Local storage** — all data (logs, goal, reminders, records) stays on your device

## Setup

1. Download `water-tracker.html`
2. Open it in any modern browser (Chrome, Safari, Firefox, Edge)
3. To enable the AI Coach and Smart Reminders:
   - Get an API key from [console.anthropic.com](https://console.anthropic.com) → **API Keys**
   - Paste it into the **Anthropic API key** field near the top of the app
   - Click **Save**

That's it — no install, no build step, no server.

## Using it

- **Log water**: tap a quick-add button, or type a custom amount and hit Add
- **Get a coaching tip**: tap the ↻ icon on the Tide Coach card (also fires automatically after you log a drink)
- **Turn on reminders**: flip the Smart reminders switch, set your wake/sleep times, tap **Plan today's reminders**
- **View AI history**: expand **AI record** near the bottom to see everything the coach and reminders have said

## Notes on the API key

- The key is stored only in your browser's `localStorage` — it's never sent anywhere except directly from your browser to Anthropic's API
- Anyone with access to this browser/device could view it via dev tools, so don't use this on a shared or public computer with a key you care about
- Without a key, everything else in the app (logging, charts, goal tracking) still works fine — only the AI coach and reminder planner require it

## Data & privacy

All data — your logs, goal, reminder schedule, and AI record — is stored locally in your browser. Nothing is synced to a server. Clearing your browser data or switching browsers/devices will reset the app.
