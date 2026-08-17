# 2048

A clean, responsive browser implementation of the classic **2048** sliding-tile
game. Join matching tiles to double them and work your way up to the 2048 tile —
and beyond.

Built as a single self-contained `index.html` (HTML + CSS + vanilla JS). No build
step, no dependencies, no backend — just open it in a browser.

## Play

Open `index.html` in any modern browser, or serve the folder statically:

```bash
# any static server works, e.g.
python3 -m http.server 8000
# then visit http://localhost:8000
```

## How to play

- Tiles slide as far as they can in the chosen direction.
- Two tiles with the same number merge into one worth double.
- Each move spawns a new tile (a 2, or occasionally a 4).
- Reach **2048** to win — then keep going for a higher score. The game ends when
  the board is full and no moves remain.

### Controls

| Input | Action |
| --- | --- |
| Arrow keys | Move tiles |
| `W` `A` `S` `D` | Move tiles |
| `H` `J` `K` `L` | Move tiles (vim style) |
| Swipe | Move tiles (touch devices) |
| **New Game** button | Restart at any time |

## Features

- Smooth slide, spawn, and merge animations with floating score popups.
- **Score** and **Best** tracking; the best score persists across sessions via
  `localStorage` (with an in-memory fallback if storage is unavailable).
- Win / game-over overlays with "Keep going" and "Try again".
- Fully responsive — plays well from small phones to desktop.
- Accessible, semantic markup and respects the classic 2048 color palette.

## Project structure

```
.
├── index.html   # The entire game: markup, styles, and logic
└── README.md
```

## Tech

- Vanilla JavaScript — no frameworks.
- CSS grid for the board; absolutely-positioned tiles animated with
  `transform` for smooth movement.
- [Inter](https://fonts.google.com/specimen/Inter) web font via Google Fonts.

## Credits

Inspired by [2048](https://play2048.co/) by Gabriele Cirulli.
