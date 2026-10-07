# Sudoku Workbench

A four-page Sudoku trainer. Every page is self-contained — no build step, no
bundler, no dependencies, no server code.

- **`index.html`** — the board. Solve it yourself with mistake checking, and ask
  for the logic only when you want it.
- **`solve.html`** — step-by-step walkthrough. Paste a puzzle code (or arrive
  from the board with **Walk through →**) and step through the whole solve, one
  named deduction at a time.
- **`library.html`** — all twenty techniques, each explained, each with tips for
  spotting it, and each played out on three real positions.
- **`stuck.html`** — what to do when you're stuck: a triage, then a fixed ladder
  of passes from cheapest to most expensive.

## Hosting

Put all four files in the repository root. For GitHub Pages:
**Settings → Pages → Source: Deploy from a branch → main → /(root)**.
The pages link to each other by relative filename, so they must share a folder.

## Input on the board

- Select a cell and press **1**–**9** to place a digit.
- **Ctrl**/**Shift** + a number, or the **note** pad, pencils in a candidate.
- Select several cells (shift-click or drag) and a number pencils a note into
  all of them at once.
- **Ctrl+Z** / **Ctrl+Y** undo and redo, **H** for a hint, **P** to pause,
  **R** toggles the row/column/box highlight.

## The walkthrough page

Takes a puzzle code in the URL as `solve.html#p=<81 characters>`, so you can
bookmark or share a specific puzzle's solution path. Every move is listed and
clickable; **Skip to next interesting** jumps past the routine singles.
Arrow keys step, space plays.

## Notes

- Animations are CSS and DOM rather than video or GIF files, so they stay crisp
  at any size and cost nothing to load.
- Every board shown in the library is a genuine mid-solve position, and every
  mark, elimination and placement was verified against the finished puzzle.
- Fonts load from Google Fonts; without a connection everything still works and
  falls back to system fonts.
- Nothing persists between sessions. Puzzles travel as 81-character codes.
