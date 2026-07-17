# Legends Guess — Football & Basketball apps (monorepo)

Live-ready web apps. Each app is a single self-contained `index.html` (no build step, no backend).

## Apps
| Folder | App | Status |
|---|---|---|
| `07-legends-guess/` | ⭐ Legends Guess — guess the ⚽/🏀 legend + watch highlights (218 legends) | READY — launch first |
| `06-legends-clip-vault/` | Legends Vault — browse legends, open their clips | READY |
| `01-daily-football-game/` | Footy Guess — original football-only puzzle | READY |
| `02-prediction-game/` | Prediction game (brief only) | TO BUILD |
| `03-fantasy-ai-tools/` | Fantasy AI tools (brief only) | TO BUILD |
| `04-grassroots-ai-highlights/` | Grassroots AI highlights (brief only) | TO BUILD |
| `05-player-cv-scouting/` | Player CV + scouting (brief only) | TO BUILD |

## Domain
Primary: **legendsguess.com** (registered at Hostinger). Plan: main domain = Legends Guess; other apps on subdomains later (all covered by one AdSense approval).

## Deploy (any of these)
- **Netlify/Vercel:** point at repo, publish directory = repo root, serve `07-legends-guess/index.html` as site root (or set base directory to `07-legends-guess`).
- **GitHub Pages:** enable Pages on this repo; put the flagship at root or use a subfolder.
- **Hostinger:** upload `07-legends-guess/index.html` as `index.html` in `public_html`.

See `LAUNCH-GUIDE.md` and `HANDOVER.md`.
