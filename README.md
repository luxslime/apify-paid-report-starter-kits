# Apify Paid Report Starter Kits

Free sample, paid preview, and full-report inputs for 8 public-data and authorized-site Apify Actors.

The seven deployment actors expose a source-linked static sample with `sample=true`, `dryRun=true`, and `maxChargeUsd=0`; the sample is not live data. Each has a separate paid preview with `dryRun=false` and `maxChargeUsd=0.25`. Full reports remain opt-in and use the prices shown on each Actor's live Apify Store page.

Publisher catalog (no prices): [https://apify.momiji-space.com/llms.txt](https://apify.momiji-space.com/llms.txt). This repo: [docs/llms.txt](docs/llms.txt). MCP / agent Store IDs and minimal Input JSON: [docs/mcp-agents.md](docs/mcp-agents.md). Profile: [https://apify.com/taroyamada](https://apify.com/taroyamada).

[Download the stable v1.0.0 starter-kit release](https://github.com/luxslime/apify-paid-report-starter-kits/releases/tag/v1.0.0).

| Actor | Store ID | Sample | Sample cap | Paid preview cap | Inputs |
| --- | --- | --- | ---: | ---: | --- |
| [Technical SEO & AI Crawler Audit](https://apify.com/taroyamada/technical-seo-portfolio-regression-report?utm_source=github_pages&utm_medium=starter_catalog&utm_campaign=phase10_paid_reports&utm_content=technical-seo-portfolio-regression-report__github_readme) | `taroyamada/technical-seo-portfolio-regression-report` | Free static sample (not live data) | $0.00 | $0.25 | [sample](inputs/technical-seo-portfolio-regression-report.json) / [paid preview](preview-inputs/technical-seo-portfolio-regression-report.json) / [full report](report-inputs/technical-seo-portfolio-regression-report.json) |
| [Apple Podcasts Category Benchmark](https://apify.com/taroyamada/podcast-category-network-benchmark-report?utm_source=github_pages&utm_medium=starter_catalog&utm_campaign=phase10_paid_reports&utm_content=podcast-category-network-benchmark-report__github_readme) | `taroyamada/podcast-category-network-benchmark-report` | Free static sample (not live data) | $0.00 | $0.25 | [sample](inputs/podcast-category-network-benchmark-report.json) / [paid preview](preview-inputs/podcast-category-network-benchmark-report.json) / [full report](report-inputs/podcast-category-network-benchmark-report.json) |
| [Clinical Trials & PubMed Evidence Gap Report](https://apify.com/taroyamada/biomedical-trial-literature-evidence-report?utm_source=github_pages&utm_medium=starter_catalog&utm_campaign=phase10_paid_reports&utm_content=biomedical-trial-literature-evidence-report__github_readme) | `taroyamada/biomedical-trial-literature-evidence-report` | Free static sample (not live data) | $0.00 | $0.25 | [sample](inputs/biomedical-trial-literature-evidence-report.json) / [paid preview](preview-inputs/biomedical-trial-literature-evidence-report.json) / [full report](report-inputs/biomedical-trial-literature-evidence-report.json) |
| [App Store Release & Review Benchmark](https://apify.com/taroyamada/app-release-category-review-benchmark-report?utm_source=github_pages&utm_medium=starter_catalog&utm_campaign=phase10_paid_reports&utm_content=app-release-category-review-benchmark-report__github_readme) | `taroyamada/app-release-category-review-benchmark-report` | Free static sample (not live data) | $0.00 | $0.25 | [sample](inputs/app-release-category-review-benchmark-report.json) / [paid preview](preview-inputs/app-release-category-review-benchmark-report.json) / [full report](report-inputs/app-release-category-review-benchmark-report.json) |
| [npm & PyPI Dependency Risk Report](https://apify.com/taroyamada/package-portfolio-upgrade-risk-report?utm_source=github_pages&utm_medium=starter_catalog&utm_campaign=phase10_paid_reports&utm_content=package-portfolio-upgrade-risk-report__github_readme) | `taroyamada/package-portfolio-upgrade-risk-report` | Free static sample (not live data) | $0.00 | $0.25 | [sample](inputs/package-portfolio-upgrade-risk-report.json) / [paid preview](preview-inputs/package-portfolio-upgrade-risk-report.json) / [full report](report-inputs/package-portfolio-upgrade-risk-report.json) |
| [CPSC & NHTSA Recall Portfolio Watch](https://apify.com/taroyamada/product-safety-market-action-portfolio-report?utm_source=github_pages&utm_medium=starter_catalog&utm_campaign=phase10_paid_reports&utm_content=product-safety-market-action-portfolio-report__github_readme) | `taroyamada/product-safety-market-action-portfolio-report` | Free static sample (not live data) | $0.00 | $0.25 | [sample](inputs/product-safety-market-action-portfolio-report.json) / [paid preview](preview-inputs/product-safety-market-action-portfolio-report.json) / [full report](report-inputs/product-safety-market-action-portfolio-report.json) |
| [eCFR & Federal Register Change Report](https://apify.com/taroyamada/regulatory-obligation-change-impact-report?utm_source=github_pages&utm_medium=starter_catalog&utm_campaign=phase10_paid_reports&utm_content=regulatory-obligation-change-impact-report__github_readme) | `taroyamada/regulatory-obligation-change-impact-report` | Free static sample (not live data) | $0.00 | $0.25 | [sample](inputs/regulatory-obligation-change-impact-report.json) / [paid preview](preview-inputs/regulatory-obligation-change-impact-report.json) / [full report](report-inputs/regulatory-obligation-change-impact-report.json) |
| [PubMed Literature Watch & Research Report](https://apify.com/taroyamada/pubmed-research-intelligence?utm_source=github_pages&utm_medium=starter_catalog&utm_campaign=phase10_paid_reports&utm_content=pubmed-research-intelligence__github_readme) | `taroyamada/pubmed-research-intelligence` | `new-publication-alert` | $0.25 | $0.25 | [sample](inputs/pubmed-research-intelligence.json) / [paid preview](preview-inputs/pubmed-research-intelligence.json) / [full report](report-inputs/pubmed-research-intelligence.json) |

## Run on Apify (priority)

Exact Store URLs + momiji landing pages. Paste the Input JSON into the Actor **Input** tab, then Start. No price changes in this repo.

### APS — Apple Podcasts / iTunes Scraper

Store ID: `taroyamada/apple-podcast-scraper`

- **Run on Apify:** [Open Store](https://apify.com/taroyamada/apple-podcast-scraper) · [Open Input](https://apify.com/taroyamada/apple-podcast-scraper/input)
- **Landing page:** [Apple Podcasts Scraper](https://apify.momiji-space.com/apple-podcasts-scraper/)
- **Starter JSON:** [inputs/apple-podcast-scraper.json](inputs/apple-podcast-scraper.json)

```json
{
  "searchTerm": "technology",
  "country": "us",
  "limit": 3,
  "includeEpisodes": false
}
```

### Article Content Extractor

Store ID: `taroyamada/article-content-extractor`

- **Run on Apify:** [Open Store](https://apify.com/taroyamada/article-content-extractor) · [Open Input](https://apify.com/taroyamada/article-content-extractor/input)
- **Landing page:** [Article Content Extractor](https://apify.momiji-space.com/article-content-extractor/)
- **Starter JSON:** [inputs/article-content-extractor.json](inputs/article-content-extractor.json)

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

### G2 & Capterra Review Scraper

Store ID: `taroyamada/g2-capterra-review-intelligence`

- **Run on Apify:** [Open Store](https://apify.com/taroyamada/g2-capterra-review-intelligence) · [Open Input](https://apify.com/taroyamada/g2-capterra-review-intelligence/input)
- **Landing page:** [G2 & Capterra Review Scraper](https://apify.momiji-space.com/g2-capterra-review-scraper/)
- **Starter JSON:** [inputs/g2-capterra-review-intelligence.json](inputs/g2-capterra-review-intelligence.json)

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

### TED / SAM.gov / Grants (procurement)

Store ID: `taroyamada/procurement-intel-actor`

- **Run on Apify:** [Open Store](https://apify.com/taroyamada/procurement-intel-actor) · [Open Input](https://apify.com/taroyamada/procurement-intel-actor/input)
- **Landing page:** [TED, SAM.gov & Grants Bid Alerts](https://apify.momiji-space.com/ted-sam-grants-bid-alerts/)
- **Starter JSON:** [inputs/procurement-intel-actor.json](inputs/procurement-intel-actor.json)

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

## MCP / agents (featured kits)

Pass the Store ID and this Input JSON. Keep `delivery` `dataset` when the schema includes it. Fetch rows from `defaultDatasetId`. Full catalog: [docs/mcp-agents.md](docs/mcp-agents.md).

**Apify Store Ranking** — Store ID `taroyamada/apify-store-ranking-radar` — [Store](https://apify.com/taroyamada/apify-store-ranking-radar)

```json
{
  "searches": [
    "instagram"
  ],
  "maxResultsPerSearch": 5,
  "dryRun": false
}
```

**Article** — Store ID `taroyamada/article-content-extractor` — [Store](https://apify.com/taroyamada/article-content-extractor)

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

**G2** — Store ID `taroyamada/g2-capterra-review-intelligence` — [Store](https://apify.com/taroyamada/g2-capterra-review-intelligence)

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

**Procurement / TED-SAM** — Store ID `taroyamada/procurement-intel-actor` — [Store](https://apify.com/taroyamada/procurement-intel-actor)

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

## Related Apify Actors / Guides

- [Apple Podcasts / iTunes Scraper: Search, Charts, Episodes](https://apify.com/taroyamada/apple-podcast-scraper) — Store ID `taroyamada/apple-podcast-scraper`. cheapest first paid run: small search, `includeEpisodes` false ([starter JSON](inputs/apple-podcast-scraper.json)). Live Store PPE: Result $2.50/1,000, Start $0.005. [discovery page](docs/apple-podcasts-scraper/index.html) — [Apple Podcasts scraper Apify notes (RSS vs Store)](docs/guides/apple-podcasts-scraper-apify.md) — [HTML tools docs](docs/tools/apple-podcasts-scraper/) ([search](docs/tools/apple-podcasts-scraper/search.html), [charts](docs/tools/apple-podcasts-scraper/charts.html), [watchlists](docs/tools/apple-podcasts-scraper/watchlists.html), [webhooks](docs/tools/apple-podcasts-scraper/webhooks.html), [dataset fields](docs/tools/apple-podcasts-scraper/dataset-fields.html))
- [Apify Store Ranking Scraper](https://apify.com/taroyamada/apify-store-ranking-radar) — Store ID `taroyamada/apify-store-ranking-radar`. cheapest first paid run: one search, `maxResultsPerSearch` 5, `dryRun` false ([starter JSON](inputs/apify-store-ranking-radar.json), [Make input](integrations/make/apify-store-ranking-radar.json), [n8n input](integrations/n8n/apify-store-ranking-radar.json)). Live Store PPE: Actor Start $0.00005, Result $0.001.
- [Article Extractor & Reader Scraper (News, Blog, RAG)](https://apify.com/taroyamada/article-content-extractor) — Store ID `taroyamada/article-content-extractor`. cheapest first paid run: one public article URL, `generateReport` false, `emitExport` false ([starter JSON](inputs/article-content-extractor.json), [Make input](integrations/make/article-content-extractor.json), [n8n input](integrations/n8n/article-content-extractor.json)). Live Store PPE: Actor Start $0.00005, Useful article row $0.008.
- [G2 & Capterra Review Scraper](https://apify.com/taroyamada/g2-capterra-review-intelligence) — Store ID `taroyamada/g2-capterra-review-intelligence`. cheapest first paid run: one review page URL, `reviewLimit` 1, `dryRun` false ([starter JSON](inputs/g2-capterra-review-intelligence.json), [Make input](integrations/make/g2-capterra-review-intelligence.json), [n8n input](integrations/n8n/g2-capterra-review-intelligence.json)). Live Store PPE: Actor Start $0.001, result $0.003.
- [Apple Podcasts Chart Scraper](https://apify.com/taroyamada/apple-podcast-chart-tracker) — Store ID `taroyamada/apple-podcast-chart-tracker`. cheapest first paid run: one US storefront, chart depth 3, `generateMovementReport` false ([starter JSON](inputs/apple-podcast-chart-tracker.json), [Make input](integrations/make/apple-podcast-chart-tracker.json), [n8n input](integrations/n8n/apple-podcast-chart-tracker.json)). Live Store PPE: apify-default-dataset-item $0.003.
- [Apple Podcasts Reviews Scraper](https://apify.com/taroyamada/apple-podcast-reviews-monitor) — Store ID `taroyamada/apple-podcast-reviews-monitor`. cheapest first paid run: snapshot mode, one podcast ID, one country, `maxPagesPerPair` 1, `generateReport` false ([starter JSON](inputs/apple-podcast-reviews-monitor.json), [Make input](integrations/make/apple-podcast-reviews-monitor.json), [n8n input](integrations/n8n/apple-podcast-reviews-monitor.json)). Live Store PPE: apify-default-dataset-item $0.003.
- [TED, SAM.gov & Grants Bid Alerts Scraper](https://apify.com/taroyamada/procurement-intel-actor) — Store ID `taroyamada/procurement-intel-actor`. cheapest first paid run: TED-only (`jurisdictions` eu), `generateReport` false, `emitExport` false ([starter JSON](inputs/procurement-intel-actor.json)). Live Store PPE: Procurement opportunity or alert row $0.008.
- [Make and n8n first paid runs](integrations/README.md) — paste-ready copies of the cheapest first paid inputs, including APS, Article, G2, Chart, Reviews, and procurement.
- [Apple Podcasts charts](docs/guides/apple-podcasts-charts.md)
- [Apple Podcasts watchlists](docs/guides/apple-podcasts-watchlists.md)
- [Apple Podcasts search and discovery](docs/guides/apple-podcasts-search-discovery.md)

## Use

1. Clone this repository and sign in with the [Apify CLI](https://docs.apify.com/cli).
2. Treat the checked-in sample output as illustrative, not current live data.
3. Replace sample watch terms or URLs with your own authorized scope.
4. Confirm the live Store pricing and run cap.
5. Run the free sample input, then the separate paid preview input.
6. Enable the report/export option only after the preview fits your workflow.

## Billing behavior

- No start charge is configured for these 8 Actors.
- The related [Apple Podcasts / iTunes Scraper](https://apify.com/taroyamada/apple-podcast-scraper) uses live Store PPE Result $2.50/1,000 and Start $0.005. Its cheapest first paid run is [inputs/apple-podcast-scraper.json](inputs/apple-podcast-scraper.json).
- The related [Article Extractor & Reader Scraper (News, Blog, RAG)](https://apify.com/taroyamada/article-content-extractor) uses live Store PPE Actor Start $0.00005 and Useful article row $0.008. Its cheapest first paid run is [inputs/article-content-extractor.json](inputs/article-content-extractor.json) (one URL; one useful row ≈ $0.00805 before optional report/export events).
- The related [G2 & Capterra Review Scraper](https://apify.com/taroyamada/g2-capterra-review-intelligence) uses live Store PPE Actor Start $0.001 and result $0.003. Its cheapest first paid run is [inputs/g2-capterra-review-intelligence.json](inputs/g2-capterra-review-intelligence.json) (one review page URL; one result row ≈ $0.004 before scaling URLs or review depth).
- The related [Apple Podcasts Chart Scraper](https://apify.com/taroyamada/apple-podcast-chart-tracker) uses live Store PPE apify-default-dataset-item $0.003. Its cheapest first paid run is [inputs/apple-podcast-chart-tracker.json](inputs/apple-podcast-chart-tracker.json) (legacy raw chart rows only; `generateMovementReport` false).
- The related [Apple Podcasts Reviews Scraper](https://apify.com/taroyamada/apple-podcast-reviews-monitor) uses live Store PPE apify-default-dataset-item $0.003. Its cheapest first paid run is [inputs/apple-podcast-reviews-monitor.json](inputs/apple-podcast-reviews-monitor.json) (snapshot mode; `generateReport` false).
- The related [TED, SAM.gov & Grants Bid Alerts Scraper](https://apify.com/taroyamada/procurement-intel-actor) uses live Store PPE Procurement opportunity or alert row $0.008. Its cheapest first paid run is [inputs/procurement-intel-actor.json](inputs/procurement-intel-actor.json) (TED-only; `generateReport` and `emitExport` false).
- The related [Apify Store Ranking Scraper](https://apify.com/taroyamada/apify-store-ranking-radar) uses live Store PPE Actor Start $0.00005 and Result $0.001. Its cheapest first paid run is [inputs/apify-store-ranking-radar.json](inputs/apify-store-ranking-radar.json) (one search; `maxResultsPerSearch` 5).
- Zero-row and unchanged monitor runs have zero event charge.
- `maxChargeUsd` is a hard buyer-controlled cap checked before delivery; deployment paid previews use $0.25.
- These starter inputs keep report and export events disabled.

## Data and use guardrails

- Technical SEO uses user-authorized public URLs only.
- Podcast examples use public Apple metadata and public RSS.
- Biomedical examples use official ClinicalTrials.gov and PubMed APIs.
- App examples use public store metadata and review samples.
- Package examples use official npm, PyPI, and OSV sources.
- Product safety examples use official CPSC and NHTSA public records.
- Regulatory examples use official eCFR and Federal Register public sources.

The outputs are source-linked research and workflow inputs, not legal, medical, investment, procurement, safety-certification, ranking, or business-outcome advice. No actor is affiliated with or endorsed by an upstream agency or platform.
