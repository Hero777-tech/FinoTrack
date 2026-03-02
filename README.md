# 📊 FinoTrak — Personal Finance & Investment Tracker

> *Built this because I was tired of maintaining 4 different Excel sheets for my FDs, gold, loans and insurance. Two weeks later — here we are.*

![FinoTrak Banner](https://img.shields.io/badge/FinTrak-v2.0-f4a830?style=for-the-badge&logo=data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCAyNCAyNCI+PHBhdGggZmlsbD0iI2Y0YTgzMCIgZD0iTTEyIDJMMiA3bDEwIDUgMTAtNS0xMC01ek0yIDE3bDEwIDUgMTAtNS0xMC01LTEwIDV6Ii8+PC9zdmc+)
![PWA](https://img.shields.io/badge/PWA-Ready-22c55e?style=for-the-badge)
![Platform](https://img.shields.io/badge/Platform-Android-3b82f6?style=for-the-badge)
![License](https://img.shields.io/badge/License-MIT-8b5cf6?style=for-the-badge)
![Made with](https://img.shields.io/badge/Made%20with-HTML%2FCSS%2FJS-f97316?style=for-the-badge)

<br>

**[🚀 Live Demo](https://hero777-tech.github.io/FinoTrack)** &nbsp;·&nbsp; **[📱 Install on Android](#-install-on-android)** &nbsp;·&nbsp; **[✨ Features](#-features)** &nbsp;·&nbsp; **[🗺️ Roadmap](#️-roadmap)**

<br>

---

## 🧠 The Story

I'm not a finance guy. I don't use Zerodha or Groww or any of the fancy investment apps. I have savings accounts in 3 different banks, a couple of FDs my dad convinced me to open, some gold my mom keeps track of in a diary, a home loan, and insurance policies I barely remember exist.

Every month I'd open 3 browser tabs, one Excel sheet, and WhatsApp my mom to ask how much the gold is worth. It was chaos.

So I spent **two weeks** building FinTrak — a single-page app that tracks everything in one place, works offline, and lives on my phone's home screen like a native app.

No sign-up. No cloud. No subscription. **Your data never leaves your phone.**

<br>

---

## ✨ Features

### 🏦 Banking
- Track **Savings, Current, FD, RD, PPF and NPS** accounts across all banks
- **AMB (Average Monthly Balance)** monitoring — get a red flag before your bank charges you
- Accordion UI grouped by bank — clean and easy to navigate

### 🔔 Smart Alerts
- **FD maturity warnings** — 30 days out (warning) and 7 days out (critical)
- **EMI due reminders** every month for all active loans
- **AMB breach alerts** — know before your bank does
- **Insurance expiry warnings** — no more accidentally lapsed policies

### 📊 Analytics
- **Net Worth Trend** — 6-month chart that auto-updates every time you open the app
- **Income vs Expense** bar chart — last 6 months at a glance
- **Asset Allocation** donut chart — see where your money actually is
- **Financial Health Score** — 0 to 100 score based on real parameters (EMI ratio, emergency fund, insurance, AMB)

### 💰 Income & Expense Tracker
- Log income and expenses with categories
- Monthly summary with net savings calculation
- Feeds directly into the dashboard charts

### 📅 Budget Planner
- Set monthly limits per category (Food, Transport, Rent, etc.)
- Visual progress bars showing how much of each budget you've used
- Pulls actual spending from your transaction log automatically

### 🎯 Savings Goals
- Set a target amount and target date
- Track how much you've saved toward each goal
- Progress bars + days remaining

### 🧮 FI Calculator Suite
- **FD Maturity Tracker** — see all your FDs and when they mature
- **RD Projection** — calculate maturity amount for recurring deposits
- **SIP Calculator** — project mutual fund SIP returns
- **Investment Growth Simulator** — with yearly/quarterly/monthly compounding options
- **Loan EMI Calculator** — calculate EMI, total interest, total payable
- **Retirement Corpus Planner** — inflation-adjusted corpus + monthly SIP needed

### 🪙 Other Trackers
- **Cash Holdings** — track physical cash at home, wallet, etc.
- **Metal Holdings** — gold, silver, platinum with weight, purity and estimated value
- **Insurance** — all policies in one place with sum assured and premium tracking
- **Loans** — repayment progress, outstanding amount, EMI tracking

### 🔐 Security & Settings
- **PIN Lock** — 4-digit PIN on app open (optional)
- **Dark / Light theme** — persists across sessions
- **Export / Import JSON** — full data backup and restore
- **Custom banks** — add any bank beyond the 6 defaults

<br>

---

## 📱 Install on Android

FinTrak is a **Progressive Web App (PWA)** — it installs on your Android home screen and works completely offline.

**Steps:**
1. Open **[https://Hero777-tech/FinoTrack](https://Hero777-tech/FinoTrack)** in **Chrome on Android**
2. Tap the **⋮ menu** (three dots, top right)
3. Tap **"Add to Home screen"** or **"Install app"**
4. Tap **"Install"**

That's it. FinTrak will appear on your home screen with its own icon, launch in fullscreen, and work offline from that point on.

> **Note:** Only works with Chrome on Android for PWA install. The web version works on any browser.

<br>

---

## 🛠️ Tech Stack

| Thing | What I used | Why |
|-------|-------------|-----|
| Frontend | Vanilla HTML + CSS + JS | No build step, no npm, no drama |
| Charts | [Chart.js](https://chartjs.org) | Easiest charting library I've found |
| Fonts | Playfair Display + DM Sans | Needed something that looked premium |
| Storage | localStorage | Data stays on device, no backend needed |
| PWA | Web App Manifest + Service Worker | Offline support + home screen install |
| Hosting | GitHub Pages | Free, fast, zero config |
| Icons | Python + Pillow (generated) | 8 sizes from 72px to 512px |

**Total dependencies: 2** (Chart.js + Google Fonts). Everything else is hand-written.

<br>

---

## 🗂️ Project Structure

```
fintrak/
├── index.html        ← Entire app (HTML + CSS + JS, single file)
├── manifest.json     ← PWA manifest (icons, theme, display mode)
├── sw.js             ← Service Worker (offline caching strategy)
├── README.md         ← You're here
└── icons/
    ├── icon-72.png
    ├── icon-96.png
    ├── icon-128.png
    ├── icon-144.png
    ├── icon-152.png
    ├── icon-192.png
    ├── icon-384.png
    └── icon-512.png
```

The whole UI, all the logic, all the styling — it's all in `index.html`. ~1700 lines. I know it's not "best practice" but it works great as a PWA and means there's literally one file to maintain.

<br>

---

## 🚀 Run Locally

No build step, no Node, no nothing:

```bash
# Clone the repo
git clone https://github.com/Hero777-tech/FinoTrack/
cd fintrak

# Option 1 — Python (built into most systems)
python3 -m http.server 8080

# Option 2 — Node (if you have it)
npx serve .

# Option 3 — VS Code
# Install "Live Server" extension → right click index.html → Open with Live Server
```

Then open `http://localhost:8080` in Chrome.

> ⚠️ Service Workers require a server (even local). Opening `index.html` directly as a `file://` URL won't register the SW — but the rest of the app will still work fine.

<br>

---

## 🔄 Updating the App (For My Reference)

Every time I push an update, I need to bump the cache version in `sw.js`:

```js
// Bump these on every release
const CACHE_NAME = 'fintrak-v3';       // ← change this
const STATIC_CACHE = 'fintrak-static-v3'; // ← and this
```

Users get the update automatically the next time they reopen the app. If it's urgent, the app shows an "Update Available" banner.

**Release log:**
- `v1.0` — Initial build (banking, FDs, loans, insurance, metals, cash)
- `v2.0` — Analytics, smart alerts, income/expense, budget planner, goals, FI suite, PIN lock, dark/light theme, PWA + onboarding

<br>

---

## 🗺️ Roadmap

Things I want to add when I get time:

- [ ] Mutual fund portfolio tracker (NAV lookup)
- [ ] Stock holdings tracker
- [ ] UPI transaction import (parse NPCI SMS)
- [ ] Bill reminders (electricity, broadband, etc.)
- [ ] Multi-currency support (for NRIs)
- [ ] Fingerprint / biometric unlock (WebAuthn)
- [ ] iCloud / Google Drive backup option
- [ ] iOS PWA improvements (Safari is a pain)
- [ ] Widget for home screen net worth (if browsers ever support this properly)
- [ ] Tax saving summary (80C, 80D investments at a glance)

PRs welcome if you want to take any of these on.

<br>

---

## 🤝 Contributing

This is a personal project but I'm happy to take contributions. A few guidelines:

1. **Keep it zero-dependency** (except Chart.js). No React, no Tailwind, no npm.
2. **Keep it a single HTML file** for the main app. Seriously.
3. **No backend, no accounts, no cloud sync.** Privacy is the whole point.
4. Open an issue first if you're planning something big — don't want to waste your time.

Bug fixes and small improvements → just open a PR directly.

<br>

---

## 🐛 Known Issues

- Service Worker on iOS Safari works but PWA install experience is manual (you have to "Add to Home Screen" from the Share menu — Apple things)
- Charts sometimes don't resize correctly when switching between landscape and portrait on older Android — working on it
- The FD maturity date calculation is off by 1 day in some edge cases around month-end FDs
- Export file has everything including the PIN hash — probably fine but worth knowing

<br>

---

## 📄 License

MIT — do whatever you want with it. If you build something cool on top of this, I'd love to see it.

<br>

---

## 🙏 Acknowledgements

- [Chart.js](https://chartjs.org) — genuinely the best charting library for projects like this
- [Google Fonts](https://fonts.google.com) — Playfair Display is beautiful
- Every Stack Overflow answer about Service Workers (there were many)
- My CA who kept telling me to "just maintain a proper record" — this is my answer

<br>

---

<div align="center">

**Built with frustration, caffeine, and an unhealthy interest in Indian banking quirks.**

*If this saved you from an AMB penalty, consider starring the repo ⭐*

</div>
