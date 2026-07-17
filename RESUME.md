# ▶ RESUME — pick up here in Claude Code CLI

## DONE
- [x] Market research + 5 money ideas (RESEARCH-REPORT.md)
- [x] Legends Guess flagship built — 218 legends, daily+endless, highlights, welcome guide, AdSense slots
- [x] Legends Vault + Footy Guess built
- [x] Domain registered: legendsguess.com (Hostinger)
- [x] Launch + AdSense guide written (LAUNCH-GUIDE.md)
- [x] Handover docs (this file, HANDOVER.md, MEMORY.md), git scaffolding (README, .gitignore, netlify.toml)

## NEXT (in order)
1. **Init + push git repo** (commands below), connect Hostinger/Netlify via GitConnect.
2. **Point legendsguess.com at the deploy**, serve 07-legends-guess/index.html as root.
3. **Set live URL:** in 07-legends-guess/index.html change `const SITE='https://legendsguess.app'` → your real URL.
4. **Create legal pages:** privacy.html, about.html, contact.html (needed for AdSense). Ask Claude to generate them.
5. **Apply to AdSense**, paste publisher snippet into <head>.
6. **Roster wave 3:** +100 accurate legends (more Asia, Latam, women's, EuroLeague) toward 1,000+.
7. Then build App #2 (Prediction Game).

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
