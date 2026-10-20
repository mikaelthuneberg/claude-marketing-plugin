# Supermetrics for Claude: marketing data and analytics workflows

**Ask Claude about your marketing performance and get answers from your live data.** This plugin connects Claude to Google Ads, Meta Ads, GA4, LinkedIn Ads, TikTok Ads, Microsoft Ads, Shopify, HubSpot and 150+ other marketing platforms through [Supermetrics](https://supermetrics.com). It adds 42 analysis workflows built by marketers.

The Supermetrics connector is included: install the plugin, sign in once, and start asking.

## Install

```
/plugin marketplace add supermetrics-public/claude-marketing-plugin
/plugin install supermetrics-marketing@supermetrics
```

Then run `/supermetrics-marketing:setup`. It signs you in to Supermetrics (OAuth, or a free trial if you're new), shows which platforms are connected, helps you connect one, and runs your first report.

> Using claude.ai or Claude Desktop? Add the [Supermetrics connector](https://claude.ai/directory/connectors/cc599e7b-8c59-4e89-9bf0-36d47bb9ec80) from the connector directory.

## Try asking

- "Compare last week's Facebook Ads performance to the week before. What changed and why?"
- "Which Google Ads search terms spent money last month without converting?"
- "Are we on track to hit this month's paid media budget?"
- "Which of our Meta ads are fatiguing and need new creative?"
- "Rank our channels by ROAS for the last 90 days and recommend where to move budget."
- "Our ad platforms report 400 conversions but GA4 shows 250. Where's the gap?"
- "Build a 90-day marketing performance overview for our leadership deck."
- "Did our San Francisco event lift branded search and traffic in the Bay Area?"
- "Which landing pages get traffic but don't convert?"
- "What's our blended ROAS by day of week across Google and Meta?"

## Slash commands

| Command | What it does |
|---|---|
| `/supermetrics-marketing:setup` | Sign in, check connected platforms, connect one, run a first report |
| `/supermetrics-marketing:weekly-performance` | Week-over-week review with prioritised actions |
| `/supermetrics-marketing:wasted-spend` | Non-converting campaigns, ads and search terms, with the estimated saving |
| `/supermetrics-marketing:ad-fatigue` | Ads with rising frequency and falling CTR |
| `/supermetrics-marketing:budget-pacing` | Month-to-date pacing and a month-end forecast per channel |
| `/supermetrics-marketing:roas-report` | Blended and per-channel ROAS with day-of-week patterns |
| `/supermetrics-marketing:funnel-audit` | Reconcile what ad platforms report with what GA4 saw |
| `/supermetrics-marketing:exec-summary` | 90-day cross-channel overview, ready for a deck |

You don't need to remember any of these. Describe what you want and Claude picks the right workflow.

## Workflows by role

| Skill | For | Workflows |
|---|---|---|
| `performance-marketer` | Paid media managers | WoW optimization · Ad fatigue · Creative testing · Daily standup · Search terms / negatives · Attribution comparison · Budget reallocation |
| `marketing-leader` | CMOs, heads of marketing, analysts | 90-day exec overview · Budget pacing · ROAS benchmarking · Annual planning · New channel case · Efficiency vs goals · CAC and LTV |
| `demand-gen` | B2B demand gen | Traffic-to-conversion audit · Lead-gen efficiency · Pipeline by channel · MQL-to-SQL · ABM · Email + ads funnel · Webinar funnel |
| `content-marketer` | Content and SEO | Landing page diagnosis · Paid promotion · SEO audit · Content attribution · Newsletter · Video · Content gaps |
| `field-marketer` | Events and field | Pre-event ROI · Post-event geo-lift · Event portfolio · Event pipeline · Account engagement · Webinar deep dive · Partner events |
| `ecommerce-marketer` | Ecommerce acquisition | Blended ROAS · Promo anomalies · SKU performance · New vs returning ROAS · AOV and basket · Retention cohorts · Promo planning |

Each workflow pulls data first and then analyzes it. Results come back as charts that colour each change by whether it's good or bad for the business. You can also get a Word doc, spreadsheet or deck when you need something to share.

## Supported platforms

**Paid media:** Google Ads, Meta Ads (Facebook and Instagram), LinkedIn Ads, TikTok Ads, Microsoft Advertising, Amazon Ads, Snapchat, Pinterest, Reddit, X Ads, DV360, Criteo and more.
**Analytics and SEO:** Google Analytics 4, Search Console, Adobe Analytics, Semrush, YouTube.
**Social:** Facebook and Instagram insights, LinkedIn Pages, TikTok organic.
**Ecommerce and CRM:** Shopify, HubSpot, Salesforce, Klaviyo, Mailchimp.

[See all 150+ sources →](https://supermetrics.com/connectors)

## Privacy and safety

- **Read-only.** These workflows never change campaigns, budgets or settings in your ad accounts.
- **Your data goes only to Supermetrics and your Claude session.** Supermetrics fetches it with your own platform logins, and the plugin adds no telemetry or hooks.
- **You choose what's connected**, and you can revoke access at any time in the [Supermetrics Hub](https://hub.supermetrics.com).

See the [privacy policy](https://supermetrics.com/privacy-policy) and [terms](https://supermetrics.com/terms-of-service).

## Pricing

Supermetrics is a paid product with a free trial. Signing in through the plugin starts the trial if you don't have an account yet.

## Support

- Plugin issues: [open an issue](https://github.com/supermetrics-public/claude-marketing-plugin/issues)
- Account, connector or data questions: [Supermetrics support](https://supermetrics.com/support), or ask Claude to "contact Supermetrics support".

## For contributors

Test locally without installing:

```
claude --plugin-dir ./plugins/supermetrics-marketing
```

Each skill has the same layout: a `SKILL.md` (when to trigger, principles, chart framework), `references/workflows.md` (step-by-step prompts), `scripts/` (Python helpers that take a CSV and return a table) and `assets/` (deliverable templates). Slash commands are in `commands/`, and the bundled connector is defined in `.mcp.json`.

Run `claude plugin validate --strict .` before opening a PR. CI runs it too.

## License

MIT
