# Sudoku Workbench

A two-page Sudoku trainer, both pages self-contained with no build step and no
dependencies.

- **`index.html`** — the board. Solve it yourself with mistake checking, and ask
  for the logic only when you want it: twenty techniques, each with spotting
  tips and worked examples on part-solved grids.
- **`stuck.html`** — what to do when you're stuck. A triage, then a fixed ladder
  of passes from cheapest to most expensive, with looping animated demos built
  from real board positions.

## Hosting

Put both files in the repository root. For GitHub Pages:
**Settings → Pages → Source: Deploy from a branch → main → /(root)**.
The two pages link to each other by relative filename, so they must sit in the
same folder.

## Input

- Select a cell and press **1**–**9** to place a digit.
- **Ctrl**/**Shift** + a number, or the **note** pad, pencils in a candidate.
- Select several cells (shift-click or drag) and a number pencils a note into
  all of them at once.
- **Ctrl+Z** / **Ctrl+Y** undo and redo, **H** for a hint, **P** to pause,
  **R** toggles the row/column/box highlight.

## Notes

- Fonts load from Google Fonts; without a connection both pages still work and
  fall back to system fonts.
- The animations on the guide are CSS and DOM, not video or GIF files — they
  stay crisp at any size and add nothing to load time.
- Nothing persists between sessions. Puzzles travel as 81-character codes.
