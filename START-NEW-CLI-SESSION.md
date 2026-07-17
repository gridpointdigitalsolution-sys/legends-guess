# ▶▶ START HERE IN CLAUDE CODE CLI — Legends Guess project

Read this whole file first, then read `HANDOVER.md`, `MEMORY.md`, `RESUME.md`, `RESEARCH-REPORT.md`, and open `07-legends-guess/index.html`. Everything needed to continue is in this folder.

---

## 0) COPY-PASTE THIS PROMPT INTO THE NEW CLI SESSION

> You are taking over an existing project called **Legends Guess**. Everything is in this folder (the "football lovers" folder). Before doing anything, READ these files fully: `START-NEW-CLI-SESSION.md`, `HANDOVER.md`, `MEMORY.md`, `RESUME.md`, `LAUNCH-GUIDE.md`, `RESEARCH-REPORT.md`, and the flagship app `07-legends-guess/index.html`. Then confirm back to me: (a) a 5-line summary of what the project is, (b) the current legend count, (c) the exact next 3 steps. The project is a free football+basketball "guess the legend, then watch highlights" web game monetized by Google AdSense, plus 4 more football apps to build later. Domain **legendsguess.com** is already registered on Hostinger. My immediate goals: (1) initialize a git repo here and push it to GitHub, (2) deploy `07-legends-guess/index.html` live to legendsguess.com, (3) create privacy.html/about.html/contact.html so I can pass AdSense review, (4) keep expanding the legend roster toward 1,000+ per sport in accuracy-first waves. Do NOT re-host or download any video — clips must stay as live search links/embeds (legal). Work directly in this folder, keep everything updated here, and don't stop to ask permission for routine steps — just do them and show me.

---

## 1) THE VISION (what we're building & why)
A portfolio of football-lover apps that give real value and make money via ads/subscriptions/affiliate. Research found the crowded spaces (livescore, generic news) are dead ends; we target low-competition, high-value angles. Flagship launched first: a daily **guess-the-legend game** (football + basketball) that unlocks **highlight clips** of each legend after you solve it — habit-forming, sharable, SEO-friendly, and monetized by Google AdSense. Clips are never hosted (legal): every "Watch" button opens the legend's real clips via a live YouTube/TikTok/Instagram search, so it's unlimited and never breaks.

## 2) THE 5 CORE APPS (from RESEARCH-REPORT.md)
1. **Daily football game** → evolved into the flagship **Legends Guess** (BUILT).
2. **Prediction game** (Superbru model): free pick'em for AFCON/NPFL/MLS; money from sponsors + betting affiliate + ads. (brief only)
3. **Fantasy AI tools** (MLS-first): paid AI assistant on top of free fantasy games; subscriptions. (brief only)
4. **Grassroots AI highlights**: phone films a match → AI highlights/stats; $20–40/mo per team. (brief only)
5. **Verified player CV + scouting** (Africa-first): anti-scam verified profiles + paid scout accounts. (brief only)
Plus two extras already built: **Legends Vault** (browse clips) and **Footy Guess** (original football-only puzzle).

## 3) WHAT'S DONE ✅
- Deep market research + 5 monetization ideas → `RESEARCH-REPORT.md`.
- **Legends Guess** flagship → `07-legends-guess/index.html`: 218 legends (138 football + 80 basketball), ⚽/🏀 toggle, guess-from-career (6 tries), welcome/how-to walkthrough, "6 guesses left" counter, **Watch-them-play** highlight buttons on solve/giveup, Daily + Endless modes, streaks, WhatsApp/X share grids, AdSense ad slots, privacy/about/contact placeholders, SEO meta. Single self-contained file, mobile-first.
- **Legends Vault** → `06-legends-clip-vault/index.html` (browse + filter + open clips).
- **Footy Guess** → `01-daily-football-game/index.html`.
- **Domain registered:** legendsguess.com (Hostinger, exp 2027-07-17, auto-renew on).
- Guides + handover: `LAUNCH-GUIDE.md`, `HANDOVER.md`, `MEMORY.md`, `RESUME.md`, `README.md`, `.gitignore`, `netlify.toml`, `PROJECT-STATUS.html`.

## 4) WHAT'S LEFT ⬜ (in order)
1. **Git:** init repo in this folder, push to GitHub (commands in RESUME.md).
2. **Deploy** `07-legends-guess/index.html` to legendsguess.com (Netlify GitConnect, or upload to Hostinger public_html).
3. **Set live URL:** change `const SITE='https://legendsguess.app'` in the game to the real URL.
4. **Legal pages:** create privacy.html, about.html, contact.html (REQUIRED for AdSense).
5. **Apply to AdSense**, paste publisher snippet into `<head>`.
6. **Roster wave 3+:** grow toward 1,000+/sport (accuracy-first). Add more Asia/Latam/women's/EuroLeague.
7. **Build App #2** (Prediction Game), then #3, #4, #5.

## 5) HOSTING / DOMAIN STATUS
- Registrar/host: **Hostinger**. Domain **legendsguess.com** active. Nameservers currently Hostinger's parking DNS.
- To go live: EITHER point nameservers to Netlify (if deploying via Git) OR use Hostinger hosting and upload the file to `public_html`. Both covered in LAUNCH-GUIDE.md.
- AdSense: approves at domain level → one approval covers all future subdomains (predict.legendsguess.com, etc.).

## 6) TECH & DATA MODEL
- All apps = single-file HTML/CSS/JS. No backend, no build step. Deploy = drop the file / point host at the folder.
- Flagship data = `DATA` array. Each entry: `{s:"⚽"|"🏀", n:name, f:flag, c:country, p:position, b:eraStartYear, cl:[clubs earliest→latest], q:"clip search query"}`.
- Clips: live search links (unbreakable, legal). Optional upgrade: add a real YouTube video ID to a legend to enable embedded in-app playback.
- Daily puzzle deterministic per date+sport (seeded RNG); Endless = random. Stats in localStorage (memory fallback).

## 7) GUARDRAILS (do not break)
- NEVER host/re-upload video — embed/link only.
- Roster accuracy first (a wrong career path = an unfair, broken puzzle).
- Keep ad density light (AdSense-friendly). Keep privacy/about/contact real before applying.

## 8) CURRENT COUNT
Football **138** + Basketball **80** = **218 legends**. Target: 500+/sport → 1,000+/sport.
