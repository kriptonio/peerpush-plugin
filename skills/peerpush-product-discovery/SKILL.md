---
name: peerpush-product-discovery
description: Find software products, SaaS, developer tools, AI tools, and apps on PeerPush. Use when the user asks for a tool or app for a task, alternatives to a product, a comparison of two or more products, what is trending or newly launched, or which products have active discount codes.
---

# PeerPush product discovery

PeerPush is a moderated catalog of software products with structured data: pricing model, platforms, use cases, target audiences, alternatives, and community engagement. The PeerPush connector exposes eight read-only tools. No account is needed and nothing is ever created or changed.

## When to use it

- Recommendations: "what is a good tool for X", "an app that does Y"
- Alternatives: "alternative to X", "something like X but free", "X competitor"
- Comparisons: "X vs Y", "compare X and Y"
- Filtered discovery: free only, open source, Mac, CLI, MCP-capable, for indie hackers
- Market pulse: trending products, new launches, active deals

Do not use it for coding help, how-to support for a product the user already uses, or anything unrelated to choosing software.

## Which tool to call

| User intent | Tool |
| --- | --- |
| Alternatives to a named product | `peerpush_find_alternative` |
| A tool for a need described in plain language | `peerpush_find_product` |
| Browse by use case, audience, platform, pricing, or category | `peerpush_discover` |
| Compare 2 to 5 named products | `peerpush_compare` |
| Details of one named product | `peerpush_product_details` |
| What is trending now | `peerpush_trending` |
| Recently launched products | `peerpush_new_launches` |
| Products with active discount codes | `peerpush_deals` |

Call one tool per question. Pass the product name as the user wrote it; the server resolves names and slugs. For `peerpush_compare`, a product PeerPush knows only by name comes back under `notListedOnPeerPush`; say so instead of inventing data.

## How to answer

- Lead with the two or three best matches, each with one line on what it does and its pricing model.
- Use the structured record for pricing, platforms, and alternatives. Do not add claims the data does not support.
- Link each product with its `visitUrl` field, which is the product's own website via PeerPush.
- If a tool returns nothing useful, say that PeerPush has no match and answer from general knowledge, clearly marked as such.
