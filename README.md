<div align="center">

<a href="https://scenivia.com">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="assets/scenivia-wordmark-dark.svg">
    <source media="(prefers-color-scheme: light)" srcset="assets/scenivia-wordmark-light.svg">
    <img alt="Scenivia" src="assets/scenivia-wordmark-light.svg" width="260">
  </picture>
</a>

### Your product launch film, made from your AI coding agent

Brief it, pick a template, edit every shot and export the MP4,
without leaving your editor.

<p>
  <img alt="MCP server" src="https://img.shields.io/badge/MCP-HTTP_%C2%B7_OAuth-0B0F19?style=flat&logo=modelcontextprotocol&logoColor=white">
  <img alt="Claude Code plugin" src="https://img.shields.io/badge/Claude_Code-plugin-D97757?style=flat&logo=claude&logoColor=white">
  <a href="LICENSE"><img alt="License: free to use" src="https://img.shields.io/badge/license-free_to_use-1A56FF?style=flat"></a>
</p>

<p>
  <a href="#install"><img alt="Add to Claude Code" src="https://img.shields.io/badge/Add_to-Claude_Code-D97757?style=for-the-badge&logo=claude&logoColor=white&labelColor=1F1F1F"></a>
  <a href="https://cursor.com/en/install-mcp?name=scenivia&config=eyJ1cmwiOiAiaHR0cHM6Ly9hcGkuc2Nlbml2aWEuY29tL21jcCJ9"><img alt="Add to Cursor" src="https://img.shields.io/badge/Add_to-Cursor-000000?style=for-the-badge&logo=cursor&logoColor=white&labelColor=1F1F1F"></a>
  <a href="https://insiders.vscode.dev/redirect/mcp/install?name=scenivia&config=%7B%22type%22%3A%22http%22%2C%22url%22%3A%22https%3A%2F%2Fapi.scenivia.com%2Fmcp%22%7D"><img alt="Install in VS Code" src="https://img.shields.io/badge/Install_in-VS_Code-007ACC?style=for-the-badge&logo=data%3Aimage%2Fsvg%2Bxml%3Bbase64%2CPHN2ZyBmaWxsPSJ3aGl0ZSIgcm9sZT0iaW1nIiB2aWV3Qm94PSIwIDAgMjQgMjQiIHhtbG5zPSJodHRwOi8vd3d3LnczLm9yZy8yMDAwL3N2ZyI%2BPHRpdGxlPlZpc3VhbCBTdHVkaW8gQ29kZTwvdGl0bGU%2BPHBhdGggZD0iTTIzLjE1IDIuNTg3TDE4LjIxLjIxYTEuNDk0IDEuNDk0IDAgMCAwLTEuNzA1LjI5bC05LjQ2IDguNjMtNC4xMi0zLjEyOGEuOTk5Ljk5OSAwIDAgMC0xLjI3Ni4wNTdMLjMyNyA3LjI2MUExIDEgMCAwIDAgLjMyNiA4Ljc0TDMuODk5IDEyIC4zMjYgMTUuMjZhMSAxIDAgMCAwIC4wMDEgMS40NzlMMS42NSAxNy45NGEuOTk5Ljk5OSAwIDAgMCAxLjI3Ni4wNTdsNC4xMi0zLjEyOCA5LjQ2IDguNjNhMS40OTIgMS40OTIgMCAwIDAgMS43MDQuMjlsNC45NDItMi4zNzdBMS41IDEuNSAwIDAgMCAyNCAyMC4wNlYzLjkzOWExLjUgMS41IDAgMCAwLS44NS0xLjM1MnptLTUuMTQ2IDE0Ljg2MUwxMC44MjYgMTJsNy4xNzgtNS40NDh2MTAuODk2eiIvPjwvc3ZnPg%3D%3D&labelColor=1F1F1F"></a>
  <a href="#chatgpt"><img alt="Connect to ChatGPT" src="https://img.shields.io/badge/Connect_to-ChatGPT-10A37F?style=for-the-badge&logo=data%3Aimage%2Fsvg%2Bxml%3Bbase64%2CPHN2ZyBmaWxsPSJ3aGl0ZSIgcm9sZT0iaW1nIiB2aWV3Qm94PSIwIDAgMjQgMjQiIHhtbG5zPSJodHRwOi8vd3d3LnczLm9yZy8yMDAwL3N2ZyI%2BPHRpdGxlPk9wZW5BSTwvdGl0bGU%2BPHBhdGggZD0iTTIyLjI4MTkgOS44MjExYTUuOTg0NyA1Ljk4NDcgMCAwIDAtLjUxNTctNC45MTA4IDYuMDQ2MiA2LjA0NjIgMCAwIDAtNi41MDk4LTIuOUE2LjA2NTEgNi4wNjUxIDAgMCAwIDQuOTgwNyA0LjE4MThhNS45ODQ3IDUuOTg0NyAwIDAgMC0zLjk5NzcgMi45IDYuMDQ2MiA2LjA0NjIgMCAwIDAgLjc0MjcgNy4wOTY2IDUuOTggNS45OCAwIDAgMCAuNTExIDQuOTEwNyA2LjA1MSA2LjA1MSAwIDAgMCA2LjUxNDYgMi45MDAxQTUuOTg0NyA1Ljk4NDcgMCAwIDAgMTMuMjU5OSAyNGE2LjA1NTcgNi4wNTU3IDAgMCAwIDUuNzcxOC00LjIwNTggNS45ODk0IDUuOTg5NCAwIDAgMCAzLjk5NzctMi45MDAxIDYuMDU1NyA2LjA1NTcgMCAwIDAtLjc0NzUtNy4wNzI5em0tOS4wMjIgMTIuNjA4MWE0LjQ3NTUgNC40NzU1IDAgMCAxLTIuODc2NC0xLjA0MDhsLjE0MTktLjA4MDQgNC43NzgzLTIuNzU4MmEuNzk0OC43OTQ4IDAgMCAwIC4zOTI3LS42ODEzdi02LjczNjlsMi4wMiAxLjE2ODZhLjA3MS4wNzEgMCAwIDEgLjAzOC4wNTJ2NS41ODI2YTQuNTA0IDQuNTA0IDAgMCAxLTQuNDk0NSA0LjQ5NDR6bS05LjY2MDctNC4xMjU0YTQuNDcwOCA0LjQ3MDggMCAwIDEtLjUzNDYtMy4wMTM3bC4xNDIuMDg1MiA0Ljc4MyAyLjc1ODJhLjc3MTIuNzcxMiAwIDAgMCAuNzgwNiAwbDUuODQyOC0zLjM2ODV2Mi4zMzI0YS4wODA0LjA4MDQgMCAwIDEtLjAzMzIuMDYxNUw5Ljc0IDE5Ljk1MDJhNC40OTkyIDQuNDk5MiAwIDAgMS02LjE0MDgtMS42NDY0ek0yLjM0MDggNy44OTU2YTQuNDg1IDQuNDg1IDAgMCAxIDIuMzY1NS0xLjk3MjhWMTEuNmEuNzY2NC43NjY0IDAgMCAwIC4zODc5LjY3NjVsNS44MTQ0IDMuMzU0My0yLjAyMDEgMS4xNjg1YS4wNzU3LjA3NTcgMCAwIDEtLjA3MSAwbC00LjgzMDMtMi43ODY1QTQuNTA0IDQuNTA0IDAgMCAxIDIuMzQwOCA3Ljg3MnptMTYuNTk2MyAzLjg1NThMMTMuMTAzOCA4LjM2NCAxNS4xMTkyIDcuMmEuMDc1Ny4wNzU3IDAgMCAxIC4wNzEgMGw0LjgzMDMgMi43OTEzYTQuNDk0NCA0LjQ5NDQgMCAwIDEtLjY3NjUgOC4xMDQydi01LjY3NzJhLjc5Ljc5IDAgMCAwLS40MDctLjY2N3ptMi4wMTA3LTMuMDIzMWwtLjE0Mi0uMDg1Mi00Ljc3MzUtMi43ODE4YS43NzU5Ljc3NTkgMCAwIDAtLjc4NTQgMEw5LjQwOSA5LjIyOTdWNi44OTc0YS4wNjYyLjA2NjIgMCAwIDEgLjAyODQtLjA2MTVsNC44MzAzLTIuNzg2NmE0LjQ5OTIgNC40OTkyIDAgMCAxIDYuNjgwMiA0LjY2ek04LjMwNjUgMTIuODYzbC0yLjAyLTEuMTYzOGEuMDgwNC4wODA0IDAgMCAxLS4wMzgtLjA1NjdWNi4wNzQyYTQuNDk5MiA0LjQ5OTIgMCAwIDEgNy4zNzU3LTMuNDUzN2wtLjE0Mi4wODA1TDguNzA0IDUuNDU5YS43OTQ4Ljc5NDggMCAwIDAtLjM5MjcuNjgxM3ptMS4wOTc2LTIuMzY1NGwyLjYwMi0xLjQ5OTggMi42MDY5IDEuNDk5OHYyLjk5OTRsLTIuNTk3NCAxLjQ5OTctMi42MDY3LTEuNDk5N1oiLz48L3N2Zz4%3D&labelColor=1F1F1F"></a>
  <a href="#windsurf"><img alt="Add to Windsurf" src="https://img.shields.io/badge/Add_to-Windsurf-0B100F?style=for-the-badge&logo=windsurf&logoColor=white&labelColor=1F1F1F"></a>
