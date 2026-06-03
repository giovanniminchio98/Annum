# Annum — Chronicle of Ages

> A timeline webapp from the Big Bang to today, narrating history as a tale of heroes and villains. Vertical right-side scroller, era-based color themes, ~172 events.

**Deployed via:** GitHub Pages (`index.html` at repo root)  
**Branch:** `claude/timeline-webapp-bigben-2026-bq3CD`  
**Live URL:** https://giovanniminchio98.github.io/Annum/ *(once GitHub Pages is enabled)*

---

## ⚡ Resume Protocol (READ THIS FIRST)

This README is updated on every significant commit. If a session ends mid-work:

1. Run `git log --oneline -10` to see what was last committed
2. Read the **Current Status** table below — it's kept up to date
3. Say: *"Continue the Annum timeline webapp — read the README"*
4. Claude will pick up exactly from the last checkpoint

**Commit policy:** README + code committed after every meaningful change (every ~10 events added, every feature completed, every layout change). Nothing is lost between sessions.

---

## Current Status

| Phase | Status | Notes |
|---|---|---|
| Project setup | ✅ Done | Branch created, repo initialized |
| Initial draft (1859–2026, horizontal scroll) | ✅ Done | Commit `08cd230` — 168 cards, all features |
| **Full rewrite: Big Bang → Today, vertical scroller** | ✅ Done | Commit `ceb365f` — 89 events, 25 eras |
| Expand events: fill gaps to ~172 events | ⏳ Next | Add missing ancient/medieval/modern events |
| Enable GitHub Pages | ⏳ Pending | Repo owner enables in GitHub Settings |
| README continuity docs | ✅ Done | This file, updated regularly |

**Last known good state:** `ceb365f` — full working app, Big Bang → June 2026, vertical scroller.

### What's in the current build (`ceb365f`)
- **89 events** from Big Bang (13.8B BCE) to Today (June 2026)  
- **25 era color themes** with smooth CSS transitions  
- **Layout:** center detail panel (era gradient bg, full narrative) + 220px right vertical scroller  
- **Scroll:** fixed cursor line at 33% from top, nearest item = active, wheel anywhere scrolls the strip  
- **Features:** auto-play, time capsule (localStorage), fate meter, Web Audio ambient sound, year/event selector modal with search + era chips, time gap display, keyboard ↑↓, touch swipe

### What's missing / next steps
1. **More events** — currently 89, target ~172. Gaps mainly in:
   - Ancient world (500 BCE – 476 CE): missing Parthenon, Socrates, Alexander, Caesar's death, Pompeii
   - Medieval (476–1400): missing Charlemagne, Crusades, Magna Carta, Black Death
   - Renaissance → 1800: missing Luther, Galileo, Newton, French Revolution
   - Modern 1859–1999: missing ~40 key events (Titanic, WWI detail, Moon landing, etc.)
2. **GitHub Pages setup** — needs to be enabled by the repo owner
3. **Polish pass** — test on mobile, check era transitions on fast scroll

---

## What This App Is

A beautiful, single-file (`index.html`) web app that:

- **Scrolls horizontally** through all of history — from the Big Bang (13.8 billion BCE) to today (June 2026)
- **Narrates each event** as a hero or villain story — like a tale where humanity is the protagonist
- **Changes its visual style** dynamically based on the historical era (cosmic purples → ancient gold → medieval stone → neon 80s → dark modern)
- **Has ~250 event cards** total, spanning cosmic prehistory through modern day

---

## Full Feature List

### Core
- [x] Horizontal scroll timeline with CSS `scroll-snap-type: x mandatory`
- [x] Intelligent scroll: converts vertical mouse wheel to horizontal, touch swipe support
- [x] Era-based dynamic color themes (CSS custom properties updated via JS)
- [x] Hero / Villain / Mixed badge on each card
- [x] Narrative text for every event (2–4 sentences, storytelling style)

### Navigation
- [x] **Year/Event selector** — full-screen grid overlay, searchable, color-coded by era
- [x] **Era jump buttons** — quick jump to Cosmic, Ancient, Classical, Medieval, Renaissance, Modern, Today
- [x] **Keyboard navigation** — ← → arrows, Escape closes modals
- [x] **Progress bar + mini-map** at bottom, clickable to jump
- [x] **Auto-play mode** — advances automatically, speed control (Slow/Normal/Fast)

### Extra Features
- [x] **Fate Meter** — running tally of hero vs villain events (shown in header)
- [x] **Time gap labels** between cards ("↔ 65 million years")
- [x] **BCE/CE epoch divider** — glowing marker when crossing year 0
- [x] **Time Capsule** — leave a note on any year card, stored in localStorage
- [x] **Web Audio ambient sound** — era-appropriate tones via Web Audio API (no external files)
- [x] **Particle effects** — subtle canvas particles that match the era style

---

## Timeline Structure (~250 cards)

