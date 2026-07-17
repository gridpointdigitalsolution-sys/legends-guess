# 🤝 HANDOVER — Legends Guess project

**Owner:** Churchill Bracknell · **Domain:** legendsguess.com (Hostinger, registered 2026-07-17)
**Goal:** launch free football+basketball web games, monetize via Google AdSense, then build the other apps.

## What exists (all in this folder, all working)
1. **07-legends-guess/index.html** — FLAGSHIP. Guess the ⚽/🏀 legend from their career (6 tries), then "Watch them play" opens their real highlights (YouTube/TikTok/IG search — legal, unlimited, nothing hosted). 218 legends (138 football, 80 basketball). Daily + Endless modes, streaks, share grids, welcome/how-to, AdSense slots + privacy/about/contact placeholders. Mobile-first, single file.
2. **06-legends-clip-vault/index.html** — Browse legends, filter (Skills/Goals/Africa/era…), open their clips.
3. **01-daily-football-game/index.html** — Footy Guess (football-only original).
4. **02–05** — briefs only (README.md in each) for the next money apps.
5. **RESEARCH-REPORT.md** — market research + the 5 monetization ideas.
6. **LAUNCH-GUIDE.md** — domain → Netlify → AdSense, step by step.
7. **PROJECT-STATUS.html** — visual dashboard.

## How the flagship works (technical)
- Pure HTML/CSS/JS, one file. Data lives in the `DATA` array (fields: s=sport ⚽/🏀, n=name, f=flag, c=country, p=position, b=era year, cl=career clubs[], q=clip search query).
- Clips = live search links (never hardcoded video IDs → never breaks, always legal). Optional: add a real YouTube video ID to enable embedded in-app play.
- Daily puzzle is deterministic per date+sport (seeded RNG). Endless = random.
- Stats saved to localStorage (falls back to memory).

## Immediate next steps (see NEXT in RESUME.md)
1. Deploy 07-legends-guess to legendsguess.com.
2. Replace `SITE` constant in the JS (currently https://legendsguess.app) with the live URL.
3. Generate real privacy.html / about.html / contact.html (required for AdSense).
4. Add AdSense code snippet to <head> once you have your publisher ID.
5. Keep expanding the roster toward 1,000+ (accuracy-first waves).

## Masterpiece roadmap
Full world-class build plan + progress tracking lives in **ROADMAP.md** (UI/UX, PWA, AdSense files, analytics, roster waves, VPS+Cloudflare deploy). Update it as items ship.

## Guardrails / decisions locked in
- NEVER host/re-upload video. Embed or link only. (Copyright-safe.)
- AdSense needs: own domain (have it), privacy policy, about/contact, real content (the game counts), light ad density, a few days live before applying.
- One domain + subdomains covers all apps for AdSense.
