<p align="center">
  <img src="https://overboard.studio/overboard-logo.png" alt="Overboard Studio" width="80" />
</p>

<h1 align="center">Overboard Studio for Claude Code</h1>

<p align="center">
  <strong>Turn conversations into visual boards — directly from your terminal.</strong>
</p>

<p align="center">
  <a href="https://overboard.studio"><img src="https://img.shields.io/badge/overboard.studio-Visit%20Site-6366f1?style=flat-square" alt="Website" /></a>
  <a href="https://github.com/alona-iaig/overboard-claude-plugin/stargazers"><img src="https://img.shields.io/github/stars/alona-iaig/overboard-claude-plugin?style=flat-square&color=f59e0b" alt="Stars" /></a>
  <a href="LICENSE"><img src="https://img.shields.io/badge/license-MIT-green?style=flat-square" alt="MIT License" /></a>
  <a href="https://overboard.studio/register"><img src="https://img.shields.io/badge/Sign%20Up-Free-10b981?style=flat-square" alt="Free Sign Up" /></a>
</p>

---

## Demo

```
you> /overboard plan Launch mobile app by Q3

Creating board "Mobile App Launch Plan"...
 Created 4 phase frames + 16 task items + 3 milestones

Board created: Mobile App Launch Plan
Open it: https://overboard.studio/board/abc123

Tip: Share with your team using the Share button.
```

## Install (30 seconds)

```bash
# 1. Add the marketplace
/plugin marketplace add alona-iaig/overboard-claude-plugin

# 2. Install
/plugin install overboard

# 3. Connect your account
/overboard:setup
```

That's it. Start creating boards.

## Usage

| Command | What it creates |
|---------|----------------|
| `/overboard plan Launch mobile app` | Phased project plan with tasks and milestones |
| `/overboard diagram Auth flow` | System diagram with shapes and connectors |
| `/overboard brainstorm Q3 ideas` | Themed sticky notes in organized frames |
| `/overboard flowchart CI/CD pipeline` | Process flow with decision points |
| `/overboard kanban Sprint 14` | To Do / In Progress / Done columns |
| `/overboard meeting Weekly sync` | Agenda + action items + decisions |
| `/overboard strategy Product roadmap` | Strategic analysis with frames |
| `/overboard retrospective Sprint 13` | What went well / didn't / actions |
| `/overboard swot vs Miro` | Four-quadrant SWOT analysis |
| `/overboard mindmap Feature ideas` | Central topic with branching nodes |
| `/overboard timeline Product milestones` | Timeline with date markers |

Or just describe what you want:

```
/overboard How should we restructure the microservices?
```

The AI picks the best board type automatically.

## Why?

You're already having the conversation in Claude Code. Why switch to another tool to visualize it?

- **No context switching** — create boards without leaving your terminal
- **AI-structured** — boards are organized, not random sticky notes
- **Shareable** — every board has a link your team can open and edit
- **Free** — unlimited boards on the free plan

## What is Overboard Studio?

[Overboard Studio](https://overboard.studio) is a free AI-powered collaborative whiteboard used by teams for:

- Project planning and roadmaps
- Architecture diagrams and flowcharts
- Brainstorming and ideation
- Sprint retrospectives and standups
- Strategy workshops and SWOT analysis
- Meeting notes and action tracking

**Features**: AI board generation, real-time collaboration, video calls, 40+ templates, export to PNG/SVG/PDF/PowerPoint, MCP integration.

## How it works

```
Claude Code  →  MCP Protocol  →  Overboard Studio API  →  Visual Board
    (you)       (this plugin)      (creates elements)      (shareable link)
```

The plugin connects via [MCP](https://modelcontextprotocol.io) (Model Context Protocol). OAuth handles authentication — no API keys to manage.

## Also works with

The Overboard MCP server works with any MCP-compatible AI tool:

- **Claude Desktop** — Add to `claude_desktop_config.json`
- **Cursor** — Add as MCP server in settings
- **ChatGPT** — Via Actions (OpenAPI spec at `api.overboard.studio/openapi.json`)
- **GitHub Copilot** — Via MCP integration

## Links

- [Overboard Studio](https://overboard.studio) — Main website
- [Sign Up Free](https://overboard.studio/register) — Create your account
- [Templates Gallery](https://overboard.studio/templates/gallery) — 40+ ready-made templates
- [MCP Server](https://api.overboard.studio/mcp) — Direct MCP endpoint
- [Blog](https://overboard.studio/blog) — Tips and tutorials

## Contributing

PRs welcome! The plugin is MIT licensed.

## Star History

If this plugin is useful, please star it to help others discover it.

[![Star History Chart](https://api.star-history.com/svg?repos=alona-iaig/overboard-claude-plugin&type=Date)](https://star-history.com/#alona-iaig/overboard-claude-plugin&Date)
