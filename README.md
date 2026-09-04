# Sudoku Workbench

A single-file Sudoku trainer: solve puzzles yourself, with mistake checking, and
ask for the logic only when you want it. Twenty solving techniques, each with
spotting tips and worked examples on part-solved grids.

## Hosting

`index.html` is completely self-contained — no build step, no dependencies, no
server-side code. Drop it in any static host.

For GitHub Pages: put `index.html` in the repository root, then
**Settings → Pages → Source: Deploy from a branch → main → /(root)**.

## Notes

- Fonts load from Google Fonts. Without a connection the app still works, it
  just falls back to system fonts.
- Nothing is stored between sessions; puzzles travel as 81-character codes you
  can copy and paste.
