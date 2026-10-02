# PeerPush for Claude

Find, compare, and discover software products with Claude: SaaS tools, developer tools, AI tools, and apps, backed by PeerPush's structured product data.

## What it does

Ask Claude in plain language and it uses the PeerPush connector to answer:

- Find alternatives to a product you already use
- Search for a tool that fits a specific need or platform
- Compare 2 to 5 products side by side
- Look up a product's pricing model, platforms, features, and recent updates
- See what is trending, newly launched, or has an active discount code

The bundled skill teaches Claude when to reach for PeerPush and how to present the results. The bundled MCP connector points at `https://peerpush.com/api/mcp/discovery`.

## Setup

Add the plugin, then connect the PeerPush connector from the plugin's Connectors tab. The connector needs no account, API key, or sign-in.

## Data

Every tool is read-only. The connector sends only the tool arguments Claude chooses, such as a product name or a search phrase, to peerpush.com. PeerPush records the tool used, a one-way hash of the arguments, the calling app's name, and a coarse country code to operate the service and give product owners aggregated statistics. It never receives your chat history. Full details: https://peerpush.com/privacy

Every listing on PeerPush is moderated. Products are reviewed when submitted and whenever they are edited, and products in prohibited categories are removed.

## Links

- Documentation: https://peerpush.com/mcp
- Support: https://peerpush.com/contact
- Privacy policy: https://peerpush.com/privacy
- Terms: https://peerpush.com/terms

## License

MIT. Copyright (c) 2026 Kriptonio Technologies d.o.o.
