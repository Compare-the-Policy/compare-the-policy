# Compare the Policy

A plain-language, single-page comparison of what Australia's federally registered
political parties are proposing — 34 parties, 511 policies, grouped into 21
standardised categories. No accounts, no election picker, no ranking of parties.

## Status

First-pass frontend. Party names, policy titles, categories and sources come from
a research pass dated 21 September 2026 (some sources still marked as needing
verification — see the ⓘ note and party-level notes on the page itself).

## Running it

This is a single self-contained file with no build step and no dependencies
beyond two Google Fonts loaded over HTTPS.

```
open index.html
```

or serve the folder with any static file server (e.g. `npx serve .`) and open it
in a browser. To publish via GitHub Pages, push this repo and enable Pages on
the `main` branch — `index.html` at the repo root is picked up automatically.

## Structure

- `index.html` — the whole app: markup, styles, and vanilla JS (no framework,
  no bundler). All party/category/policy data lives in the `SRC`, `CATS`,
  `SUMMARY`, `SRC_OVERRIDE` and `STATUS_NOTE` objects near the bottom of the
  file — that's the dataset to edit as parties update their policies.

## What's next

- Real backend/data pipeline (this repo is frontend + seed data only, per the
  original brief — no backend architecture is assumed here)
- Linking each policy to its original source passage, not just the source page
- Ongoing monitoring of party sites for added/changed/removed policies
