# Apple Podcasts scraper Apify: RSS vs Store notes

Short notes for teams that collect **public Apple Podcasts metadata** on [Apify](https://apify.com). This page compares typical **RSS** collection with **Store / iTunes API** scrapers. It does not rank vendors or invent speed, coverage, or cost benchmarks.

**Use the Actor:** [Apple Podcasts Scraper on Apify](https://apify.com/taroyamada/apple-podcast-scraper)

**Discovery docs:** [overview](../tools/apple-podcasts-scraper/), [search](../tools/apple-podcasts-scraper/search.html), [charts](../tools/apple-podcasts-scraper/charts.html), [watchlists](../tools/apple-podcasts-scraper/watchlists.html)

**Price:** From $10 per 1,000 results. Confirm the live Store page before a paid run.

## What this Apple Podcasts scraper on Apify is for

[Apple Podcasts Scraper: Search, Charts, Episodes & Watchlists](https://apify.com/taroyamada/apple-podcast-scraper) is a discovery and metadata Actor. It uses public Apple / iTunes endpoints (the Store listing notes no proxy). Typical jobs:

- **Search** — keyword discovery via the iTunes Search API
- **Charts** — country storefront rankings for podcasts or podcast episodes
- **Episodes** — optional recent-episode rows for resolved shows
- **Watchlists** — refresh known Apple collection IDs via the iTunes Lookup API

It is a related Actor to this starter-kit catalog, not one of the eight priced report starters.

## RSS collection vs Store scrapers

These are different jobs that sometimes share show title and publisher. Neither approach is universally “better.”

### RSS collection

Typical when you already have public feed URLs:

- Strong for episode lists, publish dates, descriptions, and enclosure / audio URLs in the feed
- Useful for cadence checks and show-level tags that publishers put in RSS
- Does not, by itself, provide Apple catalog search, country charts, or Apple collection IDs
- Incomplete if the feed is truncated, delayed, or missing iTunes namespace tags

### Apple Podcasts Store / iTunes API scrapers

Typical when you need Storefront discovery rather than a known feed:

- Strong for **search**, **charts**, Apple IDs, artwork, genres as Apple classifies them, and Store URLs
- Fits recurring **watchlists** of known collection IDs
- Episode depth is often a recent subset unless the tool also reads RSS
- Usually omits full historical archives and some enclosure fields that live only in the feed

### Overlap

Both can return show name, publisher, and a public source URL. Choose RSS when the feed is the source of truth for episodes. Choose a Store scraper when you need search, charts, or ID-based watchlists.

## What this Actor covers

| Lane | Input | Typical output |
| --- | --- | --- |
| Search | `searchTerm` | Show rows from Apple search |
| Charts | `chartRequests` | Ranked podcast or episode rows |
| Watchlists | `lookupIds` | Resolved shows for a known ID list |
| Episodes | `includeEpisodes` | Recent episode rows on resolved shows |

At least one of `searchTerm`, `chartRequests`, or `lookupIds` is required. Delivery can be dataset or webhook. `dryRun` validates setup without saving payable rows.

## Pricing note

Store listing: **From $10 per 1,000 results** (pay per event: result rows plus a small actor-start event). Empty unchanged watchlist polls are documented as avoiding payable default-dataset writes when there is nothing new to emit. Review current pricing on the Store page; this notes page does not freeze a quote.

## Limits (no extra claims)

- Public Apple and RSS metadata only; no private dashboards, logins, or account sessions
- Public catalog and feed data can be incomplete or delayed
- Rows are source-linked observations, not audience size, ranking advice, or business-outcome claims
- Not affiliated with or endorsed by Apple or Apify

## Run the Apple Podcasts scraper on Apify

**[Open Apple Podcasts Scraper](https://apify.com/taroyamada/apple-podcast-scraper)** — search, charts, episodes, and watchlists. From $10 per 1,000 results.

Related in this repo: the [Apple Podcasts Scraper discovery page](../apple-podcasts-scraper/index.html), [HTML tools docs](../tools/apple-podcasts-scraper/) ([search](../tools/apple-podcasts-scraper/search.html), [charts](../tools/apple-podcasts-scraper/charts.html), [watchlists](../tools/apple-podcasts-scraper/watchlists.html)), and the [Apple Podcasts Category Benchmark](https://apify.com/taroyamada/podcast-category-network-benchmark-report) starter kit, which uses public Apple metadata and public RSS for a capped planning sample.
