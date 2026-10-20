# Worked sequences

Each step names the tool and the one fact to carry to the next.

## Choose a template

1. `list_templates { usage: "launch" }` (or `feature`, `format: "9:16"`): read
   each `productKind` and `story`, and keep the two or three whose story is
   true of the product.
2. `inspect_template { template }` on each: `fitsNot` rules a template out;
   `shots` says what each shot shows and the lines (`maxChars`, `maxLines`)
   and pictures it takes, so you know the product has enough to fill it.
3. Give the person the `preview.video` link of your pick and one sentence on
   why. They place it from the Studio's Templates tab.
4. `get_project`: `studio.template` names it once placed.

## Retitle the opening shot

1. `get_project { projectId }`: keep `project.studio.revision`.
2. `find_layers { projectId, shot: 1 }`: pick the layer whose `text` is the title.
3. `inspect_layer { projectId, layerId }`: find the `text-content` control's `field`.
4. `propose_edits { projectId, baseRevision, intent, operations: [{ type: "setText", layerId, field, value }] }`:
   read `fit` (a line too wide for its box) and `exportLosses` before going on.
5. `apply_turn { projectId, turnId }`: keep `appliedRevision` as the next `baseRevision`.

On a film made from a template, `inspect_layer` lists only the template's
places, each with its limits; a change outside them comes back
`rejected_operation` with the limit in `message`.

## Repaint a film in the brand colours

1. `get_brand { projectId }` for the three colours (ground, accent, ink).
2. `find_layers { projectId }` returns 12 layers at most; when `omitted` is not
   zero, ask again shot by shot (`shot: 1`, `shot: 2`, ...) until every layer is read.
3. `inspect_layer` on each layer, keeping its `color` controls.
4. One `propose_edits` batch of `setColor` operations (32 at most), then `apply_turn`.

## Place the person's logo

1. `list_assets { projectId }`: a picture of `kind: "image"`, usually small and square.
2. `inspect_layer` to find an `image` or `asset` control.
3. `propose_edits` with `setAsset` and the asset `id`. A URL or a `data:` URI is refused.

A logo that is not in the project yet: `add_asset_from_url { projectId, url }`
with its public HTTPS address first, then use the `id` it returns.

## Join two shots with a transition

1. `list_transitions` for the names and the three lengths.
2. `propose_edits` with `{ type: "setTransition", scene: 2, transition: "whip-pan-right", length: "short" }`
   (the passage INTO shot 2), then `apply_turn`. `transition: null` cuts.

## Add or remove a shot

1. `find_components { query }` for a component and its text fields.
2. `propose_structure { projectId, baseRevision, intent, operations: [{ type: "addShot", component, text }] }`.
3. `apply_turn`: the answer is `awaiting_studio`. Tell the person the Studio
   performs it when the project is open, then poll `get_turn` until
   `appliedRevision` is set before the next change.

## Export and fetch the file

1. `check_export { projectId }`: `blocked` says why; `ready` gives `playedSeconds` and `notes`.
2. `start_render { projectId, baseRevision }` with the `scenivia:render` scope.
3. `get_render` every 15 to 30 seconds until `succeeded` or `failed`.
4. `get_render_download`: the link lasts five minutes; ask again rather than keep it.
5. On `failed`, `retry_render { projectId, renderId }` redraws the film as it stands.
