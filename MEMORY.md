# 🧠 MEMORY — context for continuing in Claude Code CLI

## Project identity
- Name: **Legends Guess** (portfolio brand for football + basketball fan apps).
- Domain: **legendsguess.com** (Hostinger). Backups considered: guessthelegend.com, playlegendsguess.com.
- Public contact email: hello@legendsguess.com (used in app privacy/contact pages).

## Product decisions
- Flagship = Legends Guess (guess-the-legend + integrated highlights).
- Two sports in one app: ⚽ Football and 🏀 Basketball (toggle).
- Monetization = Google AdSense first (free to users). Later: affiliate/sponsors on other apps.
- Clips via LIVE SEARCH links only — no hosting, no hardcoded IDs. Legal + unbreakable.
- Grow roster in accurate waves (wrong career = broken puzzle). Currently 548 legends.
- **LIVE at https://legendsguess.com** (Contabo VPS + dedicated Cloudflare tunnel under owner account; isolated `legendsguess` user). Web-app only for now — no Play Store / App Store yet (later feature). Must work for any desktop + mobile browser.

## Data model (07-legends-guess DATA array)
{s:"⚽"|"🏀", n:name, f:flag, c:country, p:position, b:eraStartYear, cl:[clubs earliest→latest], q:"clip search query"}

## Masterpiece roadmap
- Full world-class plan + live progress = **ROADMAP.md** (UI/UX pass, PWA, AdSense compliance files, analytics, roster waves, VPS+Cloudflare deploy).
- Deploy target = owner's **VPS with Cloudflare in front** (not plain static host — owner runs paid ads → spiky global traffic). Cloudflare CDN is non-negotiable.

## Roster status
- Football: 374 · Basketball: 174 · TOTAL: 548 (after wave 7). Football expanding further (owner priority); basketball healthy.
- Target: 500+/sport → 1,000+/sport, plus extra puzzle formats (guess-by-trophies, guess-the-moment).
- Coverage so far: modern stars, 90s/2000s classics, strong African set, some Asian/Latam, women's football (Marta, Rapinoe, Morgan, Sam Kerr, Bonmati…), NBA classics + WNBA (Taurasi, A'ja Wilson, Caitlin Clark…).

## Tech
- Single-file HTML apps. No backend, no build. Deploy = drop the file / point host at folder.
- localStorage for stats (graceful fallback).

## Style
- Dark UI. Football accent = green (#22c55e). Basketball accent = orange (#f97316). Inter font.
