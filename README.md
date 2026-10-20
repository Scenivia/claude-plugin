<p align="center">
  <a href="https://scenivia.com">
    <picture>
      <source media="(prefers-color-scheme: dark)" srcset="assets/scenivia-wordmark-dark.svg">
      <source media="(prefers-color-scheme: light)" srcset="assets/scenivia-wordmark-light.svg">
      <img alt="Scenivia" src="assets/scenivia-wordmark-light.svg" width="320">
    </picture>
  </a>
</p>

<h3 align="center">Scenivia for Claude Code</h3>

<p align="center">
  Brief, edit and export your product launch film without leaving your terminal.
</p>

<p align="center">
  <img alt="Claude Code plugin" src="https://img.shields.io/badge/Claude%20Code-plugin-1A56FF?style=flat-square">
  <img alt="MCP server over HTTP with OAuth" src="https://img.shields.io/badge/MCP-HTTP%20%2B%20OAuth-0B0F19?style=flat-square">
  <img alt="Version 1.0.0" src="https://img.shields.io/badge/version-1.0.0-555?style=flat-square">
</p>

<p align="center">
  <a href="#install">Install</a> ·
  <a href="#connect-your-account">Connect</a> ·
  <a href="#what-to-ask">What to ask</a> ·
  <a href="#tools">Tools</a> ·
  <a href="#limits-and-credits">Limits</a> ·
  <a href="#support">Support</a>
</p>

---

