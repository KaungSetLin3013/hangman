# 🎯 The Reckoning — Hangman

A gothic-themed number-guessing game in a single self-contained HTML file. Despite the name, it's not word-guessing hangman — it's a **1–100 number-guessing duel** where every wrong guess brings your own gallows one step closer to finished, Mastermind-style "too high / too low" hints included.

No build step, no dependencies — open the file and play.

## ✨ Features

- **Two game modes**
  - **Solo — vs Fate**: Fate picks a secret number from 1–100; guess it before the gallows is complete.
  - **Two Players — Duel**: each player secretly sets a number (1–100) for the other to guess, entered behind a "look away" cover screen so the opponent can't peek. Players then take turns guessing each other's number.
- **Hangman-as-lifebar** — instead of guessing letters, each wrong number guess draws one more piece of your own gallows. Six wrong guesses and you're condemned; your opponent (or "Fate") wins.
- **Live range narrowing** — the UI tracks the tightest possible range based on your "too high"/"too low" feedback so far, and lists every wrong guess as a chip for reference.
- **Dual scaffolds in duel mode** — both players' gallows are shown side by side, each animating independently as guesses land.
- **Score tracking across rounds**, with a "Next Round" flow that returns straight to secret-setting.
- **Custom numpad input** (with a backspace key) instead of a native number field, for quick, large touch targets on mobile.
- **Gothic visual theme** — candle-flicker accents, Cinzel/IM Fell English typography, parchment-and-ink color palette, animated gallows and hanging figure, consistent with the rest of *The Reckoning* series.

## 🎮 How to play

**Solo (vs Fate):**
1. Tap a number on the numpad and hit **Guess**.
2. "Too low" / "too high" narrows the range — use it to guess smarter.
3. Find the number within 6 wrong guesses, or the gallows claims you.

**Duel (Two Players):**
1. Player 1 sets their secret number behind the cover screen, then hands the device to Player 2 to do the same.
2. Once both secrets are set, hit **Begin the Duel**.
3. Players alternate guessing the *other* player's number. Each wrong guess advances your own gallows.
4. First to guess correctly wins the round — or if a player's gallows completes (6 wrong guesses), their opponent wins by default.

## 🛠 Tech stack

- Vanilla HTML/CSS/JS — single file, no frameworks, no build tools
- Inline SVG for the animated gallows, flame flicker, and hanged/winning figure states
- Google Fonts: [Cinzel](https://fonts.google.com/specimen/Cinzel) and [IM Fell English](https://fonts.google.com/specimen/IM+Fell+English), loaded via CDN (the game still works offline with fallback serif fonts if the fonts can't load)
- All game logic runs client-side — no backend, no external services

## 🚀 Running it

No setup required:

- **Locally**: open `index.html` in any modern browser.
- **Hosted**: drop it on GitHub Pages, Netlify, Vercel, or any static host — it's a single file with no server-side dependencies.

## ⚙️ Customization ideas

- Change the wrong-guess limit (currently `6`, matching the 6 gallows-drawing stages) to make rounds shorter or longer — you'd also need to add/remove corresponding SVG stages.
- Adjust the number range (`1–100`) in the input-validation checks if you want a smaller or larger guessing pool.
- Swap the `--gold` / `--p1` / `--p2` CSS variables to retheme the color palette away from the gothic look.

