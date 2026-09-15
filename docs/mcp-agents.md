# MCP / agent Store IDs and minimal Input JSON

Use these exact Store IDs (`username/name`) with Apify MCP, the Apify CLI, Make, or n8n. Do not pass display titles.

Machine catalogs:

- Publisher earn-first listing (no prices): [https://apify.momiji-space.com/llms.txt](https://apify.momiji-space.com/llms.txt)
- This repo catalog: [llms.txt](llms.txt)
- Profile: [https://apify.com/taroyamada](https://apify.com/taroyamada)

How to run:

1. Call the Actor with the Store ID and the JSON object below as `input`.
2. Keep `delivery` `dataset` when the schema includes it. Leave report/export flags false on the first paid run.
3. Fetch rows from `defaultDatasetId` (`get-dataset-items` / Get Dataset Items). Confirm live Store pricing before a paid run. This page does not invent metrics.

Paste-ready copies also live in [`inputs/`](https://github.com/luxslime/apify-paid-report-starter-kits/tree/master/inputs) and [`integrations/`](../integrations/README.md).

## Featured kits

### APS — Apify Store Ranking Scraper

- Store ID: `taroyamada/apify-store-ranking-radar`
- Store: [https://apify.com/taroyamada/apify-store-ranking-radar](https://apify.com/taroyamada/apify-store-ranking-radar)
- File: [inputs/apify-store-ranking-radar.json](https://github.com/luxslime/apify-paid-report-starter-kits/blob/master/inputs/apify-store-ranking-radar.json)

```json
{
  "searches": [
    "instagram"
  ],
  "maxResultsPerSearch": 5,
  "dryRun": false
}
```

### Article — Article Extractor & Reader Scraper (News, Blog, RAG)

- Store ID: `taroyamada/article-content-extractor`
- Store: [https://apify.com/taroyamada/article-content-extractor](https://apify.com/taroyamada/article-content-extractor)
- File: [inputs/article-content-extractor.json](https://github.com/luxslime/apify-paid-report-starter-kits/blob/master/inputs/article-content-extractor.json)

```json
{
  "urls": [
    "https://en.wikipedia.org/wiki/Web_scraping"
  ],
  "outputFormat": "markdown",
  "includeImages": true,
  "concurrency": 5,
  "delivery": "dataset",
  "generateReport": false,
  "emitExport": false,
  "dryRun": false
}
```

### G2 — G2 & Capterra Review Scraper

- Store ID: `taroyamada/g2-capterra-review-intelligence`
- Store: [https://apify.com/taroyamada/g2-capterra-review-intelligence](https://apify.com/taroyamada/g2-capterra-review-intelligence)
- File: [inputs/g2-capterra-review-intelligence.json](https://github.com/luxslime/apify-paid-report-starter-kits/blob/master/inputs/g2-capterra-review-intelligence.json)

```json
{
  "reviewPageUrls": [
    "https://www.g2.com/products/notion/reviews"
  ],
  "reviewLimit": 1,
  "delivery": "dataset",
  "dryRun": false
}
```

### Procurement / TED-SAM — TED, SAM.gov & Grants Bid Alerts Scraper

- Store ID: `taroyamada/procurement-intel-actor`
- Store: [https://apify.com/taroyamada/procurement-intel-actor](https://apify.com/taroyamada/procurement-intel-actor)
- File: [inputs/procurement-intel-actor.json](https://github.com/luxslime/apify-paid-report-starter-kits/blob/master/inputs/procurement-intel-actor.json)

TED-only first paid run (`jurisdictions` `eu`).

```json
{
  "jurisdictions": "eu",
  "keywords": "cloud,cybersecurity,IT services",
  "cpvCodes": "72000000,72220000",
  "daysAhead": 21,
  "maxItemsPerSource": 40,
  "minValue": 100000,
  "delivery": "dataset",
  "generateReport": false,
  "emitExport": false,
  "dryRun": false
}
```

## Paid report starters

The seven deployment Actors use a free static sample (`sample` path: `dryRun` true, `maxChargeUsd` 0; not live data) and a separate paid preview (`preview-inputs/`, `dryRun` false, `maxChargeUsd` 0.25). PubMed Literature Watch uses a paid sample. JSON below is the **first paid** preview (or the PubMed sample, which is already a paid monitor run). Full-report files stay in `report-inputs/` and remain opt-in.

### Technical SEO & AI Crawler Audit

- Store ID: `taroyamada/technical-seo-portfolio-regression-report`
- Store: [https://apify.com/taroyamada/technical-seo-portfolio-regression-report](https://apify.com/taroyamada/technical-seo-portfolio-regression-report)
- Files: [sample](https://github.com/luxslime/apify-paid-report-starter-kits/blob/master/inputs/technical-seo-portfolio-regression-report.json) / [paid preview](https://github.com/luxslime/apify-paid-report-starter-kits/blob/master/preview-inputs/technical-seo-portfolio-regression-report.json)

```json
{
  "urls": [
    "https://example.com/"
  ],
  "aiCrawlerUserAgents": [
    "GPTBot",
    "ClaudeBot"
  ],
  "maxPages": 3,
  "checkRobotsTxt": true,
  "checkLlmsTxt": true,
  "authorizedUseConfirmed": false,
  "emitPageRows": false,
  "emitRawRows": false,
  "generateReport": false,
  "emitExport": false,
  "emitUnchanged": false,
  "initialRunMode": "baseline_only",
  "maxChargeUsd": 0.25,
  "dryRun": false
}
```

### Apple Podcasts Category Benchmark

- Store ID: `taroyamada/podcast-category-network-benchmark-report`
- Store: [https://apify.com/taroyamada/podcast-category-network-benchmark-report](https://apify.com/taroyamada/podcast-category-network-benchmark-report)
- Files: [sample](https://github.com/luxslime/apify-paid-report-starter-kits/blob/master/inputs/podcast-category-network-benchmark-report.json) / [paid preview](https://github.com/luxslime/apify-paid-report-starter-kits/blob/master/preview-inputs/podcast-category-network-benchmark-report.json)

```json
{
  "rssFeedUrls": [
    "https://feeds.npr.org/510289/podcast.xml"
  ],
  "showUrls": [],
  "searchTerms": [],
  "targetKeywords": [
    "economics",
    "business",
    "money"
  ],
  "maxEpisodesPerFeed": 3,
  "initialRunMode": "emit_backfill",
  "monitorKey": "starter-podcast-category-benchmark",
  "generateReport": false,
  "emitRawRows": true,
  "emitShortlistExport": false,
  "emitUnchanged": false,
  "maxChargeUsd": 0.25,
  "dryRun": false
}
```

### Clinical Trials & PubMed Evidence Gap Report

- Store ID: `taroyamada/biomedical-trial-literature-evidence-report`
- Store: [https://apify.com/taroyamada/biomedical-trial-literature-evidence-report](https://apify.com/taroyamada/biomedical-trial-literature-evidence-report)
- Files: [sample](https://github.com/luxslime/apify-paid-report-starter-kits/blob/master/inputs/biomedical-trial-literature-evidence-report.json) / [paid preview](https://github.com/luxslime/apify-paid-report-starter-kits/blob/master/preview-inputs/biomedical-trial-literature-evidence-report.json)

```json
{
  "searchTerms": [],
  "watchlists": [
    {
      "id": "starter-study",
      "nctIds": [
        "NCT04280705"
      ],
      "maxStudies": 1
    }
  ],
  "fromDate": "2025",
  "sort": "most_recent",
  "maxResultsPerQuery": 1,
  "maxArticles": 1,
  "maxStudiesPerWatchlist": 1,
  "maxPagesPerWatchlist": 1,
  "runMode": "monitor",
  "monitorKey": "starter-nct04280705-v2",
  "initialRunMode": "emit_backfill",
  "emitRawRows": true,
  "generateReport": false,
  "generateExport": false,
  "emitUnchanged": false,
  "maxChargeUsd": 0.25,
  "dryRun": false
}
```

### App Store Release & Review Benchmark

- Store ID: `taroyamada/app-release-category-review-benchmark-report`
- Store: [https://apify.com/taroyamada/app-release-category-review-benchmark-report](https://apify.com/taroyamada/app-release-category-review-benchmark-report)
- Files: [sample](https://github.com/luxslime/apify-paid-report-starter-kits/blob/master/inputs/app-release-category-review-benchmark-report.json) / [paid preview](https://github.com/luxslime/apify-paid-report-starter-kits/blob/master/preview-inputs/app-release-category-review-benchmark-report.json)

```json
{
  "appleAppIds": [
    "284882215"
  ],
  "appleCountries": [
    "us"
  ],
  "googlePlayIds": [],
  "reviewLimit": 5,
  "lookbackDays": 60,
  "releaseWindowDays": 21,
  "runMode": "monitor",
  "initialRunMode": "emit_backfill",
  "monitorKey": "starter-app-release-benchmark",
  "emitRawReviews": false,
  "emitRawRows": true,
  "generateReport": false,
  "generateExport": false,
  "emitUnchanged": false,
  "maxChargeUsd": 0.25,
  "dryRun": false
}
```

### npm & PyPI Dependency Risk Report

- Store ID: `taroyamada/package-portfolio-upgrade-risk-report`
- Store: [https://apify.com/taroyamada/package-portfolio-upgrade-risk-report](https://apify.com/taroyamada/package-portfolio-upgrade-risk-report)
- Files: [sample](https://github.com/luxslime/apify-paid-report-starter-kits/blob/master/inputs/package-portfolio-upgrade-risk-report.json) / [paid preview](https://github.com/luxslime/apify-paid-report-starter-kits/blob/master/preview-inputs/package-portfolio-upgrade-risk-report.json)

```json
{
  "packages": [
    {
      "name": "lodash",
      "ecosystem": "npm",
      "version": "4.17.20"
    }
  ],
  "includeGitHub": false,
  "monitorKey": "starter-package-upgrade-risk",
  "initialRunMode": "emit_backfill",
  "generateReport": false,
  "emitRawRows": true,
  "emitUnchanged": false,
  "emitExport": false,
  "maxChargeUsd": 0.25,
  "dryRun": false
}
```

### CPSC & NHTSA Recall Portfolio Watch

- Store ID: `taroyamada/product-safety-market-action-portfolio-report`
- Store: [https://apify.com/taroyamada/product-safety-market-action-portfolio-report](https://apify.com/taroyamada/product-safety-market-action-portfolio-report)
- Files: [sample](https://github.com/luxslime/apify-paid-report-starter-kits/blob/master/inputs/product-safety-market-action-portfolio-report.json) / [paid preview](https://github.com/luxslime/apify-paid-report-starter-kits/blob/master/preview-inputs/product-safety-market-action-portfolio-report.json)

```json
{
  "watchlists": [
    {
      "id": "battery-recalls",
      "agency": "CPSC",
      "productNames": [
        "battery"
      ],
      "lookbackDays": 30
    }
  ],
  "monitorKey": "starter-battery-recalls",
  "initialRunMode": "emit_backfill",
  "generateReport": false,
  "emitRawRows": true,
  "emitUnchanged": false,
  "emitExport": false,
  "maxChangedRecords": 1,
  "maxChargeUsd": 0.25,
  "dryRun": false
}
```

### eCFR & Federal Register Change Report

- Store ID: `taroyamada/regulatory-obligation-change-impact-report`
- Store: [https://apify.com/taroyamada/regulatory-obligation-change-impact-report](https://apify.com/taroyamada/regulatory-obligation-change-impact-report)
- Files: [sample](https://github.com/luxslime/apify-paid-report-starter-kits/blob/master/inputs/regulatory-obligation-change-impact-report.json) / [paid preview](https://github.com/luxslime/apify-paid-report-starter-kits/blob/master/preview-inputs/regulatory-obligation-change-impact-report.json)

```json
{
  "watchlists": [
    {
      "id": "benzene-exposure",
      "cfrTitle": 29,
      "part": "1910",
      "keywords": [
        "benzene"
      ],
      "federalRegisterTerms": [
        "benzene"
      ]
    }
  ],
  "monitorKey": "starter-benzene-exposure",
  "initialRunMode": "emit_backfill",
  "generateReport": false,
  "emitRawRows": true,
  "emitUnchanged": false,
  "emitExport": false,
  "maxFederalRegisterDocuments": 1,
  "lookbackDays": 30,
  "maxChargeUsd": 0.25,
  "dryRun": false
}
```

### PubMed Literature Watch & Research Report

- Store ID: `taroyamada/pubmed-research-intelligence`
- Store: [https://apify.com/taroyamada/pubmed-research-intelligence](https://apify.com/taroyamada/pubmed-research-intelligence)
- Files: [sample](https://github.com/luxslime/apify-paid-report-starter-kits/blob/master/inputs/pubmed-research-intelligence.json) / [paid preview](https://github.com/luxslime/apify-paid-report-starter-kits/blob/master/preview-inputs/pubmed-research-intelligence.json)

```json
{
  "searchTerms": [
    "CRISPR sickle cell"
  ],
  "pmids": [],
  "sort": "most_recent",
  "maxResultsPerQuery": 1,
  "maxArticles": 1,
  "runMode": "monitor",
  "monitorKey": "starter-pubmed-crispr-sickle-cell-v1",
  "initialRunMode": "emit_backfill",
  "emitRawRows": false,
  "generateReport": false,
  "generateExport": false,
  "maxChargeUsd": 0.25,
  "dryRun": false
}
```

## Other kits in this repo

### Apple Podcasts / iTunes Scraper

- Store ID: `taroyamada/apple-podcast-scraper`
- Store: [https://apify.com/taroyamada/apple-podcast-scraper](https://apify.com/taroyamada/apple-podcast-scraper)

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

### Apple Podcasts Chart Scraper

- Store ID: `taroyamada/apple-podcast-chart-tracker`
- Store: [https://apify.com/taroyamada/apple-podcast-chart-tracker](https://apify.com/taroyamada/apple-podcast-chart-tracker)

```json
{
  "countries": [
    "us"
  ],
  "limit": 3,
  "generateMovementReport": false,
  "dryRun": false
}
```

### Apple Podcasts Reviews Scraper

- Store ID: `taroyamada/apple-podcast-reviews-monitor`
- Store: [https://apify.com/taroyamada/apple-podcast-reviews-monitor](https://apify.com/taroyamada/apple-podcast-reviews-monitor)

```json
{
  "mode": "snapshot",
  "podcastIds": [
    "1535809341"
  ],
  "countries": [
    "us"
  ],
  "maxPagesPerPair": 1,
  "generateReport": false,
  "dryRun": false
}
```

### Website Content Extractor

- Store ID: `taroyamada/website-content-extractor`
- Store: [https://apify.com/taroyamada/website-content-extractor](https://apify.com/taroyamada/website-content-extractor)

```json
{
  "urls": [
    "https://docs.apify.com/platform/actors"
  ],
  "outputFormat": "markdown",
  "includeMetadata": true,
  "concurrency": 5,
  "delivery": "dataset",
  "dryRun": false
}
```

### YouTube Transcript Scraper

- Store ID: `taroyamada/youtube-transcript-bulk-api`
- Store: [https://apify.com/taroyamada/youtube-transcript-bulk-api](https://apify.com/taroyamada/youtube-transcript-bulk-api)

```json
{
  "videoUrls": [
    "https://www.youtube.com/watch?v=jNQXAC9IVRw"
  ],
  "language": "en",
  "includeAutoGenerated": true,
  "outputFormat": "json",
  "maxVideos": 1,
  "delivery": "dataset",
  "dryRun": false
}
```

### RSS & Atom Feed Extractor

- Store ID: `taroyamada/rss-feed-aggregator`
- Store: [https://apify.com/taroyamada/rss-feed-aggregator](https://apify.com/taroyamada/rss-feed-aggregator)

```json
{
  "feedUrls": [
    "https://blog.google/rss/"
  ],
  "maxItemsPerFeed": 5,
  "deduplicate": true,
  "delivery": "dataset",
  "dryRun": false
}
```

### Google News Scraper & RSS URL Extractor

- Store ID: `taroyamada/google-news-scraper`
- Store: [https://apify.com/taroyamada/google-news-scraper](https://apify.com/taroyamada/google-news-scraper)

```json
{
  "queries": [
    "artificial intelligence"
  ],
  "language": "en",
  "country": "US",
  "maxItems": 10,
  "deduplicate": true,
  "delivery": "dataset",
  "dryRun": false
}
```

### Wayback Machine Bulk Checker

- Store ID: `taroyamada/wayback-machine-checker`
- Store: [https://apify.com/taroyamada/wayback-machine-checker](https://apify.com/taroyamada/wayback-machine-checker)

```json
{
  "urls": [
    "https://example.com"
  ],
  "concurrency": 3,
  "delivery": "dataset",
  "dryRun": false
}
```

### Shopify App Store Review Scraper

- Store ID: `taroyamada/shopify-app-store-review-intelligence`
- Store: [https://apify.com/taroyamada/shopify-app-store-review-intelligence](https://apify.com/taroyamada/shopify-app-store-review-intelligence)

```json
{
  "appUrls": [
    "https://apps.shopify.com/omnisend"
  ],
  "reviewLimit": 5,
  "delivery": "dataset",
  "dryRun": false
}
```

### Bulk Phone Format Validator

- Store ID: `taroyamada/phone-number-validator`
- Store: [https://apify.com/taroyamada/phone-number-validator](https://apify.com/taroyamada/phone-number-validator)

```json
{
  "numbers": [
    "+14155552671"
  ],
  "defaultCountry": "US",
  "delivery": "dataset",
  "dryRun": false
}
```

### Chrome Web Store Extension Intelligence

- Store ID: `taroyamada/chrome-web-store-extension-intelligence`
- Store: [https://apify.com/taroyamada/chrome-web-store-extension-intelligence](https://apify.com/taroyamada/chrome-web-store-extension-intelligence)

```json
{
  "extensionUrls": [
    "https://chromewebstore.google.com/detail/google-translate/aapbdbdomjkkjkaonfhkkikfgjllcleb"
  ],
  "delivery": "dataset",
  "dryRun": false
}
```

### Bulk URL Status Checker

- Store ID: `taroyamada/bulk-url-health-checker`
- Store: [https://apify.com/taroyamada/bulk-url-health-checker](https://apify.com/taroyamada/bulk-url-health-checker)

```json
{
  "urls": [
    "https://example.com"
  ],
  "concurrency": 5,
  "followRedirects": true,
  "delivery": "dataset",
  "dryRun": false
}
```

### DMARC & Email Security Checker

- Store ID: `taroyamada/dns-dmarc-security-checker`
- Store: [https://apify.com/taroyamada/dns-dmarc-security-checker](https://apify.com/taroyamada/dns-dmarc-security-checker)

```json
{
  "domains": [
    "google.com"
  ],
  "checkDkim": false,
  "concurrency": 3,
  "delivery": "dataset",
  "dryRun": false
}
```

### HHS Healthcare Data Breach Change Scraper

- Store ID: `taroyamada/data-breach-disclosure-monitor`
- Store: [https://apify.com/taroyamada/data-breach-disclosure-monitor](https://apify.com/taroyamada/data-breach-disclosure-monitor)

```json
{
  "lookbackDays": 30,
  "maxBreachesInEvidence": 10,
  "delivery": "dataset",
  "dryRun": false
}
```

### Tech Events & CFP Calendar Scraper

- Store ID: `taroyamada/tech-events-intelligence`
- Store: [https://apify.com/taroyamada/tech-events-intelligence](https://apify.com/taroyamada/tech-events-intelligence)

```json
{
  "topics": [
    "kubernetes"
  ],
  "year": 2026,
  "delivery": "dataset",
  "dryRun": false
}
```

### Bulk Email Syntax & MX Validator

- Store ID: `taroyamada/email-deliverability-checker`
- Store: [https://apify.com/taroyamada/email-deliverability-checker](https://apify.com/taroyamada/email-deliverability-checker)

```json
{
  "emails": [
    "test@gmail.com"
  ],
  "checkMx": true,
  "checkDisposable": true,
  "delivery": "dataset",
  "dryRun": false
}
```

### Structured Data Scraper & Validator

- Store ID: `taroyamada/structured-data-validator`
- Store: [https://apify.com/taroyamada/structured-data-validator](https://apify.com/taroyamada/structured-data-validator)

```json
{
  "urls": [
    "https://schema.org/docs/gs.html"
  ],
  "concurrency": 3,
  "delivery": "dataset",
  "dryRun": false
}
```

### Sitemap Scraper & Analyzer

- Store ID: `taroyamada/sitemap-analyzer`
- Store: [https://apify.com/taroyamada/sitemap-analyzer](https://apify.com/taroyamada/sitemap-analyzer)

```json
{
  "sitemapUrls": [
    "https://apify.com/sitemap.xml"
  ],
  "maxUrls": 50,
  "checkStatus": false,
  "delivery": "dataset",
  "dryRun": false
}
```

### SSL/TLS Certificate Scraper

- Store ID: `taroyamada/ssl-certificate-monitor`
- Store: [https://apify.com/taroyamada/ssl-certificate-monitor](https://apify.com/taroyamada/ssl-certificate-monitor)

```json
{
  "domains": [
    "apify.com"
  ],
  "expiryWarningDays": 30,
  "emitUnchanged": false,
  "delivery": "dataset",
  "dryRun": false
}
```

### Trade Show Exhibitor Intelligence

- Store ID: `taroyamada/trade-show-exhibitor-intelligence`
- Store: [https://apify.com/taroyamada/trade-show-exhibitor-intelligence](https://apify.com/taroyamada/trade-show-exhibitor-intelligence)

```json
{
  "urls": [
    "https://www.ces.tech/exhibitors/"
  ],
  "maxResults": 10,
  "dryRun": false
}
```

### Google Maps Lead Enrichment Scraper

- Store ID: `taroyamada/google-maps-lead-enrichment`
- Store: [https://apify.com/taroyamada/google-maps-lead-enrichment](https://apify.com/taroyamada/google-maps-lead-enrichment)

```json
{
  "leads": [
    {
      "businessName": "Example Cafe",
      "address": "1 Market St, San Francisco, CA",
      "website": "https://example.com"
    }
  ],
  "includeContacts": true,
  "maxLeads": 1,
  "delivery": "dataset",
  "dryRun": false
}
```

### Google Maps Review Scraper

- Store ID: `taroyamada/google-maps-review-intelligence`
- Store: [https://apify.com/taroyamada/google-maps-review-intelligence](https://apify.com/taroyamada/google-maps-review-intelligence)

```json
{
  "placeUrls": [
    "https://www.google.com/maps/place/Tokyo+Station/"
  ],
  "reviewLimit": 5,
  "delivery": "dataset",
  "dryRun": false
}
```

### robots.txt Parser & AI Crawler Block Checker

- Store ID: `taroyamada/robotstxt-ai-checker`
- Store: [https://apify.com/taroyamada/robotstxt-ai-checker](https://apify.com/taroyamada/robotstxt-ai-checker)

```json
{
  "domains": [
    "openai.com"
  ],
  "datasetMode": "all",
  "concurrency": 3,
  "dryRun": false
}
```

### AI Brand Visibility Scraper

- Store ID: `taroyamada/ai-visibility-monitor-actor`
- Store: [https://apify.com/taroyamada/ai-visibility-monitor-actor](https://apify.com/taroyamada/ai-visibility-monitor-actor)

```json
{
  "brand": "Apify",
  "brandTerms": [
    "apify.com",
    "apify"
  ],
  "keywords": [
    "web scraping platform"
  ],
  "searchSources": [
    "google"
  ],
  "maxResultsPerKeyword": 5,
  "datasetMode": "all",
  "delivery": "dataset",
  "dryRun": false
}
```
