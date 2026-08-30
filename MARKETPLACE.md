# Marketplace listing — heyquarry

Append this object to `.grok-plugin/marketplace.json` in https://github.com/xai-org/plugin-marketplace
after publishing `heyquarry-grok-plugin` to a public GitHub repo and pinning its commit SHA.

```json
{
  "name": "heyquarry",
  "description": "Shopify store + app catalog for Grok — search millions of stores and apps. Free: firmographics and app metadata only, no contact info.",
  "category": "development",
  "source": {
    "source": "url",
    "url": "https://github.com/REPLACE_ORG/heyquarry-grok-plugin.git",
    "sha": "REPLACE_WITH_40_CHAR_COMMIT_SHA"
  },
  "homepage": "https://heyquarry.com",
  "keywords": ["heyquarry", "shopify stores", "shopify apps", "ecommerce leads"],
  "domains": ["heyquarry.com"]
}
```

Then run:

```bash
python3 scripts/generate-plugin-index.py
python3 scripts/validate-catalog.py
```

Open a PR to `xai-org/plugin-marketplace`.
