<div align="center">
<img width="1200" height="475" alt="GHBanner" src="https://ai.google.dev/static/site-assets/images/share-ais-513315318.png" />
</div>

# Run and deploy your AI Studio app

This contains everything you need to run your app locally.

View your app in AI Studio: https://ai.studio/apps/11912c87-2400-4fb3-b317-807a0923e19d

## Run Locally

**Prerequisites:**  Node.js


1. Install dependencies:
   `npm install`
2. Set the `GEMINI_API_KEY` in [.env.local](.env.local) to your Gemini API key
3. Run the app:
   `npm run dev`
# 🌋 Caldera Overload

**A high-risk, push-your-luck arcade game.** Charge the caldera, bank your yield, and don't let it erupt.

🎮 **Play it here:** [DEPLOYED_URL_HERE]
📦 **Source code:** You're looking at it.

---

## What is this?

Caldera Overload is an endless risk-and-reward arcade game built around a single core tension: the longer you hold to charge thermal pressure, the more you *could* bank — but push too far past the eruption threshold and you lose everything from that hold.

It's designed to be playable in seconds with zero tutorial, but hard to put down once the difficulty curve, streak multipliers, and near-miss tension kick in.

---

## How to Play

1. **Hold** `SPACE`, `Click`, or `Touch` to charge the caldera's core.
2. Watch the pressure percentage rise — the core glows hotter as it climbs.
3. **Release** before it crosses the eruption limit (shown as the red threshold marker) to **bank** your yield.
4. If you cross the limit while still holding, the caldera **erupts** — you lose the unbanked pressure from that hold.
5. Chain successful banks in a row to build a **streak multiplier** for bonus yield.
6. Release right near the eruption limit for a **Perfect Vent** — a high-risk timing bonus.
7. Difficulty escalates the longer you survive: charge rate speeds up and the safe zone shrinks.

**Modes:**
- **Caldera Drill** — endless mode with progressive difficulty scaling
- **Pressure Sprint** — 60-second timed run, auto-archives your score
- **Valve Practice** — no eruption risk, for tuning your timing

**Extra features:**
- 🏆 Achievements (Perfect Vent, streak milestones, lifetime yield goals)
- 🔗 **Challenge a Friend** — generate a shareable link with your score; whoever opens it sees a live "ghost" comparison against your run
- 🔊 Full sound design with mute toggle
- 📱 Fully responsive — playable on mobile, tablet, and desktop

---

## Built During the 24-Hour Hackathon Window

Everything in this repository was built from scratch during the Parsewave Game Jam build window (July 10–11, 2026). No prior project, template, or starter code was reused.

**What was built, in order:**
1. Core charge/release/eruption mechanic and canvas rendering
2. Difficulty scaling (dynamic charge rate + shrinking safe zone), streak system, score multipliers
3. Visual/audio juice — screen shake, particle effects, glow states, Web Audio sound design
4. Game states, localStorage-based high score persistence
5. Full visual theme pass (volcanic/caldera identity, UI redesign)
6. Mobile responsiveness and simplified mobile HUD
7. Achievements system
8. Challenge Link + ghost marker comparison feature
9. Bug fixes, performance pass, and final polish

---

## AI Tools Used

This project was built using **Google AI Studio** (Gemini) as the primary AI-assisted development tool, used iteratively throughout the entire build — not a single generation, but a continuous back-and-forth: prompting features, testing, reporting bugs/issues back with screenshots, and refining based on results.

### AI Build Log (highlights)

- **Core loop first:** Started with a single, tightly-scoped prompt for the charge/bank/erupt mechanic to get something playable immediately, rather than over-specifying up front.
- **Iterative difficulty tuning:** The initial eruption threshold felt too punishing on first playtest; iterated through prompts to land on a dynamic threshold that shrinks from 85% → 60% over time, balancing tension against fairness.
- **Visual identity search:** Generated multiple UI direction variants (a clean minimal "energy stabilizer" theme vs. a more thematic "volcanic caldera" direction) before committing to the volcanic theme for stronger visual identity.
- **Mobile bug fixing:** Initial responsive pass caused panel overlap and off-screen elements on small viewports; caught via direct screenshot review and fixed through a targeted mobile-first layout overhaul, including a simplified mobile HUD with a drawer for secondary stats.
- **Performance pass:** Reviewed for particle system memory leaks, uncleared timers on restart, and frame drops under heavy particle load — fixed through a dedicated cleanup prompt late in the build.
- **Feature ideation:** Explored multiplayer/leaderboard options; chose a lightweight client-side "Challenge Link" (score encoded in a shareable URL) over a backend-dependent leaderboard, prioritizing reliability within the time constraint over scope.

Full prompt history, chat exports, and AI-agent traces are included in `ai-traces.zip` (submitted alongside this repo).

---

## Tech Stack

- **Vanilla HTML5 / CSS3 / JavaScript** — no frameworks
- **Canvas API** for core game rendering and particle effects
- **Web Audio API** for dynamic sound design
- **localStorage** for high scores, achievements, and mute preference persistence
- No external libraries or dependencies

---

## Credits & Disclosures

- [ ] No pre-existing templates, engines, or starter kits were used — built from a blank file.
- [ ] No external code snippets, tutorials, or open-source projects were copied in.
- [ ] No pre-generated or external art/audio assets — all visuals are programmatically rendered (canvas shapes/gradients); all audio is synthesized via Web Audio, not sourced externally.
- [ ] All development was done using Google AI Studio as described above.

*(Edit the above list if any of it doesn't apply — e.g., if you did use a font from Google Fonts, a specific icon set, or any snippet, disclose it here explicitly.)*

---

## Repository Structure
