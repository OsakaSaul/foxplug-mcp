# FoxPlug MCP server

FoxPlug turns what you ship into launch posts, a walkthrough of your own screens and a changelog. Everything is a draft until you approve it. Nothing posts by itself.

This MCP server is hosted. There is nothing to install.

![FoxPlug](assets/foxplug-fox-512.png)

- Endpoint: https://foxplug.com/mcp (Streamable HTTP)
- Auth: header `Authorization: Bearer fpk_YOUR_AGENT_KEY`
- Get a key: open https://foxplug.com/app/ , Settings, Your code, Read straight from the AI tool you code in, Make an agent key. It is shown once.
- Registry name: `io.github.OsakaSaul/foxplug` (Official MCP Registry)
- Tools (11): record_work, log_update, get_brief, list_drafts, simulate_buyers, set_plan, check_drift, get_plan_status, what_nobody_knows, recall, supersede_fact. Capture is free; nothing posts.

## Set it up in your tool

| Tool | Guide |
|---|---|
| Cursor | [configs/cursor.md](configs/cursor.md) |
| Kiro | [configs/kiro.md](configs/kiro.md) |
| Cline | [configs/cline.md](configs/cline.md) |
| Gemini CLI | [configs/gemini-cli.md](configs/gemini-cli.md) |
| OpenAI Codex CLI | [configs/codex.md](configs/codex.md) |
| Grok Build | [configs/grok-build.md](configs/grok-build.md) |

`.mcp.json` at the root is the same config for tools that read it, with a placeholder key.

## Links

- Home https://foxplug.com
- Privacy https://foxplug.com/legal/privacy , terms https://foxplug.com/legal/terms , trust https://foxplug.com/trust/ , support https://foxplug.com/support.html

## Privacy Policy

Data handling is described at https://foxplug.com/legal/privacy.
