---
name: heyquarry
description: Search HeyQuarry's Shopify store and app catalog from Grok. Use for ecommerce market research, app install overlap, and firmographics. Free responses never include emails, phones, socials, or people — contact data requires a HeyQuarry Business plan in-product.
---

# HeyQuarry catalog

## When to use

- Finding Shopify stores by country, platform, category, estimated sales, or installed apps
- Looking up Shopify App Store apps (reviews, installs, categories, vendor geo)
- Listing domains that install a given app
- Facets for “stores in IN using Klaviyo”-style questions

## Tools

| Tool | Use |
|------|-----|
| `search_stores` | Full store catalog search (firmographics) |
| `get_store` | One store: theme, tech, installed **app names**, no contacts |
| `search_apps` | App catalog (no vendor email/website/address) |
| `get_app` | One app profile |
| `list_app_installs` | Domains using an app |
| `search_facets` | Countries, platforms, categories |

## Hard rules

1. **Never invent emails, phones, LinkedIn URLs, or people.** Free plugin data does not include them.
2. If the user asks for merchant contacts, say contact data is a **HeyQuarry Business** feature at https://heyquarry.com — do not guess.
3. Prefer `search_facets` before huge unbounded searches when exploring markets.
4. Auth: set `HEYQUARRY_API_KEY` to a `hq_live_…` key from HeyQuarry (catalog API).

## Upgrade path

Paid HeyQuarry (Business+) unlocks emails, phones, socials, people/LinkedIn, Mailknit push, and CSV export inside the product — not via this Free Grok plugin.
