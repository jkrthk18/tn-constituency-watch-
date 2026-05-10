# TN Constituency Watch · 2026

A civic accountability dashboard for the Tamil Nadu 17th Legislative Assembly (2026).

**Live site:** https://YOUR_USERNAME.github.io/tn-constituency-watch

---

## What this does

- Interactive Tamil Nadu map — click any constituency to see MLA profile
- 2026 election results: winner, party, margin, runner-up
- Links to ECI affidavit and MyNeta criminal record data for each MLA
- Manually-updated progress tracker for schemes, RTI responses, fund utilisation

## Data sources

| Data | Source |
|------|--------|
| Election results | Election Commission of India (results.eci.gov.in) |
| Affidavit & criminal records | ADR / MyNeta (myneta.info) |
| Constituency boundaries | Datameet India Maps (GeoJSON) |
| Progress tracking | This repo — manually maintained |

## How to add tracking entries

Drop a markdown file in `data/track/CONSTITUENCY_NAME.md` using this format:

```markdown
# Constituency Name – Progress Tracker
**MLA:** Name (Party)
**Last updated:** YYYY-MM-DD

## Schemes & Announcements
- [ ] Scheme name – date (amount if known)

## RTI / News Links
- DATE | SOURCE | SUMMARY | URL

## Notes
Free text notes here.
```

The site reads these files automatically via GitHub's raw content API.

## How to update constituency data

Edit `data/constituencies.json` — each entry has:
```json
{
  "no": 12,
  "name": "PERAMBUR",
  "winner": "VIJAY",
  "party": "TVK",
  "runner": "...",
  "runner_party": "DMK",
  "margin": 0,
  "district": "Chennai",
  "myneta_url": "https://myneta.info/..."
}
```

## Deploy to GitHub Pages

1. Create a public repo named `tn-constituency-watch`
2. Push these files to the `main` branch
3. Go to Settings → Pages → Source: Deploy from branch → Branch: main → / (root)
4. Site goes live at `https://YOUR_USERNAME.github.io/tn-constituency-watch`

---

*Data is sourced from public records. All affidavit data links to official ECI/MyNeta sources.*
