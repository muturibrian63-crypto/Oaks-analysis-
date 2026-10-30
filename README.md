# Pitch Report

Football predictions and value flags. A Python script builds the day's predictions on GitHub, and a purple and yellow web page shows them. Open the page in Chrome, or install it from Chrome's menu as an app.

## Files in this repository

- `api_football_daily.py`: the prediction script (free data from football-data.co.uk)
- `requirements.txt`: Python packages
- `index.html`, `manifest.webmanifest`, `sw.js`, `icon-192.png`, `icon-512.png`, `icon-512-maskable.png`: the web page
- `.github/workflows/daily.yml`: runs the script every day and publishes the page

## Set up

1. Create a public repository on github.com.
2. Add every file above with Add file, then Upload files. Upload the `.github/workflows/daily.yml` file with Add file, then Create new file: type `.github/workflows/daily.yml` as the name and paste the contents.
3. Settings, then Pages: set Source to **GitHub Actions**.
4. Actions tab, **Daily soccer analysis**, **Run workflow**.
5. When it finishes, open `https://YOUR-USERNAME.github.io/REPOSITORY-NAME/` in Chrome. It refreshes at 06:00 and 13:00 Nairobi time.

## Notes

- Only leagues in football-data.co.uk's fixtures file are covered.
- That source has odds only for results and over/under 2.5. For every other market, including corners, type in odds from your bookmaker to see value.
- If a run fails over an old action version, update the numbers after the `@` signs in `daily.yml`.
- Estimates only, not tips.
