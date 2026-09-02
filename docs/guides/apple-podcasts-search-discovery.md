# Apple Podcasts search and discovery

Find public shows by keyword in any Apple country storefront, then reuse the returned collection IDs and Store URLs for charts, watchlists, or a shortlist.

**Use the Actor:** [Apple Podcasts / iTunes Scraper: Search, Charts, Episodes](https://apify.com/taroyamada/apple-podcast-scraper)

**Price:** Result $10/1,000. Start $0.005. Confirm the live Store page before a paid run.

Related: [overview](apple-podcasts-scraper-apify.md) · [charts](apple-podcasts-charts.md) · [watchlists](apple-podcasts-watchlists.md) · [HTML search page](../tools/apple-podcasts-scraper/search.html) · [starter JSON](https://github.com/luxslime/apify-paid-report-starter-kits/blob/master/inputs/apple-podcast-scraper.json)

## Cheapest first paid run

This is the Store quickstart: one small search, no charts, no watchlists, `includeEpisodes` false. It matches the live input-schema example (`searchTerm` prefill `technology`, `limit` prefill `3`).

```json
{
  "searchTerm": "technology",
  "chartRequests": [],
  "lookupIds": [],
  "country": "us",
  "limit": 3,
  "includeEpisodes": false,
  "delivery": "dataset",
  "dryRun": false
}
```

Checked-in copy: [inputs/apple-podcast-scraper.json](https://github.com/luxslime/apify-paid-report-starter-kits/blob/master/inputs/apple-podcast-scraper.json).

```bash
apify actors call taroyamada/apple-podcast-scraper --input-file inputs/apple-podcast-scraper.json --output-dataset
```

Do not add `chartRequests` or `lookupIds` on the first paid run. Leave `includeEpisodes` false until episode rows are required.

## Workflow

1. Set `searchTerm` (Store prefill: `technology`).
2. Set `country` (`us`, `gb`, `jp`, and other Apple storefront codes) and a small `limit` (Store prefill: `3`).
3. Keep `includeEpisodes` false for the cheapest first success.
4. Inspect `showName`, `publisher`, `collectionId`, and `sourceUrl`.
5. Pass useful `collectionId` values into a [watchlist](apple-podcasts-watchlists.md), or add a [chart](apple-podcasts-charts.md) request once search output is useful.

Search is the lowest-friction first run. At least one of `searchTerm`, `chartRequests`, or `lookupIds` is required; start with search only, then add the other lanes.

## What search does not return

Search uses the public iTunes Search API. `rank` is a chart field and is typically `null` on search rows. Search does not provide private listener counts, emails, or account data.

## Limits

- Public Apple / iTunes search only. No login, private dashboards, or listener PII.
- Public catalog results can be incomplete or delayed.
- Not affiliated with or endorsed by Apple.

## Run a search

Run the 3-result search starter, inspect the dataset, then scale the `limit` or add charts and watchlists.

**[Search Apple Podcasts now](https://apify.com/taroyamada/apple-podcast-scraper)** — Result $10/1,000. Start $0.005.
