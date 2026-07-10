# gayify / ChakkaAI — Current App State

**Snapshot:** World-class comedy product upgrade (compete with Fable-tier demos). Full single-file rewrite with multi-beat theater, games, splash, distinctive club/ballroom UI.

**Live:** https://sauvira0.github.io/gayify/  
**Repo:** https://github.com/sauvira0/gayify

## Ironclad rules (DO NOT CHANGE)

- Pure client-side: one `index.html` (Tailwind CDN + vanilla JS + Font Awesome + Google fonts).
- **No** localStorage, sessionStorage, cookies, IndexedDB.
- All state in JS memory: messages, gayMoments, badges, sessionMemory, slayScore, etc.
- Close tab / refresh = gone. Isolated per tab.
- Images stay in-browser (FileReader → canvas).
- Direct upload flow (no attach-then-send).

## What ships now

### Comedy engine
- Expanded special-case replies + replacements + theatrical full rewrites when no word hits
- Persona wrappers (6 vibes) mutate language
- **Multi-beat delivery:** main response → optional coven side-chat → optional follow-up/callback
- Short **sessionMemory** (last 8) for callbacks + LLM context (still ephemeral)

### Games
- Roast Me, Category Is, Hot Seat, Spill Tea, Go Off, Vibe Roulette
- Demo = cinematic scripted multi-beat showcase

### Image
- Vibe sampling, persona filters, sparkles, bokeh, gold tag, border
- Side-by-side original/gayified, captions, re-gay, rate

### Gamification
- Slay score, levels, streak, badges, diary, meme card, story export, share text
- Level-up overlay + confetti + chimes

### AI
- OpenRouter `openrouter/free`, baked demo key, toggle, retry, 10s timeout, offline/auth fallback to local engine
- System prompt includes persona voice + recent memory

### UI
- Splash: “ENTER THE FUNCTION”
- Fonts: Bricolage Grotesque + Outfit (not Inter)
- Velvet club palette: void black, hot pink, gold, mint
- Persona theme CSS variables
- Bottom sheets, toasts, mobile composer, games rail

## Files

- `index.html` — entire product
- `README.md` — public docs
- `CURRENT_APP_STATE.md` — this file
- `.github/workflows/deploy.yml` — Pages deploy

## How to test

1. Open `index.html`
2. Enter splash → Demo button
3. Text chat (AI on/off)
4. Roast Me / Category Is
5. Upload pic → re-gay on persona switch
6. Meme / Story export
7. Burn session
8. Mobile viewport in devtools

## Deploy

```bash
git add . && git commit -m "..." && git push
```

## Product north star

World-class **funny** gay app: timing, theater, virality, privacy. Compete with polished Fable-built demos on delight — not on enterprise agent features.
