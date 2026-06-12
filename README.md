# web-mcp-skill

An [agent skill](https://www.skills.sh) that turns your coding agent into a **WebMCP** expert — the proposed web standard (W3C WebML CG, Google + Microsoft) that lets web pages expose client-side functionality as MCP-style tools for in-browser AI agents (Gemini in Chrome, Copilot in Edge).

The skill is **framework-agnostic**: it covers the full standard for any web app — vanilla JS, React, Vue, Svelte, Angular.

## Install

With the [skills.sh CLI](https://github.com/vercel-labs/skills) (works with Claude Code, Codex, Cursor, OpenCode, and many more agents):

```bash
npx skills add cr4yfish/web-mcp-skill
```

## What's inside

[`skills/webmcp/SKILL.md`](skills/webmcp/SKILL.md) — a complete WebMCP reference:

- **Imperative API**: `document.modelContext` / `navigator.modelContext`, `registerTool`, `provideContext`, events, Permissions Policy
- **Declarative API**: `toolname`/`tooldescription` form attributes, schema synthesis, `SubmitEvent.respondWith`, CSS pseudo-classes
- **Security model**: prompt injection, exposure scope, human-in-the-loop design
- **Best practices**: tool granularity, naming, schemas, outputs, errors, lifecycle
- **Framework integration gotchas**: SSR safety, registration timing, re-registration churn, stale closures, cleanup
- **Testing & evals**: DevTools WebMCP panel, the official evals CLI, mocking patterns
- **WebMCP vs. backend MCP** comparison
- Browser availability and how to enable it (flags, origin trial)

## Using React?

Check out **[react-web-mcp](https://github.com/cr4yfish/react-web-mcp)** — zero-dependency React hooks and components (`useWebMCPTool`, `useWebMCP`, `<ToolForm>`) that handle all the WebMCP integration gotchas for you, plus a React-free `react-web-mcp/vanilla` entry usable from any framework. The skill covers it in detail.

## References

- [Spec](https://webmachinelearning.github.io/webmcp/) · [Explainer](https://github.com/webmachinelearning/webmcp)
- [Chrome docs](https://developer.chrome.com/docs/ai/webmcp)
- [Official demos & evals CLI](https://github.com/GoogleChromeLabs/webmcp-tools)
