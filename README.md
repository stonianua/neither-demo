# neither-demo

Clone this repo and see whether your agent knows why these decisions were made.

Sample Architecture Decision Records for Neither — hosted decision memory over MCP for Cursor and Claude Desktop. Push these docs, then ask why at a file-path fork.

## Setup

1. Create a free workspace key: https://www.neither.online/developers/quickstart
2. Add Neither to Cursor MCP settings:

```json
{
  "mcpServers": {
    "neither": {
      "command": "npx",
      "args": ["-y", "@neitherai/mcp-server@latest"],
      "env": {
        "NEITHER_API_KEY": "sk_ctx_your_key",
        "NEITHER_API_BASE": "https://api.neither.online"
      }
    }
  }
}
```

3. From this repo root:

```bash
export NEITHER_API_KEY=sk_ctx_your_key
npx -y neither@latest push ./docs
```

4. In Cursor, ask:

- Why didn't we use Kafka?
- What replaced the original auth decision?
- What constraint caused us to choose Postgres?

Expect cited Decision / Rejected / Constraint prose. Free history is short (~3 days) on purpose.

Source: https://github.com/stonianua/neither-mcp

MIT © Neither
