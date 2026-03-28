# awareness-canvas

> A canvas where your AI builds the dashboard.

`awareness-canvas` is the visual companion to [mcp-awareness](https://github.com/cmeans/mcp-awareness). Instead of a fixed dashboard with pre-built widgets, you have a chat panel and a spatial canvas. Ask your AI for a visualization and it generates a React component on the fly, queries Awareness for the data, and renders it as a draggable, resizable widget on your canvas.

Over time, your canvas becomes your personalized dashboard — not because you configured it, but because you asked for what you wanted and kept what was useful.

## Status

**Planning phase.** See [docs/design.md](docs/design.md) for the architecture and approach.

## How it works

1. You type in the chat panel: "Show me my pending intentions on a timeline"
2. The AI generates a self-contained React component that queries Awareness
3. The widget appears on the canvas — drag it, resize it, keep it or close it
4. Say "add a tag cloud next to it" and another widget appears
5. Your layout persists across sessions

## What makes this different

- **No widget catalog to learn.** You describe what you want in natural language.
- **Widgets are data-aware from birth.** The AI generates them with the query baked in.
- **The AI knows your data shape** (via `get_stats`, `get_tags`) and can suggest visualizations.
- **Widgets can be conversational.** "This chart looks wrong, filter out the test entries" and the AI regenerates it in place.
- **Some core widgets ship pre-built** for zero-friction onboarding.

## Relationship to mcp-awareness

`mcp-awareness` is the store — knowledge, intentions, alerts, patterns. It speaks MCP.

`awareness-canvas` is the surface — a web app that talks to Awareness through the AI. The AI is the API layer. The canvas never touches the database directly.

## License

[AGPL-3.0-or-later](LICENSE)

---

*Part of the [Awareness](https://github.com/cmeans/mcp-awareness) ecosystem. Copyright (c) 2026 Chris Means.*
