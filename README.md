# hAI Padel Americano 🎾🤖

> Smart tournament manager for **Padel Americano** – built for clubs, schools and Friday-night padel addicts.

<p align="center">
  <img src="https://img.shields.io/badge/padel-americano-22c55e?style=for-the-badge&logo=google-forms&logoColor=ffffff" alt="Padel Americano" />
  <img src="https://img.shields.io/badge/status-prototype-blue?style=for-the-badge" alt="Status Prototype" />
  <img src="https://img.shields.io/badge/license-MIT-green?style=for-the-badge" alt="MIT License" />
</p>

<p align="center">
  <img src="https://img.shields.io/github/languages/top/jbkunama1/hAI.PadelAmericano?color=38bdf8&label=main%20stack&style=flat-square" alt="Main Stack" />
  <img src="https://img.shields.io/github/repo-size/jbkunama1/hAI.PadelAmericano?style=flat-square&color=a855f7" alt="Repo size" />
</p>

---

## ✨ Features

- 🎲 **Americano scheduler** – generate doubles rounds with rotating partners & opponents.
- 📋 **Match editor** – enter scores per court and round.
- 🧮 **Live leaderboard** – individual ranking by points, matches and point difference.
- 🖥️ **Monitor mode** – full-screen friendly view for TV/beamers.
- 💾 **Offline first** – runs entirely in the browser, no backend required.
- 📦 **JSON import/export** – save and reload tournaments across browsers.

> Note: This repository currently ships the **client-side prototype**.

---

## 🚀 Quick start

### 1. Clone the repository

```bash
git clone https://github.com/jbkunama1/hAI.PadelAmericano.git
cd hAI.PadelAmericano
```

### 2. Open the app locally

Option A – double-click:

- Open `index.html` directly in your browser.

Option B – simple HTTP server:

```bash
python3 -m http.server 8000
```

Then open:

```text
http://localhost:8000/index.html
```

---

## 📦 Project structure

```text
hAI.PadelAmericano/
├── index.html      # Single-page app (SPA) – UI + logic
├── README.md       # English README
├── README.de.md    # Deutsche README
├── LICENSE_PLACEHOLDER_MIT
└── .gitignore
```

---

## 🧠 Tech stack

- **HTML5 + CSS3** (no framework)
- **Vanilla JavaScript** for scheduling & state management
- **JSON** import/export for persistent tournament data

No build tools, bundlers or package managers required.

---

## 🧪 Americano logic (high level)

- Players are entered as a simple list of names.
- The app creates **rounds** of doubles matches.
- If the number of players is not divisible by 4, one player per round may have a **bye**.
- After each match, points are added **per player**, not per team.
- The leaderboard uses total points, matches played and point difference.

Scheduling is heuristic: it aims for a fair mix of partners and opponents, not a mathematically perfect coverage.

---

## 📜 License (MIT)

This project is intended to be licensed under the **MIT License**, a widely used permissive open source license. It allows reuse, modification and distribution with minimal restrictions as long as copyright notice and license text remain. [web:46][web:47][web:50][web:53][web:56][web:59]

> ⚠️ For legal correctness, copy the official MIT license text from a trusted source (for example *choosealicense.com*) into the `LICENSE_PLACEHOLDER_MIT` file or replace it with a proper `LICENSE` file.
