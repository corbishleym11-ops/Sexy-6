# Sexy 6 — 2026 Dashboard

## Upload these five files to the repo root

- `index.html` — the dashboard
- `support.js` — required runtime (page is blank without it)
- `sexy6-mark.png` — the midfield logo watermark
- `league.json` — the league's picks and scores
- `README.md` — this file

## Turn on GitHub Pages

Settings -> Pages -> Source: **Deploy from a branch** -> branch `main`, folder `/ (root)`.
Your board is then at `https://<you>.github.io/<repo>/`.

## Running the league (commissioner)

Open the board with `?commish` on the end of the URL, e.g.
`https://<you>.github.io/<repo>/?commish` — or click **commish mode** in the header.
Everyone else gets a read-only board.

**Weekly routine**

1. **Pull games from feed**, then click six games to set the slate.
2. Lines and totals float with the feed until **Thursday 7:00 AM ET**, then freeze on their own.
   There is a **lock now** override if you want them frozen early.
3. Click the M / A / S buttons under Favorite, Underdog, Over and Under to enter picks.
   Duplicate selections are blocked.
4. Pick super dogs from the dropdown — +10 or worse, and never a game on the slate.
   (No super dogs in week 0.)
5. Hit **Export league.json**, replace the file in the repo, commit. Everyone sees it on refresh.

**Preseason:** enter all 24 win-total picks on the Win Totals tab, export and commit before week 0.
Type each team's record like `7-3` during the season to drive the clinched / alive / dead tracker.

## Scoring

- Favorite, underdog, over, under: **1 point** each, **0.5** for a push.
- All four correct: **+1 bonus** (a five-point week).
- Super dog cover: **0.5**. Outright win: **2**.
- Win totals: **1 point** each, settled after the regular season.
- Records track wins, losses and pushes separately from points.
- A super dog that is picked and wins outright is honoured in **Giant Killers** and retired
  from future selection. Unpicked outright winners stay eligible.

## Good to know

- Live scores come from ESPN's public scoreboard and update for everyone while the page is
  open — no commits needed during games. Picks are never affected.
- ESPN deletes the spread once a game is final, so the board snapshots lines while games are
  live. Keep the board open in commish mode on Saturdays so the **Dogs that won last week**
  widget has data.
- Every game also has a manual final-score box (`24-31`) in the slate editor as a backup.
- Anyone can flip themselves into commish mode, but their edits stay in their own browser.
  The committed `league.json` is the only source of truth.
- Bowl season rules to be sorted in December.