[Scenivia](https://scenivia.com) turns a SaaS product into a short launch or
feature film. This plugin connects Claude Code to your Scenivia account, so the
agent can work on your films with the same controls you have in the Studio.

- **Brief a film**: create a project, describe the product, its audience and
  call to action, and set the brand colours and typeface.
- **Pick a template that fits**: compare the Library templates, their story,
  length and formats, and get a preview link for the one that suits your product.
- **Edit with typed changes**: retitle a shot, swap a picture, repaint in your
  colours, change a transition. Every batch is checked before it is applied.
- **Export the MP4**: check the export for free, render it, and get a download link.

## Install

In Claude Code:

```
/plugin marketplace add Scenivia/claude-plugin
/plugin install scenivia@scenivia
```

Or from your shell:

```bash
claude plugin marketplace add Scenivia/claude-plugin
claude plugin install scenivia@scenivia
```

The plugin adds one skill and the connection to the Scenivia MCP server at
`https://api.scenivia.com/mcp`. It holds no secret.

## Connect your account

The first time the agent calls a Scenivia tool, Claude Code opens the Scenivia
consent page in your browser. Sign in as usual, choose what the agent may do,
and the browser hands the agent a token. There is nothing to copy or paste.
Run `/mcp` in Claude Code to see the connection, reconnect or sign out.

| Scope | Lets the agent |
|---|---|
| `scenivia:read` | read your projects, films, assets and exports |
| `scenivia:edit` | create projects, set briefs and brand, propose and apply edits |
| `scenivia:render` | start exports, which spend credits when they succeed |

The plugin asks for `scenivia:read` and `scenivia:edit`. Exporting needs
`scenivia:render`, which you grant separately when Scenivia asks for it on the
first export.

You can disconnect the agent at any time from **Account > Security** in
Scenivia: its token stops working at once.

> Access to the MCP server is opened account by account. Until it is open for
> yours, every call answers `404`.

## What to ask

```
Make a 30 second launch film for https://example.com in Scenivia.
```

```
Which Scenivia templates would suit a developer tool? Show me the previews.
```

```
In my "Launch week" project, change the opening title to "Ship docs in minutes".
```

```
Repaint the film in our brand colours and use the logo I uploaded.
```

```
Check that the film exports cleanly, then render it and give me the download link.
```

The agent asks before it starts an export, since an export spends credits.

## Tools

| Tool | What it does | Scope |
|---|---|---|
| `list_projects` | Lists the projects you can open, most recent first | read |
| `get_project` | Reads a project: brief, revision, shots, length, format, template | read |
| `create_project` | Creates an empty project | edit |
| `set_brief` | Sets the product, audience, goal, call to action and length | edit |
| `get_brand` | Reads the brand colours, typeface and logo | read |
| `set_brand_style` | Sets the brand colours and typeface | edit |
| `start_storyboard_job` | Writes a film from a prompt, the brief and your screenshots | edit |
| `get_storyboard_job` | Reads where the storyboard generation has got to | read |
| `list_templates` | Lists the Library templates, what each tells and for which product | read |
| `inspect_template` | Details one template: its shots, lines, pictures and limits | read |
| `find_layers` | Finds layers by shot, by on-screen word or by component | read |
| `inspect_layer` | Reads a layer and the controls that can be changed on it | read |
| `list_assets` | Lists the pictures, clips, tracks and fonts of a project | read |
| `add_asset_from_url` | Adds a public PNG, JPEG or WebP image to a project | edit |
| `list_transitions` | Lists the transitions between shots and their lengths | read |
| `list_backgrounds` | Lists the backgrounds a shot can take | read |
| `find_components` | Searches the components a new shot can be made from | read |
| `preview_component` | Shows the preview image of one component | read |
| `propose_edits` | Checks a batch of edits and returns a turn to apply, saves nothing | edit |
| `propose_structure` | Checks adding a shot at the end or removing one, saves nothing | edit |
| `apply_turn` | Applies a proposed turn, once | edit |
| `get_turn` | Reads whether a turn was applied, and at which revision | read |
| `check_export` | Says whether the film exports and what it would lose, for free | read |
| `start_render` | Renders the film to MP4 | render |
| `get_render` | Reads the status of an export | read |
| `list_renders` | Lists the exports of a project | read |
| `get_render_download` | Returns a download link, valid five minutes | read |
| `retry_render` | Renders a failed export again | render |

Arguments, outputs and JSON Schemas:
[`references/capabilities.md`](plugins/scenivia/skills/scenivia/references/capabilities.md)
and [`references/catalog.json`](plugins/scenivia/skills/scenivia/references/catalog.json).

## Limits and credits

- **Nothing is charged until an export succeeds.** A failed export costs
  nothing, and retrying it costs credits only if the retry succeeds.
- Credits are bought in Scenivia, never through the agent. When you are out of
  credits, the agent tells you and stops.
- Writing a storyboard from a prompt uses your plan's generation allowance, not credits.
- Three exports run at once per account; a fourth waits for one to end.
- 120 tool calls per minute per account. Template and component browsing is
  limited to 60 calls an hour.
- Pictures come in from a public HTTPS address (PNG, JPEG or WebP), with the
  same checks as an upload.
- Placing a template or adding and removing a shot is done in your Studio: the
  agent prepares it, and it lands when you open the project.

Every bound: [`references/limits.md`](plugins/scenivia/skills/scenivia/references/limits.md).

## When something goes wrong

| What you see | What to do |
|---|---|
| `401` on every call | The connection expired or was revoked. Run `/mcp` and reconnect. |
| `insufficient_scope` | The tool needs a scope you did not grant, often `scenivia:render`. |
| `stale_revision` | The film changed since it was read, often in the Studio. The agent reads it again. |
| `awaiting_studio` | Not an error: open the project in the Studio and the change lands there. |
| `requires_open_studio` | The change was prepared in the Studio chat; apply it in the Studio. |
| `insufficient_credits` | Buy credits in Scenivia, then ask again. |

Every code and what to do about it:
[`references/errors.md`](plugins/scenivia/skills/scenivia/references/errors.md).

## Support

- Website: [scenivia.com](https://scenivia.com)
- Email: [support@scenivia.com](mailto:support@scenivia.com)

## License

Free to install and use with Scenivia, commercial work included. See [LICENSE](LICENSE).
