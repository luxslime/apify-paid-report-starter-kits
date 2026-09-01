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

## Related Apify Actors

- [Apple Podcasts Scraper: Search, Charts, Episodes & Watchlists](https://apify.com/taroyamada/apple-podcast-scraper) — [discovery page](docs/apple-podcasts-scraper/index.html) — [Apple Podcasts scraper Apify notes (RSS vs Store)](docs/guides/apple-podcasts-scraper-apify.md)

## Use

1. Clone this repository and sign in with the [Apify CLI](https://docs.apify.com/cli).
2. Treat the checked-in sample output as illustrative, not current live data.
3. Replace sample watch terms or URLs with your own authorized scope.
4. Confirm the live Store pricing and run cap.
5. Run the free sample input, then the separate paid preview input.
6. Enable the report/export option only after the preview fits your workflow.

## Billing behavior

- No start charge is configured for these 8 Actors.
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
