# Apple Podcasts search and discovery

Find public shows by keyword in any Apple country storefront, then reuse the returned collection IDs and Store URLs for charts, watchlists, or a shortlist.

**Use the Actor:** [Apple Podcasts Scraper on Apify](https://apify.com/taroyamada/apple-podcast-scraper)

**Price:** From $10 per 1,000 results. Confirm the live Store page before a paid run.

Related: [overview](apple-podcasts-scraper-apify.md) · [charts](apple-podcasts-charts.md) · [watchlists](apple-podcasts-watchlists.md)

## Workflow

1. Set `searchTerm` (Store prefill: `technology`).
2. Set `country` (`us`, `gb`, `jp`, and other Apple storefront codes) and a small `limit` (try `10`).
3. Keep `includeEpisodes` false for the cheapest first success.
4. Inspect `showName`, `publisher`, `collectionId`, and `sourceUrl`.
5. Pass useful `collectionId` values into a [watchlist](apple-podcasts-watchlists.md), or add a [chart](apple-podcasts-charts.md) request once search output is useful.

Example input:

```json
{
  "searchTerm": "technology",
  "country": "us",
  "limit": 10
}
```

Search is the lowest-friction first run. At least one of `searchTerm`, `chartRequests`, or `lookupIds` is required; start with search only, then add the other lanes.

## What search does not return

Search uses the public iTunes Search API. `rank` is a chart field and is typically `null` on search rows. Search does not provide private listener counts, emails, or account data.

## Limits

- Public Apple / iTunes search only. No login, private dashboards, or listener PII.
- Public catalog results can be incomplete or delayed.
- Not affiliated with or endorsed by Apple.

## Run a search

Run a 10-result search, inspect the dataset, then scale the `limit` or add charts and watchlists.

**[Search Apple Podcasts now](https://apify.com/taroyamada/apple-podcast-scraper)** — From $10 per 1,000 results.
