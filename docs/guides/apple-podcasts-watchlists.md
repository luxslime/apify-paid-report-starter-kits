# Apple Podcasts watchlists

Refresh known shows by Apple collection ID. Use this lane when you already have a shortlist and want recurring public metadata (and optional recent episodes).

**Use the Actor:** [Apple Podcasts / iTunes Scraper: Search, Charts, Episodes](https://apify.com/taroyamada/apple-podcast-scraper)

**Price:** Result $10/1,000. Start $0.005. Confirm the live Store page before a paid run.

Watchlists are a follow-on lane. The cheapest first paid run is a small search with `includeEpisodes` false: [starter JSON](https://github.com/luxslime/apify-paid-report-starter-kits/blob/master/inputs/apple-podcast-scraper.json).

Related: [overview](apple-podcasts-scraper-apify.md) · [search](apple-podcasts-search-discovery.md) · [charts](apple-podcasts-charts.md) · [HTML watchlists page](../tools/apple-podcasts-scraper/watchlists.html)

## Workflow

1. Collect Apple Podcasts **collection IDs**. Take them from a search or chart run, or from the `id…` segment of a public Apple show URL (for example `1535144780` from `…/id1535144780`).
2. Pass the IDs as `lookupIds`.
3. Set `includeEpisodes`: `true` only when recent episode titles help the workflow.
4. Keep the first run small. After the payload looks right, schedule recurring runs.
5. Optional: switch `delivery` to `webhook` (Slack, Discord, Zapier, or any HTTP endpoint) after you approve the shape. Use `dryRun` first.

Example input:

```json
{
  "lookupIds": ["1535144780"],
  "country": "us",
  "includeEpisodes": true
}
```

There is no dedicated show-URL input. Resolve a known show with its numeric collection ID. Public Apple pages appear as `sourceUrl` on output rows.

## Recurring runs and billing

Unchanged watchlist polls are documented as avoiding payable default-dataset writes when there is nothing new to emit. `dryRun` validates setup without saving results or firing webhooks. Review live Store pricing before a paid run.

## Limits

- Watchlists resolve **public** show metadata via the iTunes Lookup API. No private podcast dashboards, logins, or listener analytics.
- Public catalog and feed data can be incomplete or delayed.
- Not affiliated with or endorsed by Apple.

## Set up a watchlist

Add your collection IDs, inspect one dataset, then schedule the refresh.

**[Set up a podcast watchlist](https://apify.com/taroyamada/apple-podcast-scraper)** — Result $10/1,000. Start $0.005.
