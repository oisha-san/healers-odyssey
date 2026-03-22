# 🩺 Healer's Odyssey

**A lifelong medical study RPG.** Level up through 38 specialties, 1,784+ diseases, AI-powered USMLE quizzes, spaced repetition, boss battles, and more — all in a single HTML file with no install required.

**Live site:** [https://oisha-san.github.io/healers-odyssey/](https://oisha-san.github.io/healers-odyssey/)

---

## What it is

Healer's Odyssey turns medical study into an RPG progression system. Every topic you study, every review you complete, every quiz you pass earns XP and pushes you up a level curve that mirrors a real medical education timeline — from Anatomy at Level 1 to Medical Education at Level 102. It is designed to be used daily, for years.

---

## Features

### 🎓 Core Progression
- **38 medical specialties** unlocking progressively from Level 1 to Level 102
- **1,784+ diseases and topics** across all specialties
- **Quadratic XP curve** — designed so Level 102 takes roughly the time of a real medical education
- **Skill Points** earned on level-up, spent on 5 permanent ability upgrades
- **Prestige system** — reset at Level 102 up to 5 times, keeping all topics and achievements, gaining +15% XP permanently per prestige (up to +75%)
- **19 earned titles** that update dynamically based on real achievements (streak, mastery, prestige)
- **Profile picture** that evolves at milestone levels

### 🧠 Learning Engine
- **Spaced repetition** with 8 review intervals (1 → 3 → 7 → 14 → 30 → 60 → 120 → 180 days)
- **Confidence rating** on every topic — 🔴 Shaky, 🟡 OK, 🟢 Solid — directly adjusts your review interval
- **Knowledge decay colouring** — topics turn orange then red as they go overdue in the specialty list
- **Smart review sort** — most overdue and least confident topics surface first
- **Custom topics** — add your own diseases to any specialty
- **Study notes** — personal mnemonics and clinical pearls per topic
- **Flashcard mode** — active recall across all studied topics or shaky-only filter

### 🤖 AI Features (powered by Claude)
- **USMLE-style AI quiz** — 4 clinical vignettes per session, Step 1/2 difficulty, sourced from Harrison's and UpToDate standards
- **Boss Battles** — 5 harder USMLE questions triggered at Levels 20, 36, 51, 80, and 102. One-time only — fail and it's recorded permanently
- **AI Study Planner** — 7-day personalised schedule based on your weak specialties and exam countdown

### ⚔️ RPG Systems
- **Hot Streak Combo** — study multiple topics in a session for 1.5× → 2× → 3× XP multipliers
- **5 skill upgrades** (each with 5–10 levels):
  - 🎯 **Scholar's Focus** — up to +80% XP from all sources
  - 🔗 **Iron Memory** — up to +30 XP per completed review
  - 🔥 **Momentum** — your streak multiplies all XP (up to +50% at a 100-day streak)
  - 💡 **Deep Understanding** — up to +150% XP bonus when you rate a topic 🟢 Solid
  - ⏩ **Time Compression** — up to 40% shorter spaced repetition intervals
- **160+ achievements** across 15 categories, all collapsible by category
- **Boss Battle record** — win/loss permanently saved per boss
- **Streak Freezes** — buy with SP to protect your streak on missed days (max 3)

### 📅 Daily & Monthly Challenges
- **4 daily tasks** generated each day from a pool of 8 types, with random difficulty tiers (Easy / Medium / Hard / Brutal)
- **Perfect Day bonus** — complete all 4 daily tasks for +2 SP on top of individual rewards
- **3 monthly challenges** each month from a pool of 7 types, also with random difficulty
- Both systems track: questions answered, topics studied, reviews, focus sessions, AI quizzes, Solid ratings, and levels gained
- Task cards show live progress bars, difficulty badges, and flavour text

### 📊 Progress Tracking
- **Full-year activity heatmap** — GitHub contribution graph layout, navigable back through every year you've used the app, with daily tooltips
- **Mastery Radar Chart** — SVG spider chart across 10 specialty axes in your stats modal
- **Weekly digest** — XP, topics, questions, and reviews for the current week
- **Personal records** — most topics, questions, and XP in a single day
- **Quiz history** — all-time accuracy per topic from AI quizzes

### ⏱ Study Tools
- **Focus Timer** — 25-minute Pomodoro with start / pause / resume / reset, +50 XP on completion
- **Clinical Case of the Day** — a seeded daily topic with 3× XP bonus
- **Daily Check-in** — streak tracking with milestone bonuses (SP at 30, 100, 365 days)
- **Exam Countdown** — set your board exam date and see a colour-coded countdown in the header
- **Browser notifications** — review reminders even when the tab is closed

### 🎵 Music
- **12-track playlist** — 9 tracks by [Scott Buckley](https://www.scottbuckley.com.au) (CC BY 4.0) and 3 by [Kevin MacLeod](https://incompetech.com) (CC BY 3.0)
- **Shuffle and repeat modes** — shuffle, repeat all, or repeat one
- **Track selector dropdown** with artist credit

### 🔗 Integrations
- **Cloud sync** via [JSONBin.io](https://jsonbin.io) — save and load your progress across devices with a free account
- **AnkiConnect** — sync your Anki desktop reviews as questions in Healer's Odyssey (requires the [AnkiConnect plugin](https://ankiweb.net/shared/info/2055492159) and CORS config — see below)

---

## Getting Started

1. Visit the [live site](https://oisha-san.github.io/healers-odyssey/) or download `index.html` and open it in any browser
2. Click **☀️ Check-in** to start your streak and earn your first XP
3. Unlock **Anatomy** at Level 1 — tick off topics as you study them, rating your confidence each time
4. Your first spaced repetition reviews will appear in the **Reviews** section the following day

---

## Anki Integration Setup

1. Install the [AnkiConnect plugin](https://ankiweb.net/shared/info/2055492159) in Anki (code: `2055492159`)
2. In Anki → **Tools → Add-ons → AnkiConnect → Config**, update the CORS list:
```json
{
    "webCorsOriginList": [
        "http://localhost",
        "https://oisha-san.github.io"
    ]
}
```
3. Restart Anki fully
4. In Healer's Odyssey → **Settings → Anki Integration** → click **🔌 Test Connection**
5. Cards you review in Anki will sync as questions — counting toward Question Blitz, The Gauntlet, and the monthly Question Marathon challenge

---

## Cloud Sync Setup

1. Create a free account at [jsonbin.io](https://jsonbin.io)
2. Go to **API Keys** and copy your Master Key
3. In Healer's Odyssey → **Settings → Cloud Sync** → paste your key and click **🔑 Connect**
4. Click **☁️ Save to Cloud** / **📥 Load from Cloud** to sync across devices

---

## Hosting on GitHub Pages

1. Fork or upload `index.html` to a GitHub repository
2. Go to **Settings → Pages → Deploy from branch → main → / (root)**
3. Your site will be live at `https://YOUR-USERNAME.github.io/REPO-NAME/`

---

## Tech Stack

- Vanilla JavaScript, HTML5, CSS3 — no build step, no dependencies
- [Tone.js](https://tonejs.github.io/) for sound effects
- [Claude API](https://www.anthropic.com/) (`claude-sonnet-4-20250514`) for USMLE quizzes, boss battles, and study planner
- [JSONBin.io](https://jsonbin.io) for cloud saves
- [AnkiConnect](https://foosoft.net/projects/anki-connect/) for Anki integration

---

## Music Credits

**Scott Buckley** — [scottbuckley.com.au](https://www.scottbuckley.com.au) — CC BY 4.0
Echoes Of Home · Undertow · I Walk With Ghosts · Horizons · Penumbra · Amberlight · Wildflowers · Memories Of Stone · Legionnaire

**Kevin MacLeod** — [incompetech.com](https://incompetech.com) — CC BY 3.0
Lost Frontier · Deliberate Thought · Long Road Ahead

---

## License

MIT — free to use, modify, and distribute.
