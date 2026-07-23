# Apify Paid Report Starter Kits

Small, capped inputs for testing seven public-data and authorized-site Apify Actors before enabling their full report events.

Six examples exercise the real public source and bill only delivered source and buyer-facing signal rows. The authorized-site SEO example remains a free safe demo until you confirm authorization and choose a paid output. Every input has `maxChargeUsd <= 1`. Full reports remain opt-in and use the prices shown on each Actor's live Apify Store page.

| Actor | Expected starter outcome | Expected charge | Run cap | Starter input |
| --- | --- | ---: | ---: | --- |
| [Technical SEO & AI Crawler Audit](https://apify.com/taroyamada/technical-seo-portfolio-regression-report?utm_source=github_pages&utm_medium=starter_catalog&utm_campaign=phase10_paid_reports&utm_content=technical-seo-portfolio-regression-report__github_readme) | Free authorization-safe demo | $0.000 | $0.00 | [starter](inputs/technical-seo-portfolio-regression-report.json) / [report](report-inputs/technical-seo-portfolio-regression-report.json) |
| [Apple Podcasts Category Benchmark](https://apify.com/taroyamada/podcast-category-network-benchmark-report?utm_source=github_pages&utm_medium=starter_catalog&utm_campaign=phase10_paid_reports&utm_content=podcast-category-network-benchmark-report__github_readme) | `podcast-show-benchmarked` + `podcast-network-signal` | $0.088 | $0.50 | [starter](inputs/podcast-category-network-benchmark-report.json) / [report](report-inputs/podcast-category-network-benchmark-report.json) |
| [Clinical Trials & PubMed Evidence Gap Report](https://apify.com/taroyamada/biomedical-trial-literature-evidence-report?utm_source=github_pages&utm_medium=starter_catalog&utm_campaign=phase10_paid_reports&utm_content=biomedical-trial-literature-evidence-report__github_readme) | `biomedical-evidence-row` + `evidence-gap-alert` | $0.158 | $0.50 | [starter](inputs/biomedical-trial-literature-evidence-report.json) / [report](report-inputs/biomedical-trial-literature-evidence-report.json) |
| [App Store Release & Review Benchmark](https://apify.com/taroyamada/app-release-category-review-benchmark-report?utm_source=github_pages&utm_medium=starter_catalog&utm_campaign=phase10_paid_reports&utm_content=app-release-category-review-benchmark-report__github_readme) | `app-benchmarked` + `app-review-regression` | $0.115 | $0.50 | [starter](inputs/app-release-category-review-benchmark-report.json) / [report](report-inputs/app-release-category-review-benchmark-report.json) |
| [npm & PyPI Dependency Risk Report](https://apify.com/taroyamada/package-portfolio-upgrade-risk-report?utm_source=github_pages&utm_medium=starter_catalog&utm_campaign=phase10_paid_reports&utm_content=package-portfolio-upgrade-risk-report__github_readme) | `package-risk-row` + `package-upgrade-risk-alert` | $0.260 | $0.50 | [starter](inputs/package-portfolio-upgrade-risk-report.json) / [report](report-inputs/package-portfolio-upgrade-risk-report.json) |
| [CPSC & NHTSA Recall Portfolio Watch](https://apify.com/taroyamada/product-safety-market-action-portfolio-report?utm_source=github_pages&utm_medium=starter_catalog&utm_campaign=phase10_paid_reports&utm_content=product-safety-market-action-portfolio-report__github_readme) | `safety-record-row` + `market-action-alert` | $0.206 | $1.00 | [starter](inputs/product-safety-market-action-portfolio-report.json) / [report](report-inputs/product-safety-market-action-portfolio-report.json) |
| [eCFR & Federal Register Change Report](https://apify.com/taroyamada/regulatory-obligation-change-impact-report?utm_source=github_pages&utm_medium=starter_catalog&utm_campaign=phase10_paid_reports&utm_content=regulatory-obligation-change-impact-report__github_readme) | `regulatory-change-row` + `obligation-impact-alert` | $0.308 | $1.00 | [starter](inputs/regulatory-obligation-change-impact-report.json) / [report](report-inputs/regulatory-obligation-change-impact-report.json) |

## Use

1. Clone this repository and sign in with the [Apify CLI](https://docs.apify.com/cli).
2. Replace sample watch terms or URLs with your own authorized scope.
3. Confirm the live Store pricing and run cap.
4. Run `apify actors call taroyamada/<actor-slug> --input-file inputs/<actor-slug>.json --output-dataset`.
5. Enable the report/export option only after the entry result fits your workflow.

## Billing behavior

- No start charge is configured for these seven Actors.
- Zero-row and unchanged monitor runs have zero event charge.
- `maxChargeUsd` is a hard buyer-controlled cap checked before delivery.
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
