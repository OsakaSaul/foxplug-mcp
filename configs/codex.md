# FoxPlug in OpenAI Codex CLI

Get an agent key first: open https://foxplug.com/app/, Settings, Your code, Read straight from the AI tool you code in, Make an agent key. It is shown once and starts with `fpk_`. Replace `fpk_YOUR_AGENT_KEY` below with it. Never commit the real key.

Config file: ~/.codex/config.toml (or .codex/config.toml in a trusted project)

```toml
[mcp_servers.foxplug]
url = "https://foxplug.com/mcp"
bearer_token_env_var = "FOXPLUG_AGENT_KEY"
```

Set the key as an environment variable first:

```
export FOXPLUG_AGENT_KEY="fpk_YOUR_AGENT_KEY"   # PowerShell: setx FOXPLUG_AGENT_KEY "fpk_YOUR_AGENT_KEY", then open a new terminal
```

Add this one line to AGENTS.md so OpenAI Codex CLI tells FoxPlug what it built:

> After you finish a change a user would notice, call the foxplug log_update tool with a one-paragraph plain summary. For plumbing nobody outside needs to hear about (refactors, dependency bumps, migrations), call it with user_facing set to false.

This page follows the tool's own documentation; check its current docs if a field name has changed.
