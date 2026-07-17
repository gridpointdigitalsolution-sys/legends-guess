# 🚀 LAUNCH GUIDE — Get Legends Guess Live + AdSense (step by step)

This is the plain-English, do-it-once guide to put your game online for free and start the money process. Follow it top to bottom. No coding needed.

---

## PART 1 — Buy your domain (5 minutes, ~$10–12/year)

You need ONE domain you own. Google AdSense approves at the domain level, so this one domain covers ALL your apps on subdomains later.

1. Go to **namecheap.com** (or GoDaddy / Cloudflare — Namecheap is cheapest & easiest).
2. In the search box, type your name choice and press enter:
   - First choice: **legendsguess.com**
   - Backups if taken: **guessthelegend.com**, **playlegendsguess.com**, **legendsdaily.com**
3. When one shows a green **"Available"**, add it to cart and check out (~$10–12/year). Turn ON free "WhoisGuard/Domain Privacy" if offered.
4. Done — you own the domain. Keep the login safe.

> Tip: buy the .com. Grab a backup too if it's cheap.

---

## PART 2 — Put the game online for FREE (10 minutes, Netlify)

Netlify hosts your HTML free, gives HTTPS, and connects your domain.

1. Go to **netlify.com** → **Sign up** (use your Google account — fastest).
2. On the dashboard, look for **"Add new site" → "Deploy manually"** (it says "Drag and drop your site output folder here").
3. On your computer, open the folder **07-legends-guess** and **drag the whole folder** (with index.html inside) onto that box.
4. Netlify uploads it and instantly gives you a live link like `random-name-12345.netlify.app`. **Your game is already live** — open it to check.
5. Connect YOUR domain: **Site settings → Domain management → Add a domain** → type your domain (e.g. legendsguess.com) → follow the on-screen steps. Netlify tells you 2 things to paste into Namecheap:
   - In Namecheap: **Domain List → Manage → Nameservers → Custom DNS** → paste the Netlify nameservers they show you → Save.
6. Wait 15 min – a few hours for it to connect. Netlify auto-adds free HTTPS (the padlock). Now **https://legendsguess.com** shows your game. 🎉

> To update the game later: just drag the updated folder onto Netlify again. That's it.

---

## PART 3 — Before you apply to AdSense (do these — they decide approval)

Google rejects thin/empty sites. Tick these first:

- ✅ **Own domain live** (Parts 1–2 done) — not a free .netlify.app address.
- ✅ **Real content on the page** — your game IS interactive original content (good). 
- ✅ **Privacy Policy page** — REQUIRED. (The game has a Privacy link; before applying, replace it with a real privacy page. I can generate a full privacy.html + about.html + contact.html for you — just ask.)
- ✅ **About page + Contact email** — add a real email in the Contact link.
- ✅ **Some traffic + a few days of the site being live** — don't apply the same hour you launch. Give it a few days and share it so real people visit.
- ✅ **Clean, not ad-spammy** — we kept ad slots minimal on purpose. Good.

---

## PART 4 — Apply to Google AdSense (10 minutes)

1. Go to **adsense.google.com** → **Sign up** with your Google account.
2. Enter your website: **legendsguess.com** and your country. Accept terms.
3. AdSense gives you a **code snippet**. You paste it once into the site `<head>` (I'll add the exact spot for you when you have your AdSense ID — just send it).
4. In Namecheap/Netlify nothing else needed. Submit for review.
5. **Wait**: review takes a few days up to ~2–4 weeks. You'll get an email: approved or "needs work."
   - If rejected, the email says why (usually "not enough content" or "missing privacy policy"). Fix that item and re-apply — re-applying is normal and free.
6. Once approved, ads appear in the slots we built. You earn per view/click. Payout starts once you reach Google's threshold (usually $100).

---

## PART 5 — After approval: scale the money

- Add the **other football apps** on subdomains (predict.legendsguess.com, etc.) — one AdSense account covers them all.
- Drive traffic: share daily result grids in WhatsApp groups, football/basketball TikTok, Reddit, X. The built-in share buttons are your growth engine.
- Add more legends & puzzle types (ongoing — see ROADMAP below) to keep people coming back daily = more ad views.

---

## ROADMAP — growing to 1,000+ puzzles (honest plan)

The game engine already supports unlimited legends and unlimited clips (every legend's highlights come from a live search, so each one already has hundreds of real clips going back to the 1990s — nothing is hardcoded, nothing breaks).

To reach 1,000+ puzzles we grow the legend roster in **waves** (accuracy first — a wrong career path makes an unfair puzzle, so each legend is added carefully):
- **Now:** 58 football + 51 basketball legends live and playable, plus Endless mode = unlimited rounds.
- **Next waves:** add ~100 legends per wave (more African, Asian, South American, women's football, classic NBA, EuroLeague, WNBA), each with an accurate career path and a sharpened clip query.
- **Target:** 500+ per sport, then 1,000+, plus extra puzzle formats (guess-by-trophies, guess-the-moment) that multiply total puzzles.

I keep every update saved in this same **football-apps** folder, app by app, so it's always current on your side.

---

*Need me to auto-generate privacy.html, about.html and contact.html so you're 100% AdSense-ready? Say the word and they'll be in the 07-legends-guess folder.*
