# Apify Paid Report Starter Kits

Small, capped inputs for testing seven public-data and authorized-site Apify Actors before enabling their full report events.

These examples are intentionally **not dry runs**: they exercise the real public source and bill only delivered rows. Every input has `maxChargeUsd <= 1`. Full reports remain opt-in and use the prices shown on each Actor's live Apify Store page.

| Actor | Entry event | Run cap | Starter input |
| --- | --- | ---: | --- |
| [Technical SEO & AI Crawler Audit](https://apify.com/taroyamada/technical-seo-portfolio-regression-report) | `seo-page-audited` at $0.012 | $0.50 | [input](inputs/technical-seo-portfolio-regression-report.json) |
| [Apple Podcasts Category Benchmark](https://apify.com/taroyamada/podcast-category-network-benchmark-report) | `podcast-show-benchmarked` at $0.008 | $0.50 | [input](inputs/podcast-category-network-benchmark-report.json) |
| [Clinical Trials & PubMed Evidence Gap Report](https://apify.com/taroyamada/biomedical-trial-literature-evidence-report) | `biomedical-evidence-row` at $0.008 | $0.50 | [input](inputs/biomedical-trial-literature-evidence-report.json) |
| [App Store Release & Review Benchmark](https://apify.com/taroyamada/app-release-category-review-benchmark-report) | `app-benchmarked` at $0.015 | $0.50 | [input](inputs/app-release-category-review-benchmark-report.json) |
| [npm & PyPI Dependency Risk Report](https://apify.com/taroyamada/package-portfolio-upgrade-risk-report) | `package-risk-row` at $0.010 | $0.50 | [input](inputs/package-portfolio-upgrade-risk-report.json) |
| [CPSC & NHTSA Recall Portfolio Watch](https://apify.com/taroyamada/product-safety-market-action-portfolio-report) | `safety-record-row` at $0.006 | $1.00 | [input](inputs/product-safety-market-action-portfolio-report.json) |
| [eCFR & Federal Register Change Report](https://apify.com/taroyamada/regulatory-obligation-change-impact-report) | `regulatory-change-row` at $0.008 | $1.00 | [input](inputs/regulatory-obligation-change-impact-report.json) |

## Use

1. Open the Actor link.
2. Paste the matching JSON from `inputs/`.
3. Replace sample watch terms or URLs with your own authorized scope.
4. Confirm the live Store pricing and run cap.
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
