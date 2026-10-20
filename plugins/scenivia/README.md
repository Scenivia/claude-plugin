# Scenivia plugin for Claude Code

Connects Claude Code to [Scenivia](https://scenivia.com): the agent can brief a
film, compare the Library templates, propose and apply typed edits, check the
export and render the MP4. It carries one skill (`skills/scenivia/`) and the
connection to the Scenivia MCP server (`.mcp.json`, HTTP with OAuth). It holds
no secret.

```
/plugin marketplace add Scenivia/claude-plugin
/plugin install scenivia@scenivia
```

The first call opens the Scenivia consent page in your browser. The plugin asks
for `scenivia:read` and `scenivia:edit`; exporting needs `scenivia:render`,
granted separately. Exports spend credits only when they succeed.

Never put a token in `.mcp.json` or in a header: the OAuth flow keeps it in
Claude Code's own credential store.

Installation, scopes, tools, limits and support:
[the repository README](https://github.com/Scenivia/claude-plugin#readme).
