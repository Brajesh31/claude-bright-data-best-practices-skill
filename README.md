# Claude Bright Data Best Practices Skill

A developer reference for choosing and implementing Bright Data web data products. It explains when to use Web Unlocker, SERP API, Web Scraper API, or Browser API, with practical authentication, request, response, and operational patterns.

## What It Covers

- **API selection:** Match scraping, search, structured extraction, and browser interaction to the appropriate Bright Data product.
- **Authentication:** Configure API keys, zone names, and Browser API credentials securely.
- **Web Unlocker:** Fetch page content without browser interaction.
- **SERP API:** Retrieve structured search results from supported search engines.
- **Web Scraper API:** Use pre-built datasets for structured extraction from supported platforms.
- **Browser API:** Automate pages through Playwright, Puppeteer, or Selenium using CDP/WebDriver.
- **Operations:** Handle asynchronous jobs, pagination, sessions, geographic targeting, errors, and usage costs.

## Installation

Clone the repository into your Claude skills directory:

```bash
git clone https://github.com/Brajesh31/claude-bright-data-best-practices-skill.git ~/.claude/skills/bright-data-best-practices
```

This repository is a reference skill. Configure the appropriate Bright Data product and credentials for the workflow you intend to run.

## Choosing the Right API

| Need | Bright Data product |
|---|---|
| Fetch a page by URL without interaction | Web Unlocker |
| Extract search engine results | SERP API |
| Retrieve structured data from supported platforms | Web Scraper API |
| Click, scroll, fill forms, or execute page JavaScript | Browser API |

## Authentication

Keep API keys and zone credentials in environment variables or a secret manager. Never commit credentials:

```bash
export BRIGHTDATA_API_KEY="your-api-key"
export BRIGHTDATA_UNLOCKER_ZONE="your-unlocker-zone"
export BRIGHTDATA_SERP_ZONE="your-serp-zone"
export BROWSER_AUTH="customer-zone:password"
```

## Using the Skill

Example request:

```text
Use the bright-data-best-practices skill to choose the right Bright Data
API for extracting structured results from a set of webpages.
```

The skill's detailed product guidance is organized in [SKILL.md](SKILL.md), with supporting references for Web Unlocker, SERP API, Web Scraper API, and Browser API.

## References

- `references/web-unlocker.md`
- `references/serp-api.md`
- `references/web-scraper-api.md`
- `references/browser-api.md`

## Good Practices

Choose the most specific product for the task. Use Browser API for browser automation rather than trying to combine Web Unlocker with browser automation libraries. Review current product documentation, billing, and service limits before production use.
