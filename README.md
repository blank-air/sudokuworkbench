# Sudoku Workbench

A single-file Sudoku trainer. Solve puzzles yourself with mistake checking, and
ask for the logic only when you want it — twenty solving techniques, each with
spotting tips and worked examples on part-solved grids. Optional live rooms let
several people solve the same grid together.

## Hosting

`index.html` is self-contained: no build step, no bundler, no server code.
Drop it on any static host.

For GitHub Pages, put `index.html` in the repository root, then
**Settings → Pages → Source: Deploy from a branch → main → /(root)**.

## Optional: live rooms

Solo play needs no setup. Shared rooms need something to relay messages between
players, which a static host can't do. Supabase Realtime handles this on its free
tier, and needs **no database tables** — only broadcast and presence.

1. Create a free project at [supabase.com](https://supabase.com).
2. Your **Project URL** is `https://<project-id>.supabase.co` — the project ID is
   on **Project Settings → General**, and the URL is also shown on
   **Project Settings → Data API**.
3. Open **Project Settings → API Keys** and copy the **publishable** key
   (`sb_publishable_...`). Older projects label this the **anon / public** key;
   either works. Do not use the **secret** key.
4. Paste both into `SUPABASE_URL` and `SUPABASE_KEY` near the top of the
   `<script>` block in `index.html`.

The project's **Connect** button shows the URL and key together, which is the
quickest way to grab both. The publishable key is designed to be published, so it
is safe in a public repo. Rooms
hold no server-side state: the relay just forwards messages between whoever is
connected, so a room empties when the last player leaves.

## Notes

- Fonts load from Google Fonts; without a connection the app still works and
  falls back to system fonts.
- The Supabase client is imported only when you actually open a room.
- Nothing persists between sessions. Puzzles travel as 81-character codes you
  can copy, paste and share.