</p>

[Install](#install) · [Other apps](#use-it-in-other-apps) · [Connect](#connect-your-account) · [What to ask](#what-to-ask) · [Tools](#tools) · [Limits](#limits-and-credits) · [Support](#support)

</div>

---

## Why

[Scenivia](https://scenivia.com) turns a SaaS product into a short launch or
feature film, built from a catalogue of designed templates you stay in control
of. This plugin gives Claude Code the same controls you have in the Studio.

<table>
  <tr>
    <td width="50%" valign="top">
      <h4>Brief the film</h4>
      Create a project, describe the product, its audience and call to action,
      and set your brand colours and typeface.
    </td>
    <td width="50%" valign="top">
      <h4>Pick the right template</h4>
      Compare the Library templates, what each one tells and for which product,
      with a preview, before choosing.
    </td>
  </tr>
  <tr>
    <td width="50%" valign="top">
      <h4>Edit every shot</h4>
      Retitle a shot, swap a picture, repaint in your colours, change a
      transition. Every batch is checked before it is applied.
    </td>
    <td width="50%" valign="top">
      <h4>Export the MP4</h4>
      Check the export for free, render it in 16:9, 1:1 or 9:16, and get a
      download link.
    </td>
  </tr>
</table>

## Install

Three steps, about a minute.

**1. Add the marketplace and install the plugin** in Claude Code:

```text
/plugin marketplace add Scenivia/claude-plugin
/plugin install scenivia@scenivia
```

**2. Ask for a film.** The first Scenivia call opens the consent page in your
browser: sign in, choose what the agent may do, done.

**3. Watch it come together** in your Scenivia Studio, and export when you like it.

<details>
<summary>From your shell instead</summary>

```bash
claude plugin marketplace add Scenivia/claude-plugin
claude plugin install scenivia@scenivia
```

</details>

The plugin adds one skill and the connection to the Scenivia MCP server at
`https://api.scenivia.com/mcp`. It holds no secret.

## Use it in other apps

The same server works in any app that speaks MCP over HTTP with OAuth. The
address is always `https://api.scenivia.com/mcp`; the consent page opens on
first use, exactly as in Claude Code.

<a id="claude-code"></a>

<details open>
<summary><b>Claude Code</b>, the server alone, without the plugin's skill</summary>

```bash
claude mcp add --transport http scenivia https://api.scenivia.com/mcp
```

</details>

<details>
<summary><b>Cursor</b></summary>

Click **Add to Cursor** above, or add this to `~/.cursor/mcp.json`:

```json
{ "mcpServers": { "scenivia": { "url": "https://api.scenivia.com/mcp" } } }
```

</details>

<details>
<summary><b>VS Code</b></summary>

Click **Install in VS Code** above, or add this to `.vscode/mcp.json`:

```json
{ "servers": { "scenivia": { "type": "http", "url": "https://api.scenivia.com/mcp" } } }
```

</details>

<details>
<summary><b>Claude</b> (claude.ai and the desktop app)</summary>

**Settings › Connectors › Add custom connector**, name it Scenivia and paste
`https://api.scenivia.com/mcp`. Custom connectors depend on your Claude plan.

</details>

<a id="chatgpt"></a>

<details>
<summary><b>ChatGPT</b></summary>

Turn on **developer mode** in **Settings › Apps & Connectors › Advanced**, then
**Create** a connector with the URL `https://api.scenivia.com/mcp` and OAuth.
MCP connectors depend on your ChatGPT plan.

</details>

<a id="windsurf"></a>

<details>
<summary><b>Windsurf</b> and other MCP clients</summary>

Add a remote server with the URL `https://api.scenivia.com/mcp`. In Windsurf,
in `~/.codeium/windsurf/mcp_config.json`:

```json
{ "mcpServers": { "scenivia": { "serverUrl": "https://api.scenivia.com/mcp" } } }
```

</details>

## Connect your account

There is nothing to copy or paste: Claude Code opens the Scenivia consent page
and the browser hands the agent its token. Run `/mcp` to see the connection,
reconnect or sign out.

| Scope | Lets the agent |
|---|---|
| `scenivia:read` | read your projects, films, assets and exports |
| `scenivia:edit` | create projects, set briefs and brand, propose and apply edits |
| `scenivia:render` | start exports, which spend credits only when they succeed |

The plugin asks for `read` and `edit`. Exporting needs `render`, which you grant
when Scenivia asks for it on the first export. Disconnect the agent at any time
from **Account › Security**: its token stops working at once.

> [!NOTE]
> Access to the MCP server is opened account by account. Until it is open for
> yours, every call answers `404`.

## What to ask

```text
Make a 30 second launch film for https://example.com in Scenivia, from a template.

Which Scenivia templates would suit a developer tool? Show me the previews.

In my "Launch week" project, change the opening title to "Ship docs in minutes".

Repaint the film in our brand colours and use the logo I uploaded.

Check that the film exports cleanly, then render it and give me the link.
```

The agent always asks before it starts an export, since an export spends credits.

## Tools

32 tools, grouped by what they work on.

<details>
<summary><b>Projects and brief</b> · 7 tools</summary>

| Tool | What it does | Scope |
|---|---|---|
| `list_projects` | Lists the projects you can open, most recent first | read |
| `get_project` | Reads a project: brief, revision, shots, length, format, template | read |
| `create_project` | Creates an empty project | edit |
| `set_brief` | Sets the product, audience, goal, call to action and length | edit |
| `get_brand` | Reads the brand colours, typeface and logo | read |
| `set_brand_style` | Sets the brand colours and typeface | edit |
| `start_storyboard_job` · `get_storyboard_job` | The fallback when no template fits: writes a free film from a prompt with Scenivia's AI, and reads its progress | edit · read |

</details>

<details>
<summary><b>Templates, components and assets</b> · 10 tools</summary>

| Tool | What it does | Scope |
|---|---|---|
| `list_templates` | Lists the Library templates, what each tells and for which product | read |
| `inspect_template` | Details one template: every place, its width and limits, the template's example line | read |
| `list_library` | Lists the music by mood and the sound effects by family | read |
| `find_components` | Searches the components a new shot can be made from | read |
| `preview_component` | Shows the preview image of one component | read |
| `list_transitions` | Lists the transitions between shots and their lengths | read |
| `list_backgrounds` | Lists the backgrounds a shot can take | read |
| `list_assets` | Lists the pictures, clips, tracks and fonts of a project | read |
| `add_asset_from_url` | Adds a public PNG, JPEG or WebP image to a project | edit |
| `find_layers` · `inspect_layer` | Finds layers by shot, word or component, and reads their controls | read |

</details>

<details>
<summary><b>Edits</b> · 7 tools</summary>

| Tool | What it does | Scope |
|---|---|---|
| `use_template` | Makes the film from a template with every line written by the agent, no AI generation spent | edit |
| `propose_edits` | Checks a batch of edits and returns a turn to apply, saves nothing | edit |
| `edit_film` | Changes the brand name, logo, font, music, effects, narrator and format | edit |
| `compose_screen` | Experimental: draws one bounded product screen from blocks, when no screenshot exists | edit |
| `propose_structure` | Checks adding a shot at the end or removing one, saves nothing | edit |
| `apply_turn` | Applies a proposed turn, once | edit |
| `get_turn` | Reads whether a turn was applied, and at which revision | read |

</details>

<details>
<summary><b>Export</b> · 6 tools</summary>

| Tool | What it does | Scope |
|---|---|---|
| `check_export` | Says whether the film exports and what it would lose, for free | read |
| `start_render` | Renders the film to MP4 | render |
| `get_render` · `list_renders` | Reads the status of one export, or lists a project's exports | read |
| `get_render_download` | Returns a download link, valid five minutes | read |
| `retry_render` | Renders a failed export again | render |

</details>

Arguments, outputs and JSON Schemas:
[`capabilities.md`](plugins/scenivia/skills/scenivia/references/capabilities.md) ·
[`catalog.json`](plugins/scenivia/skills/scenivia/references/catalog.json)

## Limits and credits

> [!TIP]
> **Nothing is charged until an export succeeds.** A failed export costs
> nothing, and a retry costs credits only if it succeeds.

- Credits are bought in Scenivia, never through the agent. Out of credits, the agent says so and stops.
- Writing a storyboard from a prompt uses your plan's generation allowance, not credits.
- Three exports run at once per account; a fourth waits for one to end.
- 120 tool calls a minute per account; template and component browsing, 60 calls an hour.
- Pictures come in from a public HTTPS address (PNG, JPEG or WebP), with the same checks as an upload.
- Placing a template, or adding and removing a shot, lands in your Studio: the agent prepares it, you see it when you open the project.

Every bound: [`limits.md`](plugins/scenivia/skills/scenivia/references/limits.md)

<details>
<summary><b>When something goes wrong</b></summary>

| What you see | What to do |
|---|---|
| `401` on every call | The connection expired or was revoked. Run `/mcp` and reconnect. |
| `insufficient_scope` | The tool needs a scope you did not grant, often `scenivia:render`. |
| `stale_revision` | The film changed since it was read, often in the Studio. The agent reads it again. |
| `awaiting_studio` | Not an error: open the project in the Studio and the change lands there. |
| `requires_open_studio` | The change was prepared in the Studio chat; apply it in the Studio. |
| `insufficient_credits` | Buy credits in Scenivia, then ask again. |

Every code: [`errors.md`](plugins/scenivia/skills/scenivia/references/errors.md)

</details>

## Support

Questions, a bug, an idea: **[support@scenivia.com](mailto:support@scenivia.com)** · [scenivia.com](https://scenivia.com)

## License

Free to install and use with Scenivia, commercial work included. See [LICENSE](LICENSE).
