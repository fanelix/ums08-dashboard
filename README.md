# UMS-08 PLS Monitoring Dashboard

**Site:** Tujuh Bukit Gold Project, PT Bumi Suksesindo  
**Station:** UMS-08 Primary Liner System Totalizer

## Files

| File | Purpose |
|---|---|
| `index.html` | Live dashboard — reads from Google Sheets CSV, falls back to `data.json` |
| `data.json` | Canonical data snapshot (397 rainfall · 105 totalizer · 25 water level rows) |
| `form.html` | Mobile data-entry form (deployed separately via Apps Script) |
| `_apps_script/Code.gs` | Apps Script backend — paste into Google Apps Script editor |

## Setup

1. Enable GitHub Pages: `Settings → Pages → Deploy from branch → main / root`
2. Dashboard live at: `https://<username>.github.io/<repo>/`
3. Update `SCRIPT_URL` in `form.html` after Apps Script deployment

## Data Source

Google Sheets "UMS-08 Data" — three tabs published as CSV.  
Dashboard auto-falls back to bundled `data.json` if CSV fetch fails.
