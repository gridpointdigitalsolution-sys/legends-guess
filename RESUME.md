# ▶ RESUME — pick up here in Claude Code CLI

## DONE (latest session — mobile-wow + image carousel + roster wave)
- [x] **Diagnosed why owner "saw no wow"** — viewed the LIVE site in-browser: (1) first-load welcome modal + cookie banner covered everything, (2) cursor-glow/3D-tilt were desktop-mouse-only → invisible on phone. Fixed both.
- [x] **Clue cards upgraded** — icon tiles (📍 position, 🏟️ club, 🌍 region, 🚩 nation, 📅 era), newest-revealed clue GLOWS gold + auto-pulses (mobile-visible, no mouse), all-clue entrance stagger.
- [x] **Hid AD placeholder boxes** (`.ad-slot{display:none}`) — no more "AD SPACE — activate after AdSense" half-built look. Re-enable when ads go live.
- [x] **Lighter first load** — removed the blocking welcome modal auto-open; game shows instantly; ❓ help button nudges new users; help modal still reachable.
- [x] **Bolder hero** — bigger tagline (1.62rem mobile / 2.15rem desktop) + drifting ⚽🏀 behind hero.
- [x] **Carousel redesign = image-forward** — big cards with generated **crest-avatars** (`legendAvatar()`: team-color gradient + player monogram + country code + sport ball, inline SVG data-URI). Football slides top row, basketball bottom. **Photo-ready**: `.mimg` can take real free-licensed (Wikimedia CC) portraits later. Section **gaps** added for launcher feel. Identical mobile + desktop.
- [x] **Roster +105 → 897 legends (549 ⚽ / 348 🏀)** — 2 parallel agents (football +60, basketball +45), validated: 0 schema errors, 0 dups, chronological clubs, flags matched. REGION += Jamaica/New Zealand/Switzerland. legends.html regenerated (897 cards).
- [x] All deployed → main + gh-pages + VPS pull, verified live on Cloudflare edge (http 200, new names + markers served).

## NEXT (open)
- [ ] **Real free-licensed faces (optional)** — source Wikimedia CC-BY/PD portraits for the ~36 featured carousel legends, drop URLs into a `img:` field → `.mimg` (fallback already = avatar). Needs per-image license check + attribution page. NO copyrighted/scraped photos (AdSense risk).
- [ ] **Keep roster growing** toward 1,000 ⚽ / 500 🏀 in accurate waves (need +451 ⚽ / +152 🏀).
- [ ] **GA4** — owner supplies Measurement ID (G-XXXX); snippet already in place (placeholder), loads only if set + cookies not declined.
- [ ] **Search Console** — owner supplies TXT/meta (use Digitalmindss01@gmail.com Cloudflare acct); submit sitemap https://legendsguess.com/sitemap.xml.
- [ ] **Owner: revoke the Cloudflare API token** that was pasted in chat earlier.
- [ ] Deploy flow reminder: git repo root = `legends-guess-repo/football-apps` (branch `main` → GitHub). VPS serves the **gh-pages** branch (app flattened at root) from `/opt/legendsguess/site`. Deploy = commit main → copy files into gh-pages worktree (`F:/Football LOvers/_ghp_wt`) → push gh-pages → `ssh vcc` (key `~/.ssh/vcc_contabo_ed25519`, ProxyCommand tunnel) → `sudo -u legendsguess git -C /opt/legendsguess/site pull --ff-only origin gh-pages`.

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
- [x] Roster waves 4-7 → 548 legends (374 ⚽ / 174 🏀).
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
