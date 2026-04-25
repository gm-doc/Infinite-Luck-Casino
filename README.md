# 🎰 Infinite Luck Casino

> A Kitboga Code Jam 2026 submission — an unskippable casino ad overlay that is absolutely, definitely, 100% not rigged.

**Live demo:** https://pirate-bytes.github.io/Infinite-Luck-Casino-main/

---

## What is this?

Infinite Luck Casino is a fully interactive prize wheel ad overlay built for the [Kitboga Code Jam 2026](https://kitboga.com/codejam26). It runs as a 960×540px iframe overlay on top of a video, blocks the skip button, and keeps the player spinning "just one more time" through increasingly elaborate prize tiers.

The core joke: you are far too lucky to ever run out of tickets. The wheel always makes sure of that.

---

## How to play

1. The ad starts automatically when the page loads.
2. You have **5 tickets** to begin. Each spin costs 1 ticket.
3. Spin the wheel and win prizes — credits, Google Play cards, iPhones, vehicles, and more.
4. Win enough spins and you'll **unlock the Golden Wheel**, then the **Diamond Wheel** (featuring Bitcoin).
5. A skip button appears after 60 seconds — but only works if you have zero tickets left.
6. The "Collect Prizes" button will enthusiastically explain why you shouldn't leave yet.

---

## Features

- **3-tier wheel system** — Base (purple/red) → Golden (amber) → Diamond (cyan/blue), each with a full UI reskin, themed prizes, and escalating rewards
- **Rigged probability** — ticket prizes are weighted higher when you're running low; guaranteed when you hit 1 ticket
- **Canvas prize wheel** — drawn with the Web Audio API (no external assets), 10 slices per tier, cubic ease-out spin animation with synced tick sounds
- **Synthesised audio** — every sound (spin, ticks, stop clunk, ka-ching, jackpot fanfare, denied wah, tier upgrade) is generated at runtime via Web Audio API — no audio files
- **Dramatic tier upgrade popups** — full-screen animation with confetti and a fanfare
- **Vegas aesthetics** — twinkling stars, colour-cycling border bulbs, neon title pulse, confetti bursts
- **Prizes Won list** — stacking Nx counter per prize in the left panel
- **Skip cooldown** — 60-second timer; attempting to skip early resets the clock and plays a sad trombone
