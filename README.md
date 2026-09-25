# Lock Ladder Scoreboard

Leaderboard for the LASCON 2026 progressive lockpicking contest (Oct 29–30, locksport table, vendor room).

- **Judge view:** open the site on the laptop. Sign people up and record each open (level + time taken).
- **Projector view:** click **Open projector window** and drag that window to the projector, or open `?view=display`.

- **Public page:** `?view=live` works on any phone or laptop and refreshes every minute.

Scores are stored in the laptop browser's local storage and sync between the two windows. Use **Export backup** at every break.

## Online copy

The judge page publishes `scores.json` to the `scores` branch (not `main`, so GitHub Pages never rebuilds) a few seconds after every change; the public page reads it through the GitHub API. Nothing to pay for, no server.

It needs a **fine-grained personal access token** saved on the judge laptop (Online scoreboard card):
- Repository access: only `dougray/lascon-lockpick-scoreboard`
- Permissions: Contents → Read and write (nothing else)
- Expiration: after the event (e.g. 2026-11-15)

The token never leaves that laptop's browser except to call api.github.com. Revoke it after LASCON.

Scoring: level points (10/20/35/50/75) + 1 bonus point per full 30 s left on the level's clock (5/5/10/10/15 min). Ties go to highest level, then fastest open on it. Top 5 at the 2:00 pm Friday cutoff go to the final.
