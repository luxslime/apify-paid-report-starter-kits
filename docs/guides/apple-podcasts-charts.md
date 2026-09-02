# Apple Podcasts charts

Pull official Apple Podcasts rankings by country, then export ranked show or episode rows for market tracking.

**Use the Actor:** [Apple Podcasts / iTunes Scraper: Search, Charts, Episodes](https://apify.com/taroyamada/apple-podcast-scraper)

**Price:** Result $2.50/1,000. Start $0.005. Confirm the live Store page before a paid run.

Charts are a follow-on lane. The cheapest first paid run is a small search with `includeEpisodes` false: [starter JSON](https://github.com/luxslime/apify-paid-report-starter-kits/blob/master/inputs/apple-podcast-scraper.json).

Related: [overview](apple-podcasts-scraper-apify.md) · [search](apple-podcasts-search-discovery.md) · [watchlists](apple-podcasts-watchlists.md) · [HTML charts page](../tools/apple-podcasts-scraper/charts.html)

## Workflow

1. Leave `searchTerm` empty for a charts-only run.
2. Set `chartRequests` with a country, feed type, and limit.
3. Use `feedType`: `podcasts` for show charts, or `podcast-episodes` for episode charts.
4. Override `country` per request when you need more than one storefront.
5. Keep `includeEpisodes` off until episode titles add value.
6. Read `rank`, `showName`, `publisher`, and `sourceUrl` in the dataset.

Example input:

```json
{
  "chartRequests": [
    { "country": "us", "feedType": "podcasts", "limit": 25 }
  ]
}
```

Chart requests can mix storefronts. A second item can use another country or `podcast-episodes` without changing the default `country` used by search or lookup.

## What the ranks mean

`rank` is filled on chart rows. Rankings are public Apple chart data, not private listener counts or verified audience size. Use them as a source-linked snapshot for human review.

## Limits

- Public Apple / iTunes ranking feeds only. No login or private analytics.
- Chart coverage and order can change; this page does not freeze a quote or a ranking outcome.
- Not affiliated with or endorsed by Apple.

## Run a chart request

Start with one country and a modest `limit`, inspect the ranked dataset, then scale.

**[Get Apple Podcasts chart data](https://apify.com/taroyamada/apple-podcast-scraper)** — Result $2.50/1,000. Start $0.005.
