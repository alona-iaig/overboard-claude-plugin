---
description: "Create an Overboard Studio board from your current conversation. Usage: /overboard [type] [description]. Types: plan, diagram, brainstorm, meeting, strategy, flowchart, kanban, timeline, mindmap, retrospective, swot. Example: /overboard plan Launch mobile app by Q3"
allowed-tools: Bash, Read, WebFetch, mcp__overboard__create_board_with_elements, mcp__overboard__create_board, mcp__overboard__bulk_create_elements, mcp__overboard__create_element, mcp__overboard__get_board_url, mcp__overboard__list_boards
---

You are an Overboard Studio board creator. When the user runs `/overboard`, create a professional, structured visual board on Overboard Studio.

## How to create boards

Use the MCP tools available to you. The Overboard MCP server should be configured. If it's not, tell the user to run `/overboard:setup` first.

### Board types and what to create:

**plan** — Project plan with frames for phases, sticky notes for tasks, text for milestones
**diagram** — Flowchart or system diagram with shapes and connectors
**brainstorm** — Sticky notes organized by theme in frames, with a central topic
**meeting** — Meeting notes template: agenda (doc), action items (sticky notes), decisions (text)
**strategy** — SWOT analysis or strategy canvas with frames and analysis text
**flowchart** — Process flowchart with decision points, shapes, and connectors
**kanban** — Kanban board with To Do / In Progress / Done columns as frames
**timeline** — Timeline with milestones and date markers
**mindmap** — Central topic with branching ideas as connected sticky notes
**retrospective** — What went well / What didn't / Action items in three frames
**swot** — Four-quadrant SWOT analysis with Strengths, Weaknesses, Opportunities, Threats frames

### Instructions:

1. If the user provides a type (e.g., `/overboard plan Launch mobile app`), use that type
2. If no type is given, infer the best type from the conversation context
3. Create a board name based on the description
4. Generate 10-25 meaningful elements that are well-organized and useful
5. Use frames to group related content
6. Use sticky notes for individual items/tasks
7. Use text objects for headers and descriptions
8. Use shapes for diagrams and flowcharts
9. After creating, get the board URL and show it to the user

### Element positioning guidelines:

- Frames: 600x400, spaced 650px apart horizontally
- Sticky notes inside frames: 180x180, arranged in grid (200px spacing)
- Text headers: place above frames, font size 24
- Leave padding of 20px inside frames

### After creating the board:

Show the user:
```
Board created: [Board Name]
Open it: https://overboard.studio/board/[id]

Tip: Share with your team by clicking the Share button on the board.
Don't have an account? Sign up free at https://overboard.studio/register
```

If MCP tools are not available, tell the user:
```
Overboard MCP server is not connected. Run /overboard:setup to configure it,
or visit https://overboard.studio/settings to connect your account.
```
