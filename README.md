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

    cd ~/Code/experiai/lab/iris/site && vercel deploy --prod --yes
    npx vercel alias set <deployment-url> iris.experiai.com

The alias is a separate step on every prod deploy (see the Lab CLAUDE.md). Verify on https://iris.experiai.com,
never on the deployment URL.
