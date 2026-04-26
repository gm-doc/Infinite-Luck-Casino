# 🎰 Infinite Luck Casino

A Kitboga Code Jam 2026 submission — three unskippable casino ad games that are absolutely, definitely, 100% not rigged.

**Live demo:** https://gm-doc.github.io/Infinite-Luck-Casino/

---

## What is this?

Infinite Luck Casino is a suite of three fully interactive casino ad overlays built for the [Kitboga Code Jam 2026](https://kitboga.com/codejam26). Each runs as a 960×540px iframe overlay on top of a video, blocks the skip button, and keeps the player playing "just one more time" through increasingly elaborate prize tiers.

The core joke: you are far too lucky to ever run out of tickets. The game always makes sure of that.

---

## Games

### 🎡 Prize Wheel (`submission/`)
Spin a canvas prize wheel to reveal your prize. 10 weighted slices per tier, cubic ease-out animation with synced tick sounds. The wheel always lands somewhere interesting.

### 🎰 Slot Machine (`submission-slot-machine/`)
Pull the lever and watch three reels spin. Near-misses are engineered. Jackpots are achievable. Running out of tickets is not.

### 🃏 Scratch Card (`submission-scratch/`)
Scratch a 3×3 foil grid with your mouse or finger to reveal prizes. Match 3 in a row, column, or diagonal to win. Discard and deal a new card — for just one ticket.

---

## How to play

1. The ad starts automatically when the page loads.
2. Each game starts with a small number of tickets. Each play costs 1 ticket.
3. Win prizes — credits, Google Play cards, iPhones, vehicles, and more.
4. Win enough rounds and you'll **unlock the Golden tier**, then the **Diamond tier** (featuring Bitcoin).
5. A skip button appears after 60 seconds — but only works if you have zero tickets left.
6. The "Collect Prizes" button will enthusiastically explain why you shouldn't leave yet.

---

## Shared features (all three games)

- **3-tier system** — Base (purple/red) → Golden (amber) → Diamond (cyan/blue), each with a full UI reskin, themed prizes, and escalating rewards
- **Rigged probability** — ticket prizes are weighted higher when you're running low; guaranteed at 1 ticket
- **Synthesised audio** — every sound generated at runtime via Web Audio API — no audio files; independent volume slider per game
- **Dramatic tier upgrade popups** — full-screen animation with confetti and a fanfare
- **Vegas aesthetics** — twinkling stars, colour-cycling border bulbs, neon title pulse, confetti bursts
- **Prizes Won list** — stacking Nx counter per prize in the left panel
- **Skip cooldown** — 60-second timer; attempting to skip early plays a sad trombone and resets the clock
- **`index.html` shell** — tabbed launcher with a reactive neon banner that changes colour with each tier upgrade
