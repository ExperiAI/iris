# Iris — every place has an eye

A year of hourly weather (Open-Meteo / ERA5) drawn as the iris of a place: one fibre per day, midnight at the
pupil, midnight at the rim; the dark is night, so the pupil's shape is the latitude; the colour is the
temperature; a white dot is a rainy hour. ExperiAI Lab experiment 02.

Live: https://iris.experiai.com

## Where things come from

The page is BUILT, not edited here. Source, data and tools live in the studio repo:
`~/Code/experiai/studio/productions/experiment-02/iris/` (`template.html`, `build.py`, `assets/`) and
`~/Code/experiai/studio/tools/iris*.py`. Rebuild the site with

    python3 ~/Code/experiai/studio/productions/experiment-02/iris/build.py --site ~/Code/experiai/lab/iris/site

`site/` is the deployable static folder: `index.html`, `data.js` (25 places × 4 years packed 5 bytes/hour,
Biasca every decade), the face plates and the four macro eye plates.

## Deploy

    ~/Code/experiai/lab/autorun/deploy-exhibit.sh iris

(deploys `site/`, sets the alias, verifies iris.experiai.com; by hand it is `vercel deploy --prod --yes` in
`site/` then `npx vercel alias set <deployment-url> iris.experiai.com`).

The alias is a separate step on every prod deploy (see the Lab CLAUDE.md). Verify on https://iris.experiai.com,
never on the deployment URL.

## State (2026-09-27)

Live and listed in the Lab gallery (website PR #16). Wetness levels by yearly rain: <400 mm drier, <900 dry,
<1400 brimming, <2200 a tear, above weeping; one rule for the hero, the card and the opened eye. The month
marker during the reveal is the word (Diego's pick); `#months=strip` and `#months=none` show the alternatives.

Repo: https://github.com/ExperiAI/iris (remote `github-experiai:ExperiAI/iris.git`). Announcement copy is in
`~/AI-Drafts/2026-09-27/iris-launch-linkedin.txt`. A film trailer of the reveal is optional.
