# 💅 gayify

**Mobile-first gay comedy website** with Monday-grade wit. Dry, sarcastic, hilarious on purpose — ChakkaAI is your overqualified reluctant bestie (think OpenAI’s Monday, but extremely gay).

**Compete on the web:** installable PWA, keyboard-safe composer, native share, offline shell, thumb-friendly UI. Private per-tab. Close = gone forever.

**🌐 Live:** [https://sauvira0.github.io/gayify/](https://sauvira0.github.io/gayify/)

[![Deploy to GitHub Pages](https://github.com/sauvira0/gayify/actions/workflows/deploy.yml/badge.svg)](https://github.com/sauvira0/gayify/actions/workflows/deploy.yml)

## What it is

**ChakkaAI** is the dry, gay groupchat narrator. **gayify** is the product.

- Monday-grade dry wit + queer comedy (Studio library + optional Live AI)
- **Multi-beat delivery** — main line → coven reaction → nosy follow-up
- **Anti-repeat** so the show doesn’t loop
- **6 personas** — Femme / Camp / Mystery / Daddy / Butch / Riot
- **Category Is** — 3-round ballroom game with scoreboard
- **Image gayification** — client-side canvas filters + captions
- **Ephemeral by design** — no accounts, no chat storage, no server history

## Mobile web (how we compete)

| Feature | Why |
|---------|-----|
| PWA + Add to Home Screen | Feels like an app without App Store |
| `visualViewport` keyboard handling | Composer stays usable on iOS/Android |
| 48px touch targets, 16px input | No accidental taps / no focus zoom |
| Compact header on small phones | More room for chat |
| Native `navigator.share` | One-tap WhatsApp / Messages |
| Offline shell (service worker) | Studio comedy still loads offline |
| Safe areas + notch padding | Real phones, not lab chrome |

**Privacy still ironclad:** service worker caches the *shell* only. Chat never hits disk.

## Run

**Hosted:** open the live link (best on your phone).

**Local:** serve the folder (needed for PWA/service worker):

```bash
python3 -m http.server 8080
# open http://localhost:8080
```

Or open `index.html` directly (no SW on `file://`).

## Architecture (do not break)

| Rule | Why |
|------|-----|
| Static site + optional SW | Zero backend, free Pages host |
| In-memory chat only | Safe WhatsApp group shares |
| Close tab = wipe | Privacy is the feature |
| Studio + gated Live AI | Funny offline; fresher online |

## Deploy

Push to `main` → GitHub Actions → GitHub Pages.

## Notes

Entertainment only. Be kind. Stay gay. Tip your drag queens.
