---
description: "Set up the Overboard Studio MCP connection for creating boards from Claude Code"
allowed-tools: Bash, Read, Edit, Write, AskUserQuestion
---

## Overboard Studio MCP Setup

Help the user connect their Overboard Studio account to Claude Code via MCP.

### Step 1: Check if MCP is already configured

Read the user's MCP config file. On macOS/Linux check `~/.claude/claude_mcp_config.json`. Look for an "overboard" entry.

If already configured, tell the user:
> Overboard MCP is already configured! Try `/overboard brainstorm` to create your first board.

### Step 2: If not configured, set it up

The Overboard MCP server runs in two modes:

**Option A: Remote (Recommended — no setup needed)**
Add to `~/.claude/claude_mcp_config.json`:
```json
{
  "mcpServers": {
    "overboard": {
      "type": "url",
      "url": "https://api.overboard.studio/mcp"
    }
  }
}
```
This uses OAuth — the user will be prompted to log in when first using an Overboard command.

**Option B: Local (for development)**
Requires `SUPABASE_URL` and `SUPABASE_SERVICE_ROLE_KEY`:
```json
{
  "mcpServers": {
    "overboard": {
      "command": "node",
      "args": ["/path/to/packages/mcp-server/dist/index.js"],
      "env": {
        "SUPABASE_URL": "https://your-project.supabase.co",
        "SUPABASE_SERVICE_ROLE_KEY": "your-service-role-key"
      }
    }
  }
}
```

### Step 3: Merge with existing config

Read the existing config file. If it exists, merge the "overboard" entry into the existing "mcpServers" object. Don't overwrite other MCP servers.

If the file doesn't exist, create it with just the overboard entry.

### Step 4: Verify

Tell the user:
> MCP configured! Restart Claude Code, then try:
> - `/overboard brainstorm Ideas for Q3 roadmap`
> - `/overboard plan Mobile app launch`
> - `/overboard diagram User authentication flow`
>
> Your boards will appear at https://overboard.studio/boards
> Sign up free at https://overboard.studio/register if you don't have an account yet.
