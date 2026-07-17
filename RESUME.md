# ▶ RESUME — pick up here in Claude Code CLI

## DONE
- [x] Market research + 5 money ideas (RESEARCH-REPORT.md)
- [x] Legends Guess flagship built — 218 legends, daily+endless, highlights, welcome guide, AdSense slots
- [x] Legends Vault + Footy Guess built
- [x] Domain registered: legendsguess.com (Hostinger)
- [x] Launch + AdSense guide written (LAUNCH-GUIDE.md)
- [x] Handover docs (this file, HANDOVER.md, MEMORY.md), git scaffolding (README, .gitignore, netlify.toml)

## DONE (2026-07-17 CLI session)
- [x] **Git repo pushed** → https://github.com/gridpointdigitalsolution-sys/legends-guess (branch `main`).
- [x] **Live now** via GitHub Pages → https://gridpointdigitalsolution-sys.github.io/legends-guess/ (served from `gh-pages` branch, flagship at root). Proof-of-life while domain DNS is pointed.
- [x] **Legal pages built + wired** — 07-legends-guess/{privacy,about,contact}.html (real content, dark theme). Footer links now point to real pages (removed the old alert() popups).
- [x] **Live URL set** — `const SITE='https://legendsguess.com'` in the flagship.

## DONE (masterpiece session)
- [x] UI/UX world-class pass — Bricolage/Sora fonts, gradient-mesh bg + grain, staggered motion, confetti, streak flame, shareable result image, sound+haptics, a11y focus. Verified via jsdom smoke test (0 errors) + live.
- [x] PWA — manifest, service worker, generated icons (192/512/maskable/apple-touch), favicon.svg, install button.
- [x] Compliance files — robots.txt, sitemap.xml, ads.txt, 404.html, cookie-consent banner. OG social card (1200×630).
- [x] Roster waves 4 + 5 + 6 → 548 legends (374 ⚽ / 174 🏀).
- [x] **DEPLOYED LIVE** → https://legendsguess.com (Contabo VPS, dedicated Cloudflare tunnel under owner's account, isolated `legendsguess` user). VCC untouched.
- [x] **Desktop polish** — responsive two-column layout ≥980px + mobile. Web-app for all browsers (no app store yet).
- [x] Email → hello@legendsguess.com everywhere (Gridpoint refs removed).
- See **ROADMAP.md** for the full checklist + what remains.

## NEXT (in order, post-live)
1. **Apply to Google AdSense** — site is live; wait a few days, then apply. On approval: paste publisher `<script>` into `<head>` of index + about/privacy/contact, fill the ads.txt line, activate the 3 AD SPACE slots.
2. **Analytics** — GA4 or Plausible (owner picks) to measure promo traffic.
3. **hello@legendsguess.com mailbox** — create on host (add MX record; already referenced in pages).
4. **SEO** — per-legend / programmatic pages for organic traffic (big lever, later phase).
5. **Roster** — keep expanding football in accuracy waves (owner priority) → 500 → 1,000/sport.
6. Later: App #2 (Prediction Game); optional app-store wrap.

## UPDATE THE LIVE SITE after code/roster changes
```bash
# 1) commit to main, then sync flagship to gh-pages branch, then:
ssh -i ~/.ssh/vcc_contabo_ed25519 -o IdentitiesOnly=yes vcc \
  "runuser -u legendsguess -- bash -lc 'cd /opt/legendsguess/site && git pull'"
```
(gh-pages branch = the flat web root the VPS serves. Static Node server reads files live — no restart needed.)

## Quick test locally
Open `07-legends-guess/index.html` in a browser. Pick a sport, guess, watch the name tiles + highlights unlock.
