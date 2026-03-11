<div align="center">

<br/>

<img src="https://img.shields.io/badge/⚡-Deep%20Focus-6c63ff?style=for-the-badge&labelColor=07080d&color=6c63ff" height="42"/>

<h3>A professional deep-work session logger built with React</h3>
<p>Track focus sessions · Analyze productivity · Build daily streaks</p>

<br/>

[![Live Demo](https://img.shields.io/badge/🌐%20Live%20Demo-Visit%20App-6c63ff?style=for-the-badge&labelColor=0c0e16)](https://crafted-by-tarun.github.io/Deep-Focus/)
&nbsp;
[![GitHub Pages](https://img.shields.io/badge/GitHub%20Pages-Deployed-222?style=for-the-badge&logo=github&logoColor=white)](https://pages.github.com/)
&nbsp;
[![React](https://img.shields.io/badge/React-18-61DAFB?style=for-the-badge&logo=react&logoColor=black)](https://react.dev/)
&nbsp;

<br/>
<br/>

</div>

---

## 📌 What is Deep Focus?

**Deep Focus** is a single-page productivity web app that helps you log and analyze deep work sessions. Inspired by Cal Newport's concept of distraction-free focused work, it gives you a clean timer interface, automatic session logging, streak tracking, and visual analytics — all without accounts, servers, or installations.

> Your data never leaves your browser. Everything is stored in `localStorage`.

---

## 🖥️ Preview

> _(Add a screenshot here: take one from your live app and drag it into the repo on GitHub)_

```
crafted-by-tarun.github.io/Deep-Focus/
```

---

## ✨ Features

### ⏱️ Focus Timer
- Large animated **SVG ring timer** with 60 tick marks
- Fills and glows **indigo** while running, turns **amber** when paused
- Name your session before you start (e.g. *"Study React Hooks"*)
- Full **Start → Pause → Resume → Save & Stop** flow

### 📋 Session Logging
- Every completed session is automatically saved with:
  - Session title
  - Category (Work / Study / Coding / Reading / Other)
  - Start time, end time, and total duration
- Filter history by **Today** or by **category**
- Delete any session

### 📊 Analytics Dashboard
- **3 stat cards** — total focus time today, session count, longest session
- **7-day bar chart** — drawn in pure HTML5 Canvas, today highlighted
- **Category breakdown** — horizontal bars showing time per category

### 🔥 Streaks & Motivation
- **Daily streak counter** — counts consecutive days with at least one session
- **Rotating daily quote** from focus & productivity thinkers (changes each day)

### 📱 Responsive Design
- Works on **mobile, tablet, and desktop**
- Dark theme with indigo accents and subtle gradients
- Clean card-based layout with smooth hover effects

---

## 🗂️ Project Structure

```
Deep-Focus/
├── index.html     ← The entire app — HTML, CSS, React, and charts in one file
└── README.md      ← You are here
```

> No `package.json`. No `node_modules`. No build step. Just one HTML file.

---

## 🛠️ Tech Stack

| Technology | Version | Purpose |
|---|---|---|
| **React** | 18.2 | UI components, state management, hooks |
| **SVG** | Native | Animated focus ring timer with tick marks |
| **HTML5 Canvas** | Native | 7-day bar chart — no chart library needed |
| **LocalStorage API** | Native | Persistent session data across page reloads |
| **Google Fonts** | CDN | Outfit (UI) + JetBrains Mono (numbers/code) |

> All React is loaded via **cdnjs CDN** — no npm, no Webpack, no Vite.

---

## 🏗️ Component Architecture

```
App
 ├── TopBar              — brand logo, streak chip, current date
 ├── TabNav              — Timer · Analytics · History
 │
 ├── [Timer Tab]
 │    ├── FocusTimer     — title input, category select, ring + controls
 │    │    └── TimerRing — SVG animated progress ring (60 tick marks)
 │    ├── SessionHistory — session list with filters + delete
 │    └── Sidebar
 │         ├── QuoteCard      — daily rotating motivational quote
 │         ├── TodayGlance    — quick stat summary
 │         └── CatBreakdown   — category horizontal bars
 │
 ├── [Analytics Tab]
 │    ├── StatChips      — total focus · sessions · longest today
 │    ├── BarChart       — 7-day canvas chart
 │    └── CatBreakdown   — all-time category breakdown
 │
 └── [History Tab]
      └── SessionHistory — full session log with category filter
```

---

## ⚙️ How the Timer Works

```
handleStart()  →  records startTs = Date.now()
                  setInterval fires every 500ms
                  elapsed = (now - startTs - pauseAccumulator) / 1000

handlePause()  →  records pauseStart = Date.now()
                  stops interval

handleResume() →  pauseAccumulator += (now - pauseStart)
                  restarts interval

handleStop()   →  builds session object { title, category, startTime, endTime, duration }
                  saves to localStorage
                  resets all state
```

---

## 📋 Session Categories

| Category | Color |
|---|---|
| 💼 Work | Indigo `#6c63ff` |
| 📖 Study | Cyan `#22d3ee` |
| 💻 Coding | Emerald `#10b981` |
| 📚 Reading | Amber `#f59e0b` |
| 📦 Other | Violet `#a78bfa` |

---

## 🚀 Run Locally

No terminal required — just open the file:

1. Download `index.html`
2. Double-click it to open in any browser
3. Start your first session ✅

---

## ☁️ Fork & Deploy

Want your own copy live on GitHub Pages?

1. Click **Fork** (top-right of this repo)
2. Go to **Settings → Pages**
3. Set Source → **Deploy from a branch → main → / (root)**
4. Click **Save**
5. Your app goes live at:
   ```
   https://YOUR-USERNAME.github.io/Deep-Focus/
   ```

---

## 🤝 Contributing

Found a bug or have a feature idea?

- Open an [Issue](../../issues)
- Or submit a [Pull Request](../../pulls)

All contributions are welcome!

---

## 📄 License

This project is open source under the [MIT License](LICENSE).

---

<div align="center">

<br/>

Built with ❤️ by [**crafted-by-tarun**](https://github.com/crafted-by-tarun)

<br/>

**⭐ Star this repo if Deep Focus helped you get into the zone!**

<br/>

</div>
