# Overboard Studio Claude Code Plugin

This plugin adds `/overboard` slash commands to Claude Code for creating visual boards on Overboard Studio.

## Plugin Structure
- `.claude-plugin/plugin.json` — Plugin manifest (name, commands, metadata)
- `commands/board.md` — Main `/overboard` slash command
- `commands/setup.md` — `/overboard:setup` for MCP connection config

## How it works
The plugin relies on the Overboard MCP server being configured. The `/overboard:setup` command helps users connect. Once connected, `/overboard` uses MCP tools to create boards with elements.
