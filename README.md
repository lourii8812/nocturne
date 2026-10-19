# NOCTURNE — Your Personal Universe

A midnight-blue and violet personal life dashboard built with vanilla HTML, CSS, and JavaScript. No build step or dependencies are required.

## Included features

- Overview dashboard with task, goal, focus, and habit summaries
- Task management with priorities, due dates, categories, tags, filters, and a Kanban-style board
- Monthly calendar with scheduled tasks and selected-day agenda
- Focus timer with configurable focus and break durations, saved session history
- Goals with progress tracking and individual milestones
- Habit check-ins, recent weekly history, and streak counts
- Journal entries and searchable/pinnable notes
- Insights based on locally recorded task completion, habits, and focus sessions
- Global search (`Ctrl+K` / `Cmd+K`)
- Accent colors, profile personalization, and timer settings
- JSON export/import, example data, and data clearing
- Responsive layout and a basic offline-ready PWA shell

## Run locally

Some browser features, including service workers and PWA installation, require HTTP or HTTPS. For the most reliable experience:

1. Extract the ZIP.
2. Open a terminal in the extracted `nocturne` folder.
3. Run `python -m http.server 8000`
4. Open `http://localhost:8000`

You can also open `index.html` directly to test most app features, but service worker/PWA support may not activate from a `file://` URL.

## Install as an app

Deploy the folder to a static HTTPS host (for example, GitHub Pages), then use your browser's install/add-to-home-screen option when available. PWA behavior and installation prompts vary by browser and operating system.

## Data and privacy

Your workspace is saved in `localStorage` in the current browser profile. It does not automatically sync between devices or create an account. Export JSON backups regularly. Local storage is not encrypted by default, so do not treat this as a secure vault for passwords or highly sensitive information.

## Project structure

- `index.html` — app shell, navigation, modals, global search
- `styles.css` — responsive midnight theme and components
- `app.js` — state, rendering, interactions, local storage, data import/export
- `manifest.json` — PWA metadata
- `sw.js` — static shell cache for offline app loading
- `assets/icon.svg` — app icon

## Current build notes

This is the first complete functional foundation. It deliberately avoids third-party JavaScript libraries so it can run as a small static site. Potential next iterations include recurring-task scheduling, richer drag-and-drop Kanban, encrypted local vault mode, data visualizations with date filters, calendar export, and more granular dashboard widget customization.

## Analytics dashboard

The Analytics home includes selectable 7-day, 30-day, 90-day, and all-time windows; period-over-period comparisons for task completion, habit consistency, and focus time; and donut charts for task status, task priority, and habit check-ins. Task and habit metrics are based on tracked records and dates. Goal progress is shown as a current snapshot because the app does not store historical goal-progress snapshots.
