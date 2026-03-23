# Talia Job Tracker - GitHub Pages

This is a static GitHub Pages app.

## Files
- `index.html`: frontend
- `jobs.json`: data source

## How it works
- The app fetches `jobs.json`
- It shows all jobs in an active section
- When you check `Mark as applied`, that role moves to the applied section
- Applied state is saved in browser localStorage
- `Export current jobs JSON` downloads a merged JSON so you can commit your latest changes back to the repo

## Recommended workflow
1. Keep `jobs.json` as the source of truth in the repo
2. Use the site daily to review and mark jobs applied
3. Periodically export the updated JSON
4. Replace `jobs.json` in the repo with the exported file
5. Commit and push

## Deploy on GitHub Pages
1. Create a GitHub repo, for example `talia-job-tracker`
2. Upload `index.html` and `jobs.json` to the repo root
3. In GitHub, go to Settings -> Pages
4. Under Build and deployment, choose `Deploy from a branch`
5. Select branch `main` and folder `/root`
6. Save
7. GitHub will publish the site after the next push

## Data shape
Each job should look like this:

```json
{
  "id": "unique-id",
  "title": "Mechanical Engineer I",
  "company": "Example Company",
  "location": "Madison, WI",
  "industry": "Industrial Manufacturing",
  "alignment": "high",
  "commuteMinutes": 18,
  "commuteBand": "30",
  "link": "https://example.com/jobs/123",
  "source": "LinkedIn",
  "postedDate": "2026-03-23",
  "notes": "Strong fit because of process, CAD, and manufacturing background.",
  "applied": false
}
```
