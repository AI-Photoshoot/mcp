# AI Photoshoot MCP server

Create AI photoshoots, headshots and photo edits from your AI assistant, with your [AI Photoshoot](https://aiphotoshoot.com) credits.

This is a hosted (remote) MCP server. You do not install anything.

| Server | URL | Sign-in | Tools |
|---|---|---|---|
| Full | `https://aiphotoshoot.com/mcp` | OAuth (your AI Photoshoot account) | list_photoshoot_styles, list_models, get_credit_balance, generate_image, get_generation |
| Styles only | `https://aiphotoshoot.com/mcp/styles` | None | list_photoshoot_styles, create_editor_link |

Registry name: `com.aiphotoshoot/mcp` on the [official MCP Registry](https://registry.modelcontextprotocol.io/v0/servers?search=com.aiphotoshoot).

## Connect

**Claude (claude.ai, Desktop):** Settings > Connectors > Add custom connector. Paste `https://aiphotoshoot.com/mcp`.

**Claude Code:**
```sh
claude mcp add --transport http aiphotoshoot https://aiphotoshoot.com/mcp
```

**ChatGPT:** Settings > Apps & Connectors > Advanced > Developer mode. Then Create, and paste `https://aiphotoshoot.com/mcp`.

**Grok:** grok.com/connectors > New Connector > Custom. Paste `https://aiphotoshoot.com/mcp`.

**Cursor / VS Code / other clients:**
```json
{
  "mcpServers": {
    "aiphotoshoot": { "url": "https://aiphotoshoot.com/mcp" }
  }
}
```

The first tool call opens a sign-in page. Sign in with Google and approve access.

## Tools

- `list_photoshoot_styles`: themed styles (birthday, wedding, couple, maternity, engagement, headshots and more) with prompt templates.
- `list_models`: image models and their credit cost.
- `get_credit_balance`: your credits.
- `generate_image`: make an image from a prompt. Attach up to 4 photo URLs to edit them or keep a face. Spends credits.
- `get_generation`: get the status and URL of an image.
- `create_editor_link` (styles server only): a link that opens a prompt in the AI Photoshoot editor.

## Example prompts

- "Make me a pastel birthday photoshoot from this selfie."
- "Turn this photo into a professional LinkedIn headshot."
- "Show me wedding photo styles, then make one with Nano Banana Pro."

## Links

- Website: https://aiphotoshoot.com
- Pricing: https://aiphotoshoot.com/pricing
- Privacy: https://aiphotoshoot.com/privacy
- Terms: https://aiphotoshoot.com/terms
- Support: support@aiphotoshoot.com
