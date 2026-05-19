# PostHog post-wizard report

The wizard has completed a deep integration of PostHog into the FashionHero Quality Score Dashboard. PostHog is initialized via the HTML snippet in the app's `<head>` section. Six custom events are tracked across five React components, covering the full seller engagement and Promoted Listings conversion funnel.

| Event | Description | File |
|---|---|---|
| `sidebar_tab_clicked` | User clicks a navigation tab in the sidebar (properties: `tab`, `tab_label`) | `index.html` |
| `quality_score_tile_clicked` | User clicks the Quality Score summary tile on the Dashboard (properties: `score`, `score_label`, `multiplier`) | `index.html` |
| `quality_score_viewed` | User opens the Quality Score detail view — top of PL upsell funnel (properties: `score`, `score_label`) | `index.html` |
| `metric_improvement_opened` | User opens the improvement modal for a metric (properties: `metric_id`, `metric_label`, `metric_value`, `metric_unit`, `benchmark`, `score_contrib`, `max_contrib`) | `index.html` |
| `metric_improvement_closed` | User closes the metric improvement modal (properties: `metric_id`) | `index.html` |
| `promoted_listings_clicked` | User clicks the "Kampanie PL" link in the Promoted Listings banner (properties: `multiplier`, `multiplier_label`, `score`) | `index.html` |

## Next steps

We've built some insights and a dashboard for you to keep an eye on user behavior, based on the events we just instrumented:

- [Analytics basics dashboard](https://eu.posthog.com/project/183039/dashboard/692321)
- [PL Upsell Conversion Funnel](https://eu.posthog.com/project/183039/insights/Sfn8o7qw) — 4-step funnel from Quality Score tile click to Promoted Listings click
- [Sidebar Navigation by Tab](https://eu.posthog.com/project/183039/insights/2YAlXXy6) — which sections sellers navigate to most
- [Promoted Listings Clicks Over Time](https://eu.posthog.com/project/183039/insights/jtbaGFtj) — campaign interest trend
- [Metric Improvement Modal Opens by Metric](https://eu.posthog.com/project/183039/insights/VNAa5CQJ) — which quality metrics sellers struggle with most
- [Quality Score Detail Views](https://eu.posthog.com/project/183039/insights/usMKGDGY) — daily active sellers engaging with the score breakdown

### Agent skill

We've left an agent skill folder in your project. You can use this context for further agent development when using Claude Code. This will help ensure the model provides the most up-to-date approaches for integrating PostHog.
