# Stompy – AI Memory for Claude & MCP Agents

Persistent memory system that prevents context loss between AI sessions. Store, search, and recall project knowledge across conversations.

## Features

- **Semantic Search** — Hybrid keyword + vector search over your project contexts
- **Conflict Detection** — NLI-powered contradiction detection across stored knowledge
- **Ticket Management** — Built-in ticketing with state machines per ticket type
- **Document Ingestion** — Upload and process documents with AI chunking
- **Multi-Project** — Isolated storage per project with cross-project search

## Quick Start

### VS Code / Cursor / Windsurf

Search `@mcp stompy` in the extensions gallery, or add manually:

```json
// .vscode/mcp.json
{
  "servers": {
    "stompy": {
      "type": "http",
      "url": "https://mcp.stompy.ai"
    }
  }
}
```

### Claude Desktop

Add to your Claude Desktop config (`~/Library/Application Support/Claude/claude_desktop_config.json`):

```json
{
  "mcpServers": {
    "stompy": {
      "url": "https://mcp.stompy.ai"
    }
  }
}
```

### Claude Code

```bash
claude mcp add stompy --transport streamable-http https://mcp.stompy.ai
```

## Tools

| Tool | Description |
|------|-------------|
| `lock_context` | Store content as immutable versioned snapshot |
| `recall_context` | Retrieve locked context by topic |
| `context_search` | Hybrid semantic + keyword search |
| `ticket` | CRUD + lifecycle for project tickets |
| `ticket_board` | View ticket board grouped by status |
| `detect_conflicts` | Detect contradictions using NLI |
| `ingest_document` | Ingest documents with AI processing |
| `project_create` | Create a new project with isolated storage |
| `db_query` | Read-only SQL queries against project database |

## Authentication

Stompy uses OAuth2 authentication. On first connection, your MCP client will prompt you to authorize via browser.

## Links

- **Website**: [stompy.ai](https://stompy.ai)
- **MCP Endpoint**: `https://mcp.stompy.ai`
