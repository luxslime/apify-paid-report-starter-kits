# Make and n8n first paid runs

Paste-ready Actor input for [Make](https://docs.apify.com/integrations/make) (**Run an Actor** → Input JSON) and [n8n](https://docs.apify.com/integrations/n8n) (**Run Actor** → Custom input). Each file is the same cheapest first paid run as `inputs/`. Select the Actor ID in the module, paste this JSON, keep `delivery` `dataset`, then use **Get Dataset Items** on `defaultDatasetId`. Do not enable report or export options on the first paid run.

| Actor | Actor ID | Cheapest first paid run | Make | n8n |
| --- | --- | --- | --- | --- |
| [Article Extractor & Reader Scraper (News, Blog, RAG)](https://apify.com/taroyamada/article-content-extractor) | `taroyamada/article-content-extractor` | One public article URL; `generateReport` false; `emitExport` false. Live Store PPE: Actor Start $0.00005, Useful article row $0.008. | [input](make/article-content-extractor.json) | [input](n8n/article-content-extractor.json) |
| [G2 & Capterra Review Scraper](https://apify.com/taroyamada/g2-capterra-review-intelligence) | `taroyamada/g2-capterra-review-intelligence` | One review page URL; modest `reviewLimit` (25); `dryRun` false. Live Store PPE: Actor Start $0.001, result $0.01. | [input](make/g2-capterra-review-intelligence.json) | [input](n8n/g2-capterra-review-intelligence.json) |
| [Apple Podcasts Chart Scraper](https://apify.com/taroyamada/apple-podcast-chart-tracker) | `taroyamada/apple-podcast-chart-tracker` | One US storefront; chart depth 3; `generateMovementReport` false. Live Store PPE: apify-default-dataset-item $0.003. | [input](make/apple-podcast-chart-tracker.json) | [input](n8n/apple-podcast-chart-tracker.json) |
| [Apple Podcasts Reviews Scraper](https://apify.com/taroyamada/apple-podcast-reviews-monitor) | `taroyamada/apple-podcast-reviews-monitor` | Snapshot mode; one podcast ID; one country; `maxPagesPerPair` 1; `generateReport` false. Live Store PPE: apify-default-dataset-item $0.003. | [input](make/apple-podcast-reviews-monitor.json) | [input](n8n/apple-podcast-reviews-monitor.json) |

Confirm live Store pricing before a paid run. These JSON files use only live input-schema keys so they paste into Make or n8n without extra properties.
