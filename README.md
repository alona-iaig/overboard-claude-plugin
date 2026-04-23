# Overboard Studio for Claude Code

Turn your Claude Code conversations into visual boards, diagrams, and plans — directly from your terminal.

## What it does

The Overboard plugin lets you create professional visual content on [Overboard Studio](https://overboard.studio) without leaving Claude Code:

- **Project Plans** — Phased plans with tasks, milestones, and timelines
- **Diagrams & Flowcharts** — System architecture, user flows, decision trees
- **Brainstorming** — Sticky notes organized by theme
- **Strategy** — SWOT analysis, business model canvas, competitive analysis
- **Meeting Notes** — Agenda, action items, decisions
- **Kanban Boards** — To Do / In Progress / Done task tracking
- **Mind Maps** — Central topic with branching ideas
- **Retrospectives** — What went well / What didn't / Action items

Every board is shareable, collaborative, and editable at [overboard.studio](https://overboard.studio).

## Install

```
/plugin marketplace add alona-iaig/overboard-claude-plugin
/plugin install overboard
```

Then set up the connection:

```
/overboard:setup
```

## Usage

```
/overboard plan Launch mobile app by Q3
/overboard brainstorm Ideas for improving onboarding
/overboard diagram User authentication flow
/overboard flowchart CI/CD pipeline
/overboard kanban Sprint 14 tasks
/overboard meeting Weekly team sync
/overboard strategy Q3 product roadmap
/overboard retrospective Sprint 13 review
/overboard swot Competitive analysis vs Miro
/overboard mindmap Feature ideas for v2
```

Or just `/overboard` with a description — the AI will pick the best board type:

```
/overboard How should we restructure the API?
```

## What is Overboard Studio?

[Overboard Studio](https://overboard.studio) is a free AI-powered collaborative whiteboard. Features include:

- AI board generation from text prompts
- Real-time collaboration with video calls
- 40+ templates (SWOT, Kanban, Mind Map, etc.)
- Export to PNG, SVG, PDF, PowerPoint
- MCP integration for AI assistants

**Free plan** includes unlimited boards. [Sign up here](https://overboard.studio/register).

## How it works

The plugin connects to Overboard Studio via MCP (Model Context Protocol). When you run `/overboard`, it:

1. Analyzes your request and conversation context
2. Creates a structured board with appropriate elements
3. Returns a direct link to your board on overboard.studio

No API keys needed — uses OAuth to connect to your Overboard account.

## Links

- [Overboard Studio](https://overboard.studio)
- [Sign Up (Free)](https://overboard.studio/register)
- [Templates Gallery](https://overboard.studio/templates/gallery)
- [Documentation](https://overboard.studio/settings)

## License

MIT
