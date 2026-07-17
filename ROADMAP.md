# 🎯 MASTERPIECE ROADMAP — Legends Guess

Single source of truth for "make it world-class." Check items off as they ship. Do them **step at a time, accuracy-first**. Finish this app fully before moving to App #2.

Legend: [x] done · [~] in progress · [ ] todo

## A. UI/UX world-class pass  (DONE — verified via jsdom smoke test, live)
- [x] Distinctive typography — display font (Bricolage Grotesque) + Sora body; dropped generic Inter
- [x] Atmospheric background — stadium-night gradient mesh + grain/noise, depth, premium dark theme
- [x] Motion — staggered clue reveals, win **confetti**, right/wrong feedback, modal transitions, sheen, micro-interactions
- [x] Redesigned result screen + **streak flame** meter (flickers at streak >=2)
- [x] Auto-generated shareable **RESULT IMAGE** (canvas → PNG, spoiler-free) + Save-image button
- [x] Sound effects (WebAudio) + toggle (persisted), mobile haptics
- [x] Accessibility — :focus-visible rings, ARIA labels, prefers-reduced-motion honoured
- [ ] (Optional) light/dark toggle — deferred (dark theme is the brand)

## B. PWA / app-like  (DONE)
- [x] manifest.webmanifest, service worker sw.js (offline shell cache), install prompt (⬇️ button)
- [x] App icons — 192 / 512 / maskable / apple-touch, favicon.svg + favicon-32.png (generated via node PNG encoder)
- [x] OG social preview image (1200×630) — WhatsApp/X shares show a real branded card

## C. AdSense / compliance files
- [x] privacy.html / about.html / contact.html (real content, footer-wired)
- [x] robots.txt, sitemap.xml, ads.txt (publisher id added post-approval), 404.html
- [x] cookie-consent banner (EU + AdSense personalized ads)
- [ ] Swap contact email to pro address — **PENDING user pick: hello@ vs support@legendsguess.com**
- [ ] Apply to AdSense (after domain live a few days) → paste publisher `<script>` into all pages → activate AD SPACE slots

## D. Traffic engine
- [ ] Analytics (measure promos) — GA4 or Plausible snippet (placeholder wired, id later)
- [ ] SEO: per-legend content / programmatic pages (later phase, big organic-traffic lever)

## E. Roster expansion — accuracy-first waves toward 1,000+/sport
- [x] Wave 1+2: 218 (138 ⚽ / 80 🏀)
- [x] Wave 3: 300 (186 ⚽ / 114 🏀)
- [x] Wave 4: 380 (226 ⚽ / 154 🏀) — historic greats, EuroLeague, women's, Asia/Latam/Africa
- [x] Wave 5: 420 (246 ⚽ / 174 🏀) — 90s/00s greats, Japan/Iran/India/Mexico, more WNBA
- [ ] Continue waves → 500 → 1,000 per sport (verify every club order + era before shipping)

## F. Deploy — VPS + Cloudflare  (PENDING user VPS settings)
- [x] GitHub repo + live proof (GitHub Pages)
- [ ] VPS: nginx server-block, deploy files, SSL (certbot/Cloudflare)
- [ ] **Cloudflare in front** (free plan) — CDN cache + DDoS shield so promo traffic hits cache not origin. NON-NEGOTIABLE.
- [ ] Point legendsguess.com → Cloudflare → VPS origin

## Decisions locked
- VPS is the home (owner running paid ads, global spiky traffic). Cloudflare MUST sit in front.
- Never host video — live search links only.
- Roster accuracy first; a wrong career path = a broken puzzle.
- Opus 4.8 is sufficient; accuracy is a discipline (verify + test), not a model-tier issue.
