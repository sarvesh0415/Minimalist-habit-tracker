# 📅 Daily Tracker

A minimal, single-file habit tracker that runs entirely in your browser — no installs, no accounts, no internet required. All data lives in your browser's `localStorage`.

---

## Features

### ✅ Today Tab
- Add and delete custom habits/tasks
- Click a task to **mark it done** (green checkmark)
- Hover a task to reveal the **⏭ skip button** — marks it as skipped for the day (amber, excluded from stats)
- Live stats: **Done**, **Left**, **Skipped**, **Streak**
- Progress bar that fills as you complete tasks (skipped tasks don't count against you)

### 📊 Weekly Tab
- Bar chart of your **completion % for the last 7 days**
- Today is highlighted in a distinct color

### 📆 Monthly Tab
- Bar chart of **tasks completed per day** for the last 30 days

### 📈 Rates Tab
- **Overall all-time completion rate**
- **Per-habit completion rate cards** with mini progress bars
- Skipped days are excluded from all rate calculations

### 🟩 Heatmap Tab
- GitHub-style **17-week activity heatmap**
- 5 green intensity levels based on daily completion %
- **Amber cells** for fully-skipped days
- Today is outlined for easy reference
- Month labels and day-of-week labels
- Hover any cell to see the date and exact completion %

### 🌙 Dark Mode
- Toggle with the moon/sun button in the top-right corner
- Auto-detects your system preference on first visit
- Preference is saved and persists across sessions

---

## Task States

| State | How to set | Visual |
|---|---|---|
| **Pending** | Default | Empty checkbox |
| **Done** | Click the task | Green background + checkmark |
| **Skipped** | Click ⏭ button on hover | Amber italic text + dash |

> Skipped tasks don't count as failures. They're excluded from completion %, streak calculations, and rate stats — useful for rest days, travel, or illness.

---

## Data & Privacy

- **100% local** — all data is stored in `localStorage` under the key `tracker_data`
- **No network requests**, no analytics, no tracking
- Data format: `{ tasks: [...], history: { "YYYY-MM-DD": { "TaskName": true|false|"skip" } } }`
- Clearing your browser's site data will erase all history

---

## Usage

Just open `habit-tracker.html` in any modern browser. No build step, no dependencies.

```
Double-click habit-tracker.html  →  Done.
```

Works in Chrome, Firefox, Edge, Safari.

---

## Default Habits

The tracker ships with these defaults (edit or delete them freely):

- Gym
- ML Course
- DSA
- APT
- DBMS
- Codebase Understanding
- Diet

---

## File Structure

Everything is a single self-contained HTML file:

```
habit-tracker.html
├── <style>     — CSS with CSS variables for light/dark theming
├── <body>      — Tab UI, task list, charts, heatmap panels
└── <script>    — All logic: storage, rendering, charts, heatmap
```

No external libraries. No frameworks. Vanilla HTML + CSS + JS.
