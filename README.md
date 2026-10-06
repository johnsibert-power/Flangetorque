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

## Voice control
Web Apps can't use the microphone, so voice goes through Meta AI via WebMCP: the
page registers tools on `document.modelContext` and the wearer says "Hey Meta, …"
in their own words ("done", "next", "flag it, threads are stripped", "which bolt?").
Tools change per screen and every one mirrors a button, so the app still works by
hand. If the wearer names a bolt that isn't the one on screen, nothing is recorded.

WebMCP is off by default: the glasses need Developer Mode (restart the glasses and
the Meta AI app after enabling it) or rollout eligibility. Test locally with the
Display Simulator's voice agent.

## Configure
Edit the `JOB` object at the top of the script in `index.html` (work order, flange,
bolt count, target torque, passes).
