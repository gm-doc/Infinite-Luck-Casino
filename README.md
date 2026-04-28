# 🎰 Infinite Luck Casino

> A Kitboga Code Jam 2026 submission — three unskippable casino ad games that are absolutely, definitely, 100% not rigged.

**Live demo:** https://pirate-bytes.github.io/Infinite-Luck-Casino-main/

---

## What is this?

Infinite Luck Casino is a suite of three fully interactive casino ad games built for the [Kitboga Code Jam 2026](https://kitboga.com/codejam26). All three games are merged into a single `submission/submission.html` file, routed by a URL parameter, and designed to run as a 960×540px iframe inside the code jam's ad player shell.

The core joke: you are far too lucky to ever run out of tickets. The game always makes sure of that.

---

## Project structure

```
index.html                ← tabbed launcher shell (demo / gitio page)
submission/
  submission.html         ← the merged submission (all three games)
  assets/                 ← all images and the ad video
    CrowPro.png
    SeraphSecure.png
    WindowsRG.png
    WWWW.png
    AWPDL.png
    Doot.png
    DootCry.png
    DootLove.png
    ILC-AD.mp4
```

---

## Games

Opened via `submission/submission.html?game=<wheel|slot|scratch|random>`.

### 🎡 Prize Wheel (`?game=wheel`)
Spin a canvas prize wheel to reveal your prize. 10 weighted slices per tier, cubic ease-out animation with synced tick and clunk sounds.

### 🎰 Slot Machine (`?game=slot`)
Three reels with weighted symbol strips. Near-misses are engineered. Jackpots are achievable. Running out of tickets is not.

### 🃏 Scratch Card (`?game=scratch`)
Scratch a 3×3 foil grid with mouse or finger (Web Canvas + `destination-out` compositing). Match 3 in a row, column, or diagonal to win.

### 🎲 Random (`?game=random`)
Picks one of the three games at random. Also plays the built-in ILC-AD.mp4 promo video before revealing the game — the video ad only appears in this mode.

---

## How it works

1. The intro popup explains the rules. Click **Let's Play!** to start.
2. Each play costs 1 ticket. Win prizes to earn more tickets (and shrink the skip timer).
3. Play enough rounds to **unlock the Golden tier**, then the **Diamond tier**.
4. A skip button appears after a cooldown — but only if you have zero tickets left.
5. The **Collect Prizes** button will enthusiastically explain why you shouldn't leave yet.

---

## Features

- **Single-file submission** — all three games in one HTML file, routed by `?game=` URL param
- **3-tier system** — Base → Golden (amber) → Diamond (cyan), each with a full UI reskin, themed prizes, and escalating rewards
- **Rigged probability** — wins weighted per tier; ticket prizes guaranteed when running low
- **Synthesised audio** — every sound generated at runtime via Web Audio API; no audio files shipped; independent volume slider
- **Live winners ticker** — fake scrolling winner feed starts after the intro popup is closed
- **Idle detection** — escalating nag popups if the player sits idle, with skip timer penalties
- **Dog popup** — win the dog prize and you have 2 minutes to kiss him before he leaves
- **Skip cooldown system** — 5-minute timer; prizes reduce it; trying to skip early resets it
- **Confetti bursts** — on every win and tier upgrade
- **Vegas aesthetics** — twinkling stars, colour-cycling border bulbs, neon pulsing title
- **Tier-aware tab bar** — `index.html` tab border colour updates to match the active tier via `postMessage`

---

## Running locally

```powershell
cd "c:\path\to\Infinite-Luck-Casino-main"
python -m http.server 8080
# open http://localhost:8080
```

Or use **Run and Debug → Open in Chrome** in VS Code (starts the server automatically if not already running).

---

## Submission notes

For the code jam judge, the submission entry point is:

```
submission/submission.html?game=random
```

This is the intended experience: the promo video plays, then a randomly selected game begins.
