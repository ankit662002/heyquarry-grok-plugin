# HeyQuarry Grok / Cursor plugin

Hosted MCP + skill for Grok Bot and Grok Build — search HeyQuarry’s Shopify store and app catalog.

**Listing copy**

- **Name:** HeyQuarry  
- **Category:** Research  
- **Description:** Free Shopify store database. Search stores by apps, niche, location, technology and more.

## Free scope

Returns **firmographics and app metadata only**:

- Stores: domain, merchant name, country, platform, ranks, sales/visits estimates, categories, installed app **names**, theme, plan, status
- Apps: name, description, reviews, rating, installs, categories, App Store URL, vendor geo

**Never** returns emails, phones, social profiles, people, or vendor contact fields on the Free plugin plan.

Contact enrichment is available with a HeyQuarry Business subscription at [heyquarry.com](https://heyquarry.com).

## Setup

1. Create a catalog API key (super-admin: `POST /api/admin/catalog-keys` with `{ "name": "Grok" }`).
2. Set `HEYQUARRY_API_KEY` to the returned `hq_live_…` value.
3. Install this plugin from the Grok marketplace (or point `.mcp.json` at `https://heyquarry.com/api/mcp`).

## Rate limits & quotas

- **60 requests/minute** per API key
- **Free** (`free_plugin`): **10,000 lifetime records** (each store/app/install row returned counts as 1). Facets do not count. When the cap is hit, requests fail until you upgrade.
- **Business** (`business_plugin`): unlimited records (still rate-limited)

Create keys via super-admin `POST /api/admin/catalog-keys` with `{ "name": "…", "plan": "free_plugin" | "business_plugin" }`.

## Privacy

See https://heyquarry.com for the privacy policy. Catalog queries are authenticated by API key; we retain key metadata (prefix, last used) and do not store full search result dumps from the plugin.
