# FoxPlug in Cline

Get an agent key first: open https://foxplug.com/app/, Settings, Your code, Read straight from the AI tool you code in, Make an agent key. It is shown once and starts with `fpk_`. Replace `fpk_YOUR_AGENT_KEY` below with it. Never commit the real key.

Config file: cline_mcp_settings.json (in the Cline panel: MCP Servers, Configure, Configure MCP Servers; the CLI keeps it at ~/.cline/data/settings/cline_mcp_settings.json)

```json
{
  "mcpServers": {
    "foxplug": {
      "type": "streamableHttp",
      "url": "https://foxplug.com/mcp",
      "headers": {
        "Authorization": "Bearer fpk_YOUR_AGENT_KEY"
      }
    }
  }
}
```

Command line alternative:

```
cline mcp add foxplug https://foxplug.com/mcp --transport http --header "Authorization: Bearer fpk_YOUR_AGENT_KEY" --yes
```

Add this one line to Cline rules so Cline tells FoxPlug what it built:

> After you finish a change a user would notice, call the foxplug log_update tool with a one-paragraph plain summary. For plumbing nobody outside needs to hear about (refactors, dependency bumps, migrations), call it with user_facing set to false.

This page follows the tool's own documentation; check its current docs if a field name has changed.
