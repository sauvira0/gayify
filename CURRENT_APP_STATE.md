# gayify / ChakkaAI - Current App State (Compact Context)

**Date of this snapshot:** Desi Urdu/Hindi subculture overhaul + Punjabi/Lahori juggat amp (kiddan, puttar, patakha, balle balle, shava shava, more hijra khusra language, stronger Pathan yaar/munda energy, filmi lines, mehndi/henna canvas patterns). 6 desi queer personas. JUGGAT (theater masks), The Adda, desi color vibes (haldi, mehndi, saffron, kajal). Still fully ephemeral single-file.

**Live URL:** https://sauvira0.github.io/gayify/ (GitHub Pages, auto-deploys on push to main)

**Repo:** https://github.com/sauvira0/gayify (single-file static site)

## Core Architecture (Ironclad Rules - DO NOT CHANGE)
- **Pure client-side only**: One file `index.html` (inline Tailwind 3 via CDN + vanilla JS + Font Awesome). No backend, no npm, no build step.
- **Ephemeral by design** (critical for sharing):
  - All state in JS variables only (messages[], gayMoments[], slayScore, currentStreak, badges Set, currentPersona, lastUploadedImage, sceneCount, etc.).
  - **NO localStorage, sessionStorage, cookies, IndexedDB, or any persistence**.
  - Every tab/window/person gets a completely isolated chat.
  - Close tab/window or refresh = everything gone forever. "When they close it, all info is lost."
  - Burn button (`burnSession()`) explicitly wipes everything with animation + resets to welcome.
