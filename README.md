# Sim Night

A game simulator for the NBA, NHL, soccer and the NFL that runs in your phone’s browser. Pick two teams, play the game, and get the final score, a period-by-period line score, team stats, player stats, a scoring summary and a player of the game. You can also run 1,000 games to see each team’s win chances.

## Put it on your iPhone

1. Upload every file in this folder to a new GitHub repository (Add file → Upload files).
2. In the repository, open **Settings → Pages**. Under “Build and deployment”, choose **Deploy from a branch**, pick **main** and **/ (root)**, then tap **Save**.
3. Wait a minute or two. GitHub shows your site’s link at the top of the Pages screen (something like `https://your-name.github.io/sim-night/`).
4. Open that link in **Safari**, tap the **Share** button, then **Add to Home Screen**.

It now opens full screen like an app.

## How the simulation works

- **NBA:** about 100 possessions per team, each one ending in a shot, free throws or a turnover. Rebounds, assists, steals and blocks go to players based on their role.
- **NHL:** shots, power plays and goals period by period, with overtime and a shootout when tied.
- **Soccer:** every minute both teams can create a chance with an expected-goals (xG) value. Includes penalties, cards and player ratings.
- **NFL:** each team gets about 11 drives that end in a touchdown, field goal, punt or turnover, with yards split between passing and rushing.

Stronger teams (higher rating) score more and allow less, and the home team gets a small boost unless you tick “Neutral site”.

## Change teams, ratings or players

- **In the app:** tap **Edit player names** to rename players for any team. Changes save on your phone.
- **In the code:** open `index.html` and find the `TEAMS` list near the top of the script. Each team looks like this:

  ```
  ["BOS","Boston Celtics",84,"Jayson Tatum|Jaylen Brown|Derrick White|Payton Pritchard|Neemias Queta"]
  ```

  That’s the abbreviation, the full name, a strength rating (about 60–95) and the players, separated by `|`. Player order matters; the `ROLES` list just above it explains each position.

Ratings and rosters are estimates as of mid-2026, so update them whenever teams change.

## Files

| File | What it’s for |
|---|---|
| `index.html` | The whole app |
| `manifest.webmanifest` | App name and icons for the home screen |
| `apple-touch-icon.png` | iPhone home screen icon |
| `icon-192.png`, `icon-512.png` | Icons for other devices |
