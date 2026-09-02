# Apify Paid Report Starter Kits

Free sample, paid preview, and full-report inputs for 8 public-data and authorized-site Apify Actors.

The seven deployment actors expose a source-linked static sample with `sample=true`, `dryRun=true`, and `maxChargeUsd=0`; the sample is not live data. Each has a separate paid preview with `dryRun=false` and `maxChargeUsd=0.25`. Full reports remain opt-in and use the prices shown on each Actor's live Apify Store page.

[Download the stable v1.0.0 starter-kit release](https://github.com/luxslime/apify-paid-report-starter-kits/releases/tag/v1.0.0).

| Actor | Sample | Sample cap | Paid preview cap | Inputs |
| --- | --- | ---: | ---: | --- |
| [Technical SEO & AI Crawler Audit](https://apify.com/taroyamada/technical-seo-portfolio-regression-report?utm_source=github_pages&utm_medium=starter_catalog&utm_campaign=phase10_paid_reports&utm_content=technical-seo-portfolio-regression-report__github_readme) | Free static sample (not live data) | $0.00 | $0.25 | [sample](inputs/technical-seo-portfolio-regression-report.json) / [paid preview](preview-inputs/technical-seo-portfolio-regression-report.json) / [full report](report-inputs/technical-seo-portfolio-regression-report.json) |
| [Apple Podcasts Category Benchmark](https://apify.com/taroyamada/podcast-category-network-benchmark-report?utm_source=github_pages&utm_medium=starter_catalog&utm_campaign=phase10_paid_reports&utm_content=podcast-category-network-benchmark-report__github_readme) | Free static sample (not live data) | $0.00 | $0.25 | [sample](inputs/podcast-category-network-benchmark-report.json) / [paid preview](preview-inputs/podcast-category-network-benchmark-report.json) / [full report](report-inputs/podcast-category-network-benchmark-report.json) |
| [Clinical Trials & PubMed Evidence Gap Report](https://apify.com/taroyamada/biomedical-trial-literature-evidence-report?utm_source=github_pages&utm_medium=starter_catalog&utm_campaign=phase10_paid_reports&utm_content=biomedical-trial-literature-evidence-report__github_readme) | Free static sample (not live data) | $0.00 | $0.25 | [sample](inputs/biomedical-trial-literature-evidence-report.json) / [paid preview](preview-inputs/biomedical-trial-literature-evidence-report.json) / [full report](report-inputs/biomedical-trial-literature-evidence-report.json) |
| [App Store Release & Review Benchmark](https://apify.com/taroyamada/app-release-category-review-benchmark-report?utm_source=github_pages&utm_medium=starter_catalog&utm_campaign=phase10_paid_reports&utm_content=app-release-category-review-benchmark-report__github_readme) | Free static sample (not live data) | $0.00 | $0.25 | [sample](inputs/app-release-category-review-benchmark-report.json) / [paid preview](preview-inputs/app-release-category-review-benchmark-report.json) / [full report](report-inputs/app-release-category-review-benchmark-report.json) |
| [npm & PyPI Dependency Risk Report](https://apify.com/taroyamada/package-portfolio-upgrade-risk-report?utm_source=github_pages&utm_medium=starter_catalog&utm_campaign=phase10_paid_reports&utm_content=package-portfolio-upgrade-risk-report__github_readme) | Free static sample (not live data) | $0.00 | $0.25 | [sample](inputs/package-portfolio-upgrade-risk-report.json) / [paid preview](preview-inputs/package-portfolio-upgrade-risk-report.json) / [full report](report-inputs/package-portfolio-upgrade-risk-report.json) |
| [CPSC & NHTSA Recall Portfolio Watch](https://apify.com/taroyamada/product-safety-market-action-portfolio-report?utm_source=github_pages&utm_medium=starter_catalog&utm_campaign=phase10_paid_reports&utm_content=product-safety-market-action-portfolio-report__github_readme) | Free static sample (not live data) | $0.00 | $0.25 | [sample](inputs/product-safety-market-action-portfolio-report.json) / [paid preview](preview-inputs/product-safety-market-action-portfolio-report.json) / [full report](report-inputs/product-safety-market-action-portfolio-report.json) |
| [eCFR & Federal Register Change Report](https://apify.com/taroyamada/regulatory-obligation-change-impact-report?utm_source=github_pages&utm_medium=starter_catalog&utm_campaign=phase10_paid_reports&utm_content=regulatory-obligation-change-impact-report__github_readme) | Free static sample (not live data) | $0.00 | $0.25 | [sample](inputs/regulatory-obligation-change-impact-report.json) / [paid preview](preview-inputs/regulatory-obligation-change-impact-report.json) / [full report](report-inputs/regulatory-obligation-change-impact-report.json) |
| [PubMed Literature Watch & Research Report](https://apify.com/taroyamada/pubmed-research-intelligence?utm_source=github_pages&utm_medium=starter_catalog&utm_campaign=phase10_paid_reports&utm_content=pubmed-research-intelligence__github_readme) | `new-publication-alert` | $0.25 | $0.25 | [sample](inputs/pubmed-research-intelligence.json) / [paid preview](preview-inputs/pubmed-research-intelligence.json) / [full report](report-inputs/pubmed-research-intelligence.json) |

## Related Apify Actors / Guides

- [Apple Podcasts / iTunes Scraper: Search, Charts, Episodes](https://apify.com/taroyamada/apple-podcast-scraper) — cheapest first paid run: small search, `includeEpisodes` false ([starter JSON](inputs/apple-podcast-scraper.json)). Live Store PPE: Result $2.50/1,000, Start $0.005. [discovery page](docs/apple-podcasts-scraper/index.html) — [Apple Podcasts scraper Apify notes (RSS vs Store)](docs/guides/apple-podcasts-scraper-apify.md) — [HTML tools docs](docs/tools/apple-podcasts-scraper/) ([search](docs/tools/apple-podcasts-scraper/search.html), [charts](docs/tools/apple-podcasts-scraper/charts.html), [watchlists](docs/tools/apple-podcasts-scraper/watchlists.html), [webhooks](docs/tools/apple-podcasts-scraper/webhooks.html), [dataset fields](docs/tools/apple-podcasts-scraper/dataset-fields.html))
- [Article Extractor & Reader Scraper (News, Blog, RAG)](https://apify.com/taroyamada/article-content-extractor) — cheapest first paid run: one public article URL, `generateReport` false, `emitExport` false ([starter JSON](inputs/article-content-extractor.json)). Live Store PPE: Actor Start $0.00005, Useful article row $0.008.
- [G2 & Capterra Review Scraper](https://apify.com/taroyamada/g2-capterra-review-intelligence) — cheapest first paid run: one review page URL, modest `reviewLimit` (25), `dryRun` false ([starter JSON](inputs/g2-capterra-review-intelligence.json)). Live Store PPE: Actor Start $0.001, result $0.01.
- [Apple Podcasts Chart Scraper](https://apify.com/taroyamada/apple-podcast-chart-tracker) — cheapest first paid run: one US storefront, chart depth 3, `generateMovementReport` false ([starter JSON](inputs/apple-podcast-chart-tracker.json)). Live Store PPE: apify-default-dataset-item $0.003.
- [Apple Podcasts Reviews Scraper](https://apify.com/taroyamada/apple-podcast-reviews-monitor) — cheapest first paid run: snapshot mode, one podcast ID, one country, `maxPagesPerPair` 1, `generateReport` false ([starter JSON](inputs/apple-podcast-reviews-monitor.json)). Live Store PPE: apify-default-dataset-item $0.003.
- [TED, SAM.gov & Grants Bid Alerts Scraper](https://apify.com/taroyamada/procurement-intel-actor) — cheapest first paid run: TED-only (`jurisdictions` eu), `generateReport` false, `emitExport` false ([starter JSON](inputs/procurement-intel-actor.json)). Live Store PPE: Procurement opportunity or alert row $0.008.
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
- The related [G2 & Capterra Review Scraper](https://apify.com/taroyamada/g2-capterra-review-intelligence) uses live Store PPE Actor Start $0.001 and result $0.01. Its cheapest first paid run is [inputs/g2-capterra-review-intelligence.json](inputs/g2-capterra-review-intelligence.json) (one review page URL; one result row ≈ $0.011 before scaling URLs or review depth).
- The related [Apple Podcasts Chart Scraper](https://apify.com/taroyamada/apple-podcast-chart-tracker) uses live Store PPE apify-default-dataset-item $0.003. Its cheapest first paid run is [inputs/apple-podcast-chart-tracker.json](inputs/apple-podcast-chart-tracker.json) (legacy raw chart rows only; `generateMovementReport` false).
- The related [Apple Podcasts Reviews Scraper](https://apify.com/taroyamada/apple-podcast-reviews-monitor) uses live Store PPE apify-default-dataset-item $0.003. Its cheapest first paid run is [inputs/apple-podcast-reviews-monitor.json](inputs/apple-podcast-reviews-monitor.json) (snapshot mode; `generateReport` false).
- The related [TED, SAM.gov & Grants Bid Alerts Scraper](https://apify.com/taroyamada/procurement-intel-actor) uses live Store PPE Procurement opportunity or alert row $0.008. Its cheapest first paid run is [inputs/procurement-intel-actor.json](inputs/procurement-intel-actor.json) (TED-only; `generateReport` and `emitExport` false).
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
