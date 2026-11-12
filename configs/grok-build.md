# FoxPlug in Grok Build

Get an agent key first: open https://foxplug.com/app/, Settings, Your code, Read straight from the AI tool you code in, Make an agent key. It is shown once and starts with `fpk_`. Replace `fpk_YOUR_AGENT_KEY` below with it. Never commit the real key.

Config file: ~/.grok/config.toml, or the grok mcp add command (add --scope project to write .grok/config.toml in the project)

```toml
[mcp_servers.foxplug]
url = "https://foxplug.com/mcp"
headers = { "Authorization" = "Bearer fpk_YOUR_AGENT_KEY" }
```

Command line alternative:

```
grok mcp add --transport http foxplug https://foxplug.com/mcp --header "Authorization: Bearer fpk_YOUR_AGENT_KEY"
```

Add this one line to AGENTS.md so Grok Build tells FoxPlug what it built:

> After you finish a change a user would notice, call the foxplug log_update tool with a one-paragraph plain summary. For plumbing nobody outside needs to hear about (refactors, dependency bumps, migrations), call it with user_facing set to false.

This page follows the tool's own documentation; check its current docs if a field name has changed.
