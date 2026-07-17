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
- [x] Wave 5: 480 (306 ⚽ / 174 🏀) — 90s/00s greats, Japan/Iran/India/Mexico, more WNBA
- [ ] Continue waves → 500 → 1,000 per sport (verify every club order + era before shipping)

## F. Deploy — Contabo VPS + Cloudflare Tunnel  (server DONE; 1 DNS record pending)
- [x] GitHub repo + live proof (GitHub Pages)
- [x] Isolated home on shared Contabo VPS (109.199.105.176): user `legendsguess` (uid 1002, no sudo/docker), /opt/legendsguess, systemd --user service, Node static server bound 127.0.0.1:3011 only. Deployed from gh-pages (git pull to update).
- [x] Cloudflare Tunnel ingress: added `legendsguess.com` + `www` → localhost:3011 in /root/.cloudflared/config.yml (above 404, VCC rules untouched, backup at config.yml.bak.legendsguess). cloudflared restarted, active. VCC health verified still ok.
- [ ] **PENDING (user, Cloudflare dashboard):** DNS for legendsguess.com must be **CNAME @ → 5acf974a-0b0e-48b1-8e0d-7428982d7d5e.cfargotunnel.com, Proxied (orange)**. Current record 530s = not routing to tunnel. Server can't set it (no cert.pem/API token on box). Once set, site is instantly live over HTTPS.
- Update live site after roster/code changes: push gh-pages, then on VPS `runuser -u legendsguess -- bash -lc 'cd /opt/legendsguess/site && git pull'`.

## Decisions locked
- VPS is the home (owner running paid ads, global spiky traffic). Cloudflare MUST sit in front.
- Never host video — live search links only.
- Roster accuracy first; a wrong career path = a broken puzzle.
- Opus 4.8 is sufficient; accuracy is a discipline (verify + test), not a model-tier issue.
