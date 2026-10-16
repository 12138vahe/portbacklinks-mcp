# PortBacklinks MCP

Let AI assistants search free backlink submission directories and get step-by-step submission checklists and guides for each platform.

**Remote MCP server** (Streamable HTTP, read-only, no API key): `https://portbacklinks.com/api/mcp`

Website: https://portbacklinks.com

## Tools

| Tool | Description |
|---|---|
| `search_backlink_sources` | Search free backlink / directory submission sources by query, type, cost, link attribute, language (max 20 results) |
| `get_source_details` | Get the submission checklist and guide for one source (`source_id`) |

## Setup

Any MCP client that supports remote servers (Claude, Cursor, VS Code, Windsurf, etc.):

```json
{
  "mcpServers": {
    "portbacklinks": {
      "url": "https://portbacklinks.com/api/mcp"
    }
  }
}
```

Clients that only support stdio can use `mcp-remote`:

```json
{
  "mcpServers": {
    "portbacklinks": {
      "command": "npx",
      "args": ["-y", "mcp-remote", "https://portbacklinks.com/api/mcp"]
    }
  }
}
```

## Limits

Anonymous and free. Rate limited to 20 requests/minute and 200/day per IP.

## License

MIT
