# MCP Checkup

**Look before your agent connects.** MCP Checkup watches public MCP servers and publishes what it observed: reachability, protocol revision, tool and schema fingerprints, publicly observable auth metadata, and tool-description hygiene signals. Changes to a server's tool set are recorded with signed evidence.

Facts, not verdicts: every check is VERIFIED, FAILED, OBSERVED_RISK or UNVERIFIED. Nothing is scored, blocked, or judged.

- 🌐 Directory: [mcpcheckup.com/servers](https://mcpcheckup.com/servers)
- 🔌 MCP endpoint: `https://mcpcheckup.com/mcp` (Streamable HTTP, no account, no API key)
- 📇 Official MCP Registry: `com.mcpcheckup/mcp` · [Claude Connectors Directory](https://claude.ai/directory/connectors/mcp-checkup)

## Start here

| Repo | What it's for |
| --- | --- |
| [**preflight**](https://github.com/mcpcheckup/preflight) | One-minute setup: a Claude Code plugin, a Cursor rule, and an AGENTS.md snippet that make your agent check a server on MCP Checkup before connecting. |
| [**checks**](https://github.com/mcpcheckup/checks) | Check our work: the check suite, the canonicalizer and schema behind signed attestations, a toolset diff, and an offline verifier. |

**Claude Code, in two lines:**

```
/plugin marketplace add mcpcheckup/preflight
/plugin install mcp-preflight@mcpcheckup
```

**Any MCP client:**

```json
{ "mcpServers": { "mcpcheckup": { "type": "http", "url": "https://mcpcheckup.com/mcp" } } }
```

Maintainers: your server may already have a report page. See [mcpcheckup.com/maintainers](https://mcpcheckup.com/maintainers).
