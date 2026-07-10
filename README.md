# 💅 gayify

**World-class gay comedy chat.** Type anything → get multi-beat theatrical chaos. Upload a pic → get gayified. Private per-tab. Close = gone forever.

Built to feel like a product, not a toy: cinematic demo, roast/ballroom games, persona theater, local comedy engine + optional free AI layer.

**🌐 Live:** [https://sauvira0.github.io/gayify/](https://sauvira0.github.io/gayify/)

[![Deploy to GitHub Pages](https://github.com/sauvira0/gayify/actions/workflows/deploy.yml/badge.svg)](https://github.com/sauvira0/gayify/actions/workflows/deploy.yml)

## What it is

**ChakkaAI** is the unhinged groupchat narrator. **gayify** is the product.

- Over-the-top English gay comedy (yasss, periodt, shade, realness, coven energy)
- **Multi-beat delivery** — main line → coven reaction → nosy follow-up
- **6 personas** — Femme / Camp / Mystery / Daddy / Butch / Riot
- **Games** — Roast Me, Category Is, Hot Seat, Spill Tea, Go Off, Vibe Roulette
- **Image gayification** — canvas filters, sparkles, gold tags, stealable captions
- **Slay system** — levels, badges, diary, meme + story export
- **Ephemeral by design** — no accounts, no localStorage, no server chat history

## Run

**Hosted:** open the live link above.

**Local:** open `index.html` in a browser (or any static server). No build step. No npm.

## Architecture (do not break)

| Rule | Why |
|------|-----|
| Single file `index.html` | Zero deploy friction, viral forkability |
| In-memory state only | Safe to share in WhatsApp groups |
| Close tab = wipe | Privacy is the feature |
| Local comedy + optional LLM | Funny offline; fresher online |
| Direct pic upload | No attach-then-send friction |

## Features

- Splash entrance + cinematic **Demo** button
- Thumb-friendly persona rail + live theme accents
- AI toggle (OpenRouter free model) with retry/timeout/offline fallback
- Per-message AI badges when LLM wins
- Session short-term memory for callbacks (tab only)
- Trophy case, Gay Diary, burn session, share copy
- Mobile-first velvet club aesthetic (Bricolage Grotesque + Outfit)

## Privacy

Everyone who opens the link gets an **isolated** chat. Nothing is written to disk. Refresh = fresh start. The share blurb and story exports say so out loud.

## Deploy

Push to `main` → GitHub Actions → GitHub Pages (see `.github/workflows/deploy.yml`).

## Notes

Entertainment only. Be kind. Stay gay. Tip your drag queens.

Made to compete with the best AI-built demos — personality product, not productivity cosplay.
