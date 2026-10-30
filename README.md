# Hacker News Scraper – Stories, Comments & Who Is Hiring Jobs

Search Hacker News stories and comments, export the front page, or extract every 'Who is hiring?' job post, filtered by keyword. Official HN Algolia API, LLM-ready Markdown, incremental mode.

**[Run it on Apify →](https://apify.com/devteamdrew/hacker-news-scraper?utm_source=github&utm_medium=readme&utm_campaign=hacker-news-scraper)** (pay per result, free Apify account to start)


**Hacker News Scraper** by Moxie: fast, reliable and polite, built on official/public data sources.

## What can it do?

- Tech recruiting: export and filter 'Who is hiring?' posts
- Brand and launch monitoring on HN
- Building datasets of discussions for LLM fine-tuning or RAG
- Trend research on technologies

## Data source

The official Hacker News Algolia search API (`hn.algolia.com`). Public data only.

## Features

- **Pay only for results** (pay-per-event pricing, no monthly rental)
- **Incremental mode**: scheduled runs return only items you haven't received before
- **LLM-ready output**: optional compact Markdown per item for RAG / AI agents
- **Polite rate limiting** with automatic retries and backoff
- Clean, flat JSON you can export as CSV, Excel, JSON or via API


## Quick start

1. Create a free account at [apify.com](https://apify.com/devteamdrew/hacker-news-scraper?utm_source=github&utm_medium=readme&utm_campaign=hacker-news-scraper) and copy your API token.
2. `export APIFY_TOKEN=...`
3. Run one of the examples:

```bash
bash examples/run.sh          # curl
node examples/run.js          # JavaScript (apify-client)
python examples/run.py        # Python (apify-client)
```

Example input ([examples/input.json](examples/input.json)):

```json
{
  "mode": "search",
  "queries": [
    "apify"
  ],
  "maxItems": 20
}
```

## Use with AI agents (MCP)

Add `https://mcp.apify.com/?actors=devteamdrew/hacker-news-scraper` as an MCP server in Claude, Cursor or any MCP client.

## Pricing

See the [Apify Store page](https://apify.com/devteamdrew/hacker-news-scraper?utm_source=github&utm_medium=readme&utm_campaign=hacker-news-scraper) for current pay-per-result pricing.

## More data actors

- [Bluesky Scraper & API – Posts, Profiles & Search](https://apify.com/devteamdrew/bluesky-scraper?utm_source=github&utm_medium=readme&utm_campaign=hacker-news-scraper)
- [Companies House Scraper – UK Company Data, Directors & Filings](https://apify.com/devteamdrew/companies-house-scraper?utm_source=github&utm_medium=readme&utm_campaign=hacker-news-scraper)
- [UK Planning Applications Scraper – 400+ Councils & Postcodes](https://apify.com/devteamdrew/uk-planning-applications?utm_source=github&utm_medium=readme&utm_campaign=hacker-news-scraper)
- [npm Scraper – Package Downloads, Dependencies & Maintainers](https://apify.com/devteamdrew/npm-package-scraper?utm_source=github&utm_medium=readme&utm_campaign=hacker-news-scraper)
- [GitHub Trending Scraper – Repos, Stars & Developers](https://apify.com/devteamdrew/github-trending-scraper?utm_source=github&utm_medium=readme&utm_campaign=hacker-news-scraper)
- [Mastodon Scraper – Fediverse Hashtags, Accounts & Trends](https://apify.com/devteamdrew/mastodon-scraper?utm_source=github&utm_medium=readme&utm_campaign=hacker-news-scraper)
- [Lemmy Scraper – Posts, Comments & Communities (Fediverse)](https://apify.com/devteamdrew/lemmy-scraper?utm_source=github&utm_medium=readme&utm_campaign=hacker-news-scraper)

## License

Examples in this repository are MIT licensed. The actor itself runs on the Apify platform.
