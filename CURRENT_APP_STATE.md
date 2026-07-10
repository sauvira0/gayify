# gayify / ChakkaAI — Current App State

**Snapshot:** Giant feature pack on mobile-first web — Category of the Day, quick replies, reactions, slash commands, undo, transcript export, cinema mode, shake roulette, persona long-press, Studio force, net pill, ambient coven, scroll FAB, privacy/help sheets. PWA + A2HS + slow-net Studio. Ephemeral chat unchanged.

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

### Comedy engine (Studio)
- **STUDIO_BITS**: ~95 authored multi-beat bits (main + optional side + follow), topic-tagged
- **Anti-repeat (aggressive)**: bit IDs, full line FP, openers (first 5 words), hooks, coven FP, trigram similarity vs last 24 bot lines
- Soft recycle frees oldest ~40% of bits only when needed; then **spice remix**; then **procedural gay rants** (RANT_OPEN/MID/END) so silence never copies
- Topic overuse penalty pushes variety; top-tier shuffle so same topic ≠ same bit
- `ensureFunnyGay()` wraps beige lines; Live quality gate requires queer/comedy signal
- **Multi-beat delivery:** main → coven → follow/callback (all anti-repeat checked)
- **sessionMemory** for callbacks + LLM context (ephemeral)
- ~139 authored mains + expanded coven/follow banks

### Honest AI / local split
- **STUDIO** (gold badge) = authored comedy — default quality path
- **LIVE** (mint badge) = OpenRouter free, **quality-gated** (length, anti-repeat, no AI-disclose, not near-dupe)
- If Live fails the gate → Studio (not a shame path — the written show)
- Toggle shows LIVE vs STUDIO; header says "Studio + Live" or "Studio only"

### Games
- **Category Is (killer game):** 3 rounds, 10 categories, panel reads, scoring rubric, running scoreboard /30, titles (House Legend → Chip), badges
- Roast Me (force Studio roast topics), Hot Seat, Spill Tea, Go Off, Vibe Roulette
- Demo = cinematic multi-beat showcase

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
