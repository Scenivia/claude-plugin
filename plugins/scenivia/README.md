# Scenivia plugin for Claude Code

Connects Claude Code to [Scenivia](https://scenivia.com): the agent briefs a
film, picks a Library template and writes every line of it itself (no AI
generation spent on Scenivia's side), refines the brand, music and pictures,
checks the export and renders the MP4. It carries one skill (`skills/scenivia/`) and the
connection to the Scenivia MCP server (`.mcp.json`, HTTP with OAuth). It holds
no secret.

```
/plugin marketplace add Scenivia/claude-plugin
/plugin install scenivia@scenivia
```

The first call opens the Scenivia consent page in your browser. The plugin asks
for `scenivia:read` and `scenivia:edit`; exporting needs `scenivia:render`,
granted separately. Exports spend credits only when they succeed. Driving
Scenivia from an agent is part of the Pro and Max plans; on another plan the
consent page and every call say so, with the link to upgrade.

Never put a token in `.mcp.json` or in a header: the OAuth flow keeps it in
Claude Code's own credential store.

Installation, scopes, tools, limits and support:
[the repository README](https://github.com/Scenivia/claude-plugin#readme).
