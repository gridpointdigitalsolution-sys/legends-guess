# 🎯 MASTERPIECE ROADMAP — Legends Guess

Single source of truth for "make it world-class." Check items off as they ship. Do them **step at a time, accuracy-first**. Finish this app fully before moving to App #2.

Legend: [x] done · [~] in progress · [ ] todo

## A. UI/UX world-class pass  (IN PROGRESS — this session)
- [~] Distinctive typography — display font (Bricolage Grotesque) + refined body; drop generic Inter look
- [~] Atmospheric background — stadium-night gradient mesh + grain/noise, depth, premium dark theme
- [~] Motion — staggered clue reveals, win **confetti**, right/wrong feedback, modal transitions, micro-interactions
- [~] Redesigned result screen + **streak flame** meter
- [~] Auto-generated shareable **RESULT IMAGE** (canvas → PNG) for viral promo sharing
- [~] Sound effects + toggle, mobile haptics
- [ ] Accessibility pass — keyboard, ARIA labels, contrast, visible focus states
- [ ] (Optional) light/dark toggle

## B. PWA / app-like
- [~] manifest.webmanifest, service worker (offline cache), install prompt
- [~] App icons — 192 / 512 / maskable / apple-touch, favicon.svg + favicon.png
- [~] OG social preview image (1200×630) — so WhatsApp/X shares show a real card

## C. AdSense / compliance files
- [x] privacy.html / about.html / contact.html (real content, footer-wired)
- [~] robots.txt, sitemap.xml, ads.txt (publisher id added post-approval), 404.html
- [~] cookie-consent banner (EU + AdSense personalized ads)
- [ ] Swap contact email to pro address — **PENDING user pick: hello@ vs support@legendsguess.com**
- [ ] Apply to AdSense (after domain live a few days) → paste publisher `<script>` into all pages → activate AD SPACE slots

## D. Traffic engine
- [ ] Analytics (measure promos) — GA4 or Plausible snippet (placeholder wired, id later)
- [ ] SEO: per-legend content / programmatic pages (later phase, big organic-traffic lever)

## E. Roster expansion — accuracy-first waves toward 1,000+/sport
- [x] Wave 1+2: 218 (138 ⚽ / 80 🏀)
- [x] Wave 3: 300 (186 ⚽ / 114 🏀)
- [~] Wave 4: +80 (parallel agent) → ~380
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
