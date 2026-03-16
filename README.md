# Operation Epic Fury — Cost Tracker

A daily cost tracker for the U.S. military campaign against Iran, based on CSIS Defense 360 analysis by Mark F. Cancian and Chris H. Park.

**Live site:** (https://andysaulim.github.io/Iran-War-Tracker/))

## Sources
- [CSIS, Mar 13 2026 — D+6 update ($11.3B)](https://www.csis.org/analysis/iran-war-cost-estimate-update-113-billion-day-6-165-billion-day-12)
- [CSIS, Mar 5 2026 — H+100 estimate ($3.7B)](https://www.csis.org/analysis/37-billion-estimated-cost-epic-furys-first-100-hours)

## Deployment

Hosted via GitHub Pages. No build step — single `index.html` file.

To deploy:
1. Push this repo to GitHub
2. Go to Settings → Pages → Source: Deploy from branch → `main` → `/ (root)`
3. Site will be live at `(https://andysaulim.github.io/Iran-War-Tracker/)`

## Updating data

Open the live site, click **⚙ Editor** in the Daily Cost Log section, enter the passphrase, and add/update entries. Data persists in the visitor's browser via `localStorage`. To update the default dataset for all visitors, edit the `DEFAULT` array in `index.html` and push.

## Credits

Beyond Parallel / Andy Lim Projects · not affiliated with CSIS
