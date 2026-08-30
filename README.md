# Workout Tracker

A lightweight, offline-first hypertrophy training tracker built as a single self-contained HTML file. No build step, no backend, no external dependencies at runtime — open it in any browser and it works.

**[🔗 Live demo](https://aalnisf.github.io/workout-tracker/)**

## Features

- **5-day training split** (Heavy Push, Heavy Pull, Legs, Chest+Back Volume, Arms+Shoulders) with per-exercise sets, reps, and weight targets
- **Progressive overload engine** — automatically suggests next week's numbers based on your last logged session:
  - Hit every rep target → +1 rep next time
  - Hit the rep ceiling at RIR 2 → +2.5kg, reset reps to base target
  - Missed the target → repeat the same weight/reps
- **Barbell math built in** — enter weight per side, the app calculates total (including the 20kg bar)
- **Per-session flexibility** — swap an exercise for a substitute, add an extra exercise, or remove one, all without touching the base program
- **Free/travel days** — log a fully custom session (e.g. full body or upper/lower while traveling) with its own exercise list
- **Local persistence** — all data is saved to your browser's `localStorage`. Nothing is sent to a server.

## Usage

Just open `index.html` in any modern browser (Safari, Chrome, Firefox, Edge). That's it — no installation, no dependencies, no internet connection required after the page loads.

### Run locally

```bash
git clone https://github.com/aalnisf/workout-tracker.git
cd workout-tracker
open index.html   # macOS
# or just double-click index.html in Finder/Explorer
```

### On mobile (iOS)

1. Open the [live demo link](https://aalnisf.github.io/workout-tracker/) in Safari
2. Tap the Share button → **Add to Home Screen**
3. Launch it from the home screen icon from then on — this keeps you on the same browser storage every time

## Data & privacy

- All workout data is stored **locally in your browser** via `localStorage` — it never leaves your device and is not sent to any server.
- Data is scoped to the specific browser + origin you use. Opening the app in a different browser, in private/incognito mode, or on a different device will **not** show your existing logs.
- Clearing your browser's site data for this page will erase your logs. There is currently no built-in export/import — back up important numbers manually if needed.

## Tech

Vanilla JavaScript, no framework, no build tooling. Single `index.html` file (~40KB) containing all markup, styles, and logic. Chosen deliberately for zero-dependency reliability — it will keep working regardless of any third-party service's availability.

## License

MIT — see [LICENSE](LICENSE).