| Era | Period | Cards | Color Theme |
|---|---|---|---|
| Cosmic | 13.8B BCE → 4B BCE | ~15 | Deep space purple `#0a0a1e` |
| Earth & Life | 4B BCE → 300K BCE | ~12 | Volcanic orange → jungle green |
| Human Dawn | 300K BCE → 10K BCE | ~10 | Warm cave-fire brown |
| Ancient World | 10K BCE → 500 BCE | ~35 | Desert gold `#1a1400` |
| Classical Antiquity | 500 BCE → 476 CE | ~25 | Marble blue `#0a0a14` |
| Early Medieval | 476 → 1000 CE | ~20 | Dark stone `#0e0a0a` |
| High Medieval | 1000 → 1400 CE | ~20 | Blood red stone |
| Renaissance | 1400 → 1700 CE | ~25 | Warm gold `#1a1000` |
| Age of Sail/Reason | 1700 → 1858 CE | ~15 | Ocean blue |
| Victorian | 1859 → 1900 | ~20 | Sepia `#1a0a00` |
| Edwardian / WWI | 1901 → 1919 | ~10 | Muted steel |
| Roaring 20s → WWII | 1920 → 1945 | ~15 | Gold → dark olive |
| Cold War | 1946 → 1969 | ~12 | Steel blue |
| Space Age / 70s | 1970 → 1979 | ~8 | Earth orange |
| Neon 80s | 1980 → 1989 | ~8 | Hot pink neon |
| Digital Revolution | 1990 → 1999 | ~8 | Teal `#001e1e` |
| New Millennium | 2000 → 2009 | ~12 | Dark blue |
| Social Age | 2010 → 2019 | ~12 | Flat blue |
| Crisis Era | 2020 → Today | ~10 | Dark mode `#0d1117` |

---

## Key Events Included

### Cosmic & Prehistoric
- 13.8B BCE: Big Bang
- 4.5B BCE: Earth forms
- 3.8B BCE: First life
- 600M BCE: Cambrian explosion
- 66M BCE: Asteroid wipes out dinosaurs
- 300K BCE: Homo sapiens evolves
- 70K BCE: Toba catastrophe (near-extinction)
- 40K BCE: Cave paintings — art is born
- 12K BCE: Agriculture begins (Fertile Crescent)
- 10K BCE: Göbekli Tepe — world's first temple

### Ancient World
- 3500 BCE: Sumerian civilization, first writing
- 3100 BCE: Egypt unified, hieroglyphics
- 2560 BCE: Great Pyramid built
- 1792 BCE: Code of Hammurabi
- 776 BCE: First Olympic Games
- 753 BCE: Rome founded
- 563 BCE: Birth of the Buddha
- 500 BCE: Greek Golden Age (Socrates, democracy)

### Classical Antiquity
- 336 BCE: Alexander the Great
- 44 BCE: Julius Caesar assassinated
- ~4 BCE/1 CE: Birth of Jesus Christ
- 79 CE: Vesuvius buries Pompeii
- 313 CE: Christianity legalized (Edict of Milan)
- 476 CE: Fall of Western Roman Empire

### Medieval
- 570 CE: Birth of Muhammad, Islam begins
- 800 CE: Charlemagne crowned
- 1066 CE: Battle of Hastings
- 1215 CE: Magna Carta
- 1347 CE: Black Death

### Renaissance → 1858
- 1440: Gutenberg's printing press
- 1492: Columbus reaches Americas
- 1543: Copernicus (Earth orbits the Sun)
- 1687: Newton's Principia
- 1776: American Declaration of Independence
- 1789: French Revolution
- 1859: Darwin's On the Origin of Species + Big Ben

### Modern (key events, not every year)
- 1865: Lincoln assassinated, slavery ends
- 1903: Wright Brothers fly
- 1912: Titanic sinks
- 1914–1918: World War I
- 1929: Wall Street Crash
- 1939–1945: World War II, Holocaust, atomic bombs
- 1953: DNA discovered
- 1969: Moon landing
- 1989: Berlin Wall falls
- 1991: USSR dissolves, WWW goes public
- 2001: September 11
- 2007: iPhone
- 2020: COVID-19 pandemic
- 2022: Russia invades Ukraine
- 2023: ChatGPT — AI revolution
- 2026: Today

---

## File Structure

```
Annum/
├── index.html          ← The entire app (self-contained HTML/CSS/JS)
└── README.md           ← This file — project status and resume guide
```

Everything is in one `index.html`. No build step, no dependencies except Google Fonts CDN.

---

## How to Resume This Project

If starting a new Claude Code session, say:

> "Continue building the Annum timeline webapp. Read the README for context."

Then Claude should:
1. Read this README for full context
2. Check `git log --oneline` to see what's been committed
3. Open `index.html` to see current state
4. Continue from **Current Status** table above

### What's left to do (in order):
1. **Rewrite `index.html`** with the full Big Bang → Today scope (~250 cards)
   - The agent wrote an initial draft covering 1859–2026 (every year)
   - This needs to be replaced/extended with the full cosmic scope
   - All events listed in "Key Events Included" above must be in the data array
2. **Test the scroll** — make sure wheel, touch, and keyboard all work
3. **Enable GitHub Pages** — Settings → Pages → Deploy from branch `main` (or this branch, whichever merges first)
4. **Polish pass** — check era color transitions, card layout on mobile, auto-play

---

## Design Decisions Made

- **Single file** — everything in `index.html`, no build tools needed
- **Google Fonts** — Playfair Display (serif, for card titles), Inter (body), Cinzel (header UI)
- **CSS scroll-snap** for magnetic card snapping
- **CSS custom properties** on `:root` updated by JS for era color transitions
- **No images hosted** — uses Wikimedia Commons URLs with CSS fallback gradients if images fail
- **Web Audio API** for ambient sounds — no external audio files needed
- **LocalStorage** for Time Capsule notes (user can leave notes on any year)

---

*Last updated: 2026-06-03 | Status: In active development*