- **Privacy first**: Images processed entirely in browser (FileReader → data: URLs → Canvas). Never leaves the tab. Share link is safe for gay friend WhatsApp groups.
- **Mobile friendly + world-class visuals**: Glassmorphism, gold (#d4af37) accents, bokeh, shimmer, expensive photo treatment. Responsive with Tailwind + custom CSS (min-h-dvh, safe areas, touch targets ≥36-44px on mobile).
- **Direct flows**: Text send = gayify. **Pic upload (tap big dashed box or drag to #messages or button) = instantly appends user pic + bot gay response with captions + gayified canvas image**. No "attach then send" step.

## Key Features (Addictive + Viral Loop)
- **gayify(text)**: Core transformer. Special cases, word replacements, flamboyant prefixes/suffixes ("YASSS queen", "periodt", "the girls are gagged"), intensifiers, emojis, occasional caps. Returns over-the-top sassy gay version.
- **Personas** (4 micro buttons in chat header): femme 💖, camp 🌟, mystery 🖤, daddy 🖤. Mutates both text (personaGayify) and image filters/overlays/tags in gayifyImage().
- **Image pipeline** (instant on upload):
  - analyzeImageVibe(): Canvas sampling for dominant colorVibe, pose (aspect ratio), brightness.
  - generateCaptions(): 5+ stealable gay captions based on vibe + persona.
  - gayifyImage(): Heavy canvas work — persona-driven filters (saturate/hue/sepia/contrast), 30+ sparkles, bokeh orbs, gold vignette, gold foil text tag ("SEDUCED", "YOURS"), edge treatment. Returns data URL.
  - Side-by-side original + gayified in chat. Captions with copy buttons + "Regenerate gay version" + rate buttons (+5 slay for "This ate").
- **Slay system**: Points on every message (more for bot). Levels (Baby Gay → Twink in Training → Fierce Queen → Mother of the House → Legendary Cuntress → Gay Icon). Streak, progress bar (in compact pill). Level-up toasts + confetti + chimes.
- **Addictive collection**:
  - Trophy Case (badges unlocked on milestones: first_blood, picasso, mother, icon, hot_streak, collector).
  - My Gay Diary: Grid of past moments (text + thumbs of images). Replay button (re-processes with current persona for fresh gayified).
- **Virality hooks** (fake but convincing, all client-side):
  - Live "X queens serving rn" counter (bumps on actions).
  - createMemeCard(): Luxe 800px canvas with gold borders, "GAYIFY EXCLUSIVE", latest moment + text, "PRIVATE • EPHEMERAL • TAG YOUR BESTIE".
  - exportStoryRecap(): Tall 9:16 story image for IG/WhatsApp stories (multiple moments + score + privacy warnings).
  - shareWithFriends(): Copies pre-written viral WhatsApp text.
  - Tease Me, Surprise Me, Vibe Roulette (random persona + re-gay image), Spill the Tea (prompt + dramatic response).
- **Voice**: toggleVoice() + speakText() using Web Speech API (higher pitch/rate for camp sass). Mic icon.
- **Other UX**:
  - Burn (with confirm in recent version), New Chat (clear), Quick prompts.
  - Drag & drop on messages area.
  - Typing indicators, message pop animations, confetti bursts, play sounds (AudioContext).
  - Compact header on mobile: tiny SLAY pill (score + level emoji + streak), icon-only actions.
  - Big always-visible "UPLOAD A PIC" dashed CTA in input area with clear instructions.
  - Empty state with upload spotlight.

## Recent History / What Was Done Before Revert
- Heavy focus on **mobile friendliness** ("revise the page to be mobile friendly, keep going hardest", after user screenshot of clutter):
  - Header condensed (logo + tiny live count + compact SLAY pill + small icons).
  - Bottom action row: icon-only with better padding/taps (6 buttons: heart, book, magic, sync, trophy, comment).
  - Prominent upload box + improved welcome/empty state.
  - Extra @media CSS for bubbles, inputs, persona pills, upload on xs.
  - Persona micro-pills added in chat header (mobile-friendly).
  - Fixes for missing DOM elements (guards in updateSlayScore), persona wiring (vibeRoulette safe), streak mini in pill.
- Added/enhanced: tall story export, quick re-gay on persona switch, better replay with current persona, burn confirm, refined toasts/offers, CSS polish.
- Brief pivot attempt to "juggatify" (Lahori Punjabi juggat version) was fully reverted per user "nevermind, revert to old".
- Current code is clean revert to the polished gayify state (based on 13acb7c mobile work + earlier features).
- All privacy/ephemeral guarantees preserved throughout.

## How to Resume / Next Session Tips
- Open `index.html` directly in browser for testing (or `python -m http.server`).
- To edit: Use search_replace on index.html (preferred for precision on long file). Read sections with read_file(offset, limit).
- Key files to touch: Only index.html + README.md (keep self-contained).
- Test flows: Text gayify, pic upload (various sizes/HEIC if possible in emulator), persona switch + re-gay, diary replay, meme/story export, burn, mobile emulation (devtools), voice.
- Deploy: `git add . && git commit -m "..." && git push` (Pages auto).
- When making changes: Preserve "per-tab only", "close tab = gone", direct upload, no storage. Add comments for future.
- User style: "go easy, keep going, ... keep going hardest", "world class visually appealing", "sexy and addictive", "mobile friendly", "viral in gay community", "free-hand".
- Common requests: More mobile declutter, richer visuals, new addictive hooks (without breaking privacy), better image gayification, virality for WhatsApp.
- If user mentions "compact" or "save context" again: Update this file + commit.

## Quick Commands (for future)
- Test locally: open index.html or serve it.
- Check state: `git status`, `git log --oneline -5`.
- Revert if needed: git checkout <commit> -- index.html README.md.

**App is ready for resumption.** All previous requirements (privacy, single-file, mobile, visuals, addictiveness) are intact.

**Latest evolution:** OpenRouter LLM integration (key pre-baked).
- The app now uses a real LLM (default model: "openrouter/free") for text responses and image reactions when enabled.
- Robustness layer: llmEnabled toggle (🤖 icon), per-message 🤖 LLM badges, online/offline listeners (auto-disable), callWithRetry + 10s Abort timeout, rate-limit/401 detection + toasts + fallback.
- LLM status pill in header for quick visibility.
- All paths (text, images, replays) respect the toggle and fallback gracefully.
- Key still pre-baked per user request (with security warnings in code).
- This makes answers highly non-deterministic, creative, and varied (high temperature).
- Robot icon (🤖) in header: click to override or clear the pre-set key (falls back to classic rule-based juggat).
- All previous desi subculture work (Punjabi juggat, kothi/hijra/Pathan energy, mehndi canvas patterns, etc.) is preserved and used to condition the LLM via a strong system prompt.
- ⚠️ The provided OpenRouter key is now hardcoded and public in the source / deployed page. Rotate it on OpenRouter if you don't want it exposed/used by others.
- Core ephemeral rule still holds for chat state (per-tab only), but LLM calls go to OpenRouter.

When the user says "go wild" or "more queer" again, lean harder into specific cultural references, longer chaotic rants, and even more interactive "the groupchat is watching" energy.

**Desi direction notes:** User explicitly asked for "Urdu/Hindi desi subculture". Previous juggat attempt was reverted, but this time fully embraced. Keep Roman Urdu accessible + mix with previous flamboyance. ChakkaAI name is perfect for this. Focus on adda/mehfil/gupshup/juggat/rishta/mummy/log kya kahenge energy + strong Punjabi/Lahori (kiddan, puttar, balle, patakha) and hijra/Pathan flavor. Added mehndi dots + henna curves on gayified images. Image tags and filters should feel like a desi mehfil with gold. Privacy message can lean "log nahi jaanenge".

---
Generated for session resumption. Do not modify core privacy model.