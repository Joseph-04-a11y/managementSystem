# BIRS Makurdi Monitoring Demo

An interactive demonstration built by Kimbly Technologies for business and taxpayer monitoring in Makurdi, Benue State.

## Included features

- Business and property registration with linked plaza shops.
- Customer location map with pending (P), verified (V), and follow-up (F) indicators.
- Searchable customer records and verification queue.
- Full business details, editing, verification, follow-up, and field-visit actions.
- Browser localStorage persistence for records, visits, and activity history.
- BIRS branding and Roboto typography.

## Run locally

With Python 3 installed, run from the repository root:

```bash
python -m http.server 8000 --directory dist
```

Open http://localhost:8000 in your browser. Internet access is needed for the D3 map library, Lucide icons, and Google Fonts loaded from CDNs. The sourced road geometry and BIRS logo are embedded in the page.

## Project structure

- `dist/index.html`: complete editable static application, including styles, scripts, sample data, and map geometry. No build step is required.
- `.openai/hosting.json`: configuration identifying the existing privately hosted Sites project.

## Demo behaviour

New registrations are pending review and immediately appear on the map. Verification changes their indicator to verified. Editing a record returns it to pending review. Records are stored under `birs-makurdi-demo-v2` in localStorage and remain available after reloads in the same browser and site origin. They do not sync between devices or between localhost and the hosted demo.

GPS capture is simulated. All initial customer records are fictional and their locations illustrative. Verification is a demonstration workflow, not an official tax-compliance determination. This version has no application backend or role enforcement and is not intended for real taxpayer data.

## Map attribution

Road geometry is sourced from OpenStreetMap via Overpass. Map data © [OpenStreetMap contributors](https://www.openstreetmap.org/copyright), licensed under ODbL.

## Hosted demo

https://birs-makurdi-monitoring-demo.best-kimbly.chatgpt.site

The existing hosted demo is private to its owner. Uploading this source to GitHub does not change that access or configure automatic deployment from GitHub.
