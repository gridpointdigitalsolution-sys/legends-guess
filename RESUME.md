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

## NEXT (in order)
1. **Point legendsguess.com at the deploy** (needs Hostinger/Netlify dashboard — see LAUNCH-GUIDE.md):
   - EASIEST: Netlify → "Add new site → Import from Git" → pick `legends-guess` repo → publish dir auto-reads `07-legends-guess` from netlify.toml → deploy → "Domain settings → add legendsguess.com" → follow Netlify DNS records → in Hostinger set nameservers/records to Netlify. OR
   - Hostinger direct: upload the 4 files in 07-legends-guess/ to `public_html`.
   - After custom domain works, add a CNAME file in gh-pages OR just rely on the host; keep GitHub Pages as backup.
2. **Apply to AdSense** once legendsguess.com is live a few days; paste publisher `<script>` into `<head>` of index.html + all 3 legal pages, then activate the AD SPACE slots.
3. **Roster wave 3:** +100 accurate legends (more Asia, Latam, women's, EuroLeague) toward 1,000+.
4. Then build App #2 (Prediction Game).

## GIT — create & push (run in the football lovers folder on F:)
```bash
cd /path/to/football-lovers        # your F: football lovers folder
git init
git add .
git commit -m "Legends Guess: 218-legend football+basketball game + vault + docs"
git branch -M main
# create empty repo on GitHub first (github.com/new), then:
git remote add origin https://github.com/<your-username>/<repo>.git
git push -u origin main
```
Then in Netlify/Hostinger: "Import from Git" → pick the repo → set base/publish to `07-legends-guess` (or root) → deploy → add domain legendsguess.com.

## Quick test locally
Open `07-legends-guess/index.html` in a browser. Pick a sport, guess, watch highlights unlock.
