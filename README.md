# Flange torque walkthrough

A standalone Web App for Meta Ray-Ban Display glasses that guides a technician
through a sequential flange bolt torque procedure (star pattern, staged passes,
final circular check) and records a confirmation for every bolt.

Single file, no build step: `index.html`.

## Run locally
    npm install
    npm run dev
Open http://localhost:8777/ in Chrome with the Meta Ray-Ban Display Simulator extension.

## Deploy
Static host with HTTPS (Vercel, GitHub Pages, Netlify). Then in the Meta AI app:
Developer Mode → App Settings → Apps → Web Apps → Connect Web App → paste the URL.

## Configure
Edit the `JOB` object at the top of the script in `index.html` (work order, flange,
bolt count, target torque, passes).
