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
- [x] **Desktop layout** — responsive two-column "stage" (clues left / controls sticky right) at ≥980px, wider container, larger type; single column on mobile. Web-app for all browsers (no app-store build for now).
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
- [x] Wave 6: 480 (306 ⚽ / 174 🏀) — global football depth (Latam/Africa/Asia/USA/women/classics)
- [x] Wave 7: 548 (374 ⚽ / 174 🏀) — E.Europe/Scandinavia/Turkey/Africa/Asia/Latam/women/historic. ⚽ football now 374.
- [ ] Continue waves → 500 → 1,000 per sport (football focus; verify every club order + era before shipping)

## F. Deploy — Contabo VPS + Cloudflare Tunnel  ✅ LIVE (https://legendsguess.com)
- [x] GitHub repo + live proof (GitHub Pages backup)
- [x] Isolated home on shared Contabo VPS (109.199.105.176): user `legendsguess` (uid 1002, NO sudo/docker/root), /opt/legendsguess, Node static server bound **127.0.0.1:3011 only** via systemd --user service `legendsguess`. Site = git clone of gh-pages at /opt/legendsguess/site.
- [x] **Dedicated Cloudflare tunnel** `legendsguess` (id 774f20bb-fdf2-4e5d-818b-998110ee8674) under the OWNER's own Cloudflare account (Digitalmindss01) — NOT the shared VCC tunnel (cross-account, so VCC's 5acf974a tunnel couldn't serve it). Runs as the `legendsguess` user via systemd --user service `cloudflared-legendsguess`. Config/cert in /home/legendsguess/.cloudflared. DNS CNAME legendsguess.com + www → 774f20bb…cfargotunnel.com (Cloudflare does TLS).
- [x] Shared VCC tunnel config restored to pristine (my temp lines removed). VCC health verified still `ok`. Full isolation: never touched /opt/verifiedcarcheck, /root apps, other /opt/*.
- **Update live site after changes:** push to gh-pages, then `ssh -i ~/.ssh/vcc_contabo_ed25519 -o IdentitiesOnly=yes vcc "runuser -u legendsguess -- bash -lc 'cd /opt/legendsguess/site && git pull'"`.

## Decisions locked
- VPS is the home (owner running paid ads, global spiky traffic). Cloudflare MUST sit in front.
- Never host video — live search links only.
- Roster accuracy first; a wrong career path = a broken puzzle.
- Opus 4.8 is sufficient; accuracy is a discipline (verify + test), not a model-tier issue.
