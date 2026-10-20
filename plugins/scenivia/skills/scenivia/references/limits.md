# Bounds and what the server does not do

## Bounds

- 120 tool calls per minute per person, across every tool; some tools have
  their own, tighter, limits, and a refusal then says when to retry.
- `propose_edits`: 1 to 32 operations, text values up to 4000 characters.
- `propose_structure`: up to 8 shot changes, added at the end or removed; never reordered.
- `setTransition`: into shot 2 or later, `short`, `medium` (default) or `long`,
  refused when the passage would take more than half of either shot.
- `find_layers` returns 12 layers at most and says how many it left out;
  `list_assets` 100, `list_renders` 50, `find_components` 8.
- The catalogue tools (`list_templates`, `inspect_template`,
  `find_components`, `preview_component`, `list_backgrounds`,
  `list_transitions`) share 60 calls an hour per person: enough to make
  films, not to copy the catalogue.
- `inspect_template` lists 12 lines a shot at most and counts the rest in
  `omittedLines`.
- Three exports run at once per person; a fourth is refused until one ends.
- An access token lasts one hour, a refresh token thirty days and rotates on use.

## What the server does not do

- No direct write of the film: every change goes through a typed proposal.
  No undo history.
- No camera edit: the export does not use one, so none is offered.
- Shot changes are performed by the person's Studio, not by the server: they
  wait (`awaiting_studio`) until the project is open, for a day at most, and a
  turn prepared on an older revision is never performed.
- Pictures come in from a public HTTPS address only (PNG, JPEG, WebP), with
  the same checks and limits as an upload; private and local addresses are
  refused.
- No storyboard or template placed over MCP: a generated storyboard is
  offered to the person the next time they open the project, and a template
  is placed from the Studio's Templates tab.
- No credit purchase, plan change or payment of any kind.
