# Endless Play Vault

A standalone, installable web game app (PWA). 26 distinct games holding 461 built-in puzzles, tracks and boards,
running on 23 hand-written game engines. No accounts, no payments, no trackers.

- `app/` is the finished static site. Open `app/index.html` through any static web server.
- `src/` is the source (vanilla ES modules). `./build.sh` bundles it with esbuild into `app/js`
  and regenerates the offline service worker `app/sw.js`.
- Best scores and stars are kept in this browser only (localStorage).
- Every game is free. There are no card fields and nothing is charged. An optional Tip Jar card at the bottom of the home page opens in a new tab and unlocks nothing.
- Reel House, Twenty One and Coin Pit use pretend points only. Nothing can be bought or cashed out.

Run locally: `python3 -m http.server 8765 --directory app` then open http://localhost:8765/

Test hooks: `?autoplay=1&autostart=1&ts=4` plays a round by itself; `?nosw=1` skips the service worker.

## What changed in v1.3

- One card per game: home and browse now show 26 genuinely different games in six categories (Word & Spelling 6, Puzzles 4, Action & Arcade 7, Racing & Reflex 4, Aim & Strategy 3, Cards & Luck 2). The 461 seeded puzzles, tracks, boards and themes live inside each game: pick one on the game page, or tap Next in the play bar or on the results screen.
- 149 new built-in puzzles and boards on 8 new engines, all free.
- Crossword: 32 real intersecting puzzles (mini 7x7, classic 9x9, grand 11x11) with family-friendly clues. Tap a cell twice to switch Across and Down. Keyboard or on-screen letters, Check letter, Check word, Hint, time and score saved.
- Sudoku: 24 puzzles in Easy, Medium and Hard, each with exactly one solution. Number pad, Notes, Erase, Hint, Check, conflict highlighting, row, column and box highlighting, best time saved.
- Word Search: 16 themed boards with drag or tap-tap selection and Hint.
- Spelling games: Honeycomb Speller (24 hives with pangrams and ranks), Word Scramble (12 timed sets) and Clue Speller (12 sets, with a spoken word when the browser supports it and a text clue otherwise).
- Glass Ring Marbles: 12 rings with swirled glass marbles, shadows, clinks and six layouts.
- Squeak Bounce Match: 12 tubes of glossy high-bounce rubber balls with squash and stretch, squeaks and boings. Pop 3 or more touching balls of one color over 3 stages.
- Five more Letterlock word puzzles.
- Tip Jar is now quiet: one card at the bottom of the home page only, with a single Leave a tip button. It is gone from the header, results and My scores.
- Service worker cache is now epv-v1-3-<hash>.
