# ⚡ Momentum — Daily Progress Tracker

A premium, single-file daily habit and goal tracker that runs entirely in your browser — no backend, no account, no install required.

![Dark/Light theme](https://img.shields.io/badge/theme-dark%20%2F%20light-6c63ff?style=flat-square)
![Zero dependencies](https://img.shields.io/badge/dependencies-zero-22c55e?style=flat-square)
![Single file](https://img.shields.io/badge/build-single%20HTML%20file-f59e0b?style=flat-square)

---

## ✨ Features

### 📊 Dashboard
- Live stat cards showing today's task completion, current streak, weekly average, and total goals
- Animated SVG ring chart for today's progress
- 7-day bar chart visualising completion percentage per day
- Per-goal progress bars for the current week
- Recent activity feed

### 🎯 Goal Manager
- Create goals with a name, emoji, category, and custom note fields
- Categories: Health, Work, Learning, Personal, Finance, Fitness
- Filter goals by category or status (All / Active / Completed)
- Edit and delete goals at any time
- Per-day notes modal for each goal with free-form fields

### 📓 Daily Journal
- Mood picker (10 emoji moods)
- Productivity slider (1–10)
- Prompted reflection fields: What I learned, Biggest achievement, Problems faced, Improvements for tomorrow
- Auto-saves on blur; persists across sessions

### 📅 Calendar View
- Monthly calendar with per-day completion colour coding
- Click any day to open a detail panel showing tasks and journal entry for that date

### 🔍 Search
- Full-text search across all journal entries and goal notes
- `Ctrl/Cmd + K` keyboard shortcut
- Debounced live search, results sorted newest first

### 📤 Export / Report
- Opens a print-ready HTML report in a new tab
- Includes task checklist, journal summary, streak, and generation timestamp

### 🔔 Notifications
- Requests browser notification permission on first load
- Schedules a daily 9 PM reminder if any tasks are incomplete that day

### 🎨 UI & UX
- Premium dark theme (default) and light theme, togglable at any time
- Collapsible sidebar
- Smooth page transitions and hover animations
- Custom thin scrollbars, glassmorphism topbar
- Fully keyboard accessible (Escape closes all modals)
- Responsive layout (desktop-first)

---

## 🚀 Getting Started

No build step. No server. Just open the file.

```bash
# Clone the repo
git clone https://github.com/your-username/momentum.git
cd momentum

# Open directly in your browser
open momentum.html
# or on Linux:
xdg-open momentum.html
# or on Windows:
start momentum.html
```

That's it. All data is saved to `localStorage` in your browser automatically.

---

## 📁 Project Structure

```
momentum/
└── momentum.html   # Entire app — HTML, CSS, and JS in one file
```

The file is intentionally self-contained so it can be:
- Bookmarked and opened as a local file
- Hosted on any static file host (GitHub Pages, Netlify, Vercel, etc.)
- Shared as a single attachment

---

## 🌐 Hosting on GitHub Pages

1. Push `momentum.html` to a repo (renaming it `index.html` is optional but cleaner for GitHub Pages).
2. Go to **Settings → Pages**.
3. Set Source to `main` branch, `/ (root)`.
4. Visit `https://your-username.github.io/momentum/`.

> **Note:** Each browser/device stores its own `localStorage` — data does not sync across devices.

---

## 🛠 Tech Stack

| Layer | Choice |
|-------|--------|
| Markup | Semantic HTML5 |
| Styling | Vanilla CSS with custom properties (dark + light themes) |
| Logic | Vanilla JavaScript (ES2020+) |
| Fonts | [Syne](https://fonts.google.com/specimen/Syne) (display) · [DM Sans](https://fonts.google.com/specimen/DM+Sans) (body) via Google Fonts |
| Storage | `localStorage` (browser-native, no server needed) |
| Dependencies | **None** |

---

## 💾 Data & Privacy

All data lives in your browser's `localStorage` under the key `momentum_v1`. Nothing is ever sent to a server.

To back up your data manually:
1. Open browser DevTools → Application → Local Storage.
2. Copy the value of `momentum_v1`.
3. Save it somewhere safe.

To restore, paste the value back with:
```js
localStorage.setItem('momentum_v1', '<your-backup-string>');
location.reload();
```

---

## ⌨️ Keyboard Shortcuts

| Shortcut | Action |
|----------|--------|
| `Ctrl / Cmd + K` | Open search |
| `Escape` | Close any open modal |

---

## 🖼 Screenshots

> Add your own screenshots here — dark and light mode both look great.

---

## 📄 License

MIT — do whatever you like with it.

---

## 🙌 Contributing

Pull requests are welcome. For major changes, open an issue first to discuss what you'd like to change.

1. Fork the repo
2. Create a feature branch (`git checkout -b feature/my-feature`)
3. Commit your changes (`git commit -m 'Add my feature'`)
4. Push to the branch (`git push origin feature/my-feature`)
5. Open a Pull Request
