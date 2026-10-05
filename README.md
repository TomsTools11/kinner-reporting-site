# Shane Kinner Agency Reporting

Static reporting hub for Shane Kinner Agency (Allstate, Gloucester Point VA), deployed on Vercel.

The root URL (`/`) is the report hub, with one card per report. Each report has an "← All Reports" button at the top of its sidebar that returns to the hub (hidden when printed).

## Repository layout

```
public/            # everything in here is deployed and publicly reachable
  index.html       # report hub (served at /)
  reports/
    campaign-configuration-2026-10-05.html   # /reports/campaign-configuration-2026-10-05 (VA Auto)
  assets/
    va-map.svg     # Virginia county/independent-city map, statewide targeting
  robots.txt       # asks crawlers not to index the reports
vercel.json        # output directory, clean URLs, security + noindex headers
```

## Vercel project settings

Zero-build static site. Framework Preset **Other**, no build or install command, Output Directory `public` (set in `vercel.json`), Root Directory `./`.

`/campaign-configuration` redirects to the current configuration report.
