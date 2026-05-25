# Closet Contract

Closet root path:

`<USER_CONFIGURED_CLOSET_ROOT>`

Ask the user for this path before reading or editing files if it is not already known.

## Canonical Files

- `FashionCloset.md`: living manual and system overview.
- `Fashion Closet.md`: MOC and user entry point.
- `About Me.md`: body, sizing, colors, lifestyle, silhouette rules.
- `Beliefs.md`: personal style modes, heritage, values, style rules.
- `Triage.md`: hang, fold/store, undecided, let-go categories.
- `_Item Template.md`: base for new item notes.
- `Closet Inventory/_index.md`: master item list, next numeric ID, next shoe ID.
- `Closet Inventory/_basics-overview.md`: basics that do not need individual IDs.
- `Outfits/_index.md`: outfit log index.

## ID Rules

- Clothes use numeric IDs: `01`, `02`, `03`, ...
- Shoes use `X` IDs: `X1`, `X2`, `X3`, ...
- IDs are immutable and never reused.
- Photos live in `assets/{ID}.jpg` or clear variants such as `{ID}-label.jpg`.
- Check `Closet Inventory/_index.md` before assigning a new ID.
- Basics do not get individual IDs unless they have a strong story or distinct role.

## Item Note Requirements

Use `_Item Template.md`. Preserve these frontmatter dimensions:

- `id`
- `type`
- `color`
- `secondary`
- `fabric`
- `texture`
- `pattern`
- `fit`
- `style`
- `season`
- `mode`
- `status`
- `acquired`
- `brand`
- `size`
- `tags`

Rules:

- `fabric` is composition. `texture` is surface feel. `fit` is how it sits. `style` is the garment design type.
- Do not add a separate `material` field.
- Unknown composition should be `TBD` or visual inference, not blank.
- Include description, story, when to wear, pairings, care, and status.

## Outfit Advice Rules

- Read `About Me.md`, `Beliefs.md`, and inventory before recommending.
- Ask for occasion, weather, mode, movement needs, and must-wear items when missing.
- Use owned pieces first.
- Explain through silhouette, color, mode, season, comfort, and story.
- Respect the user's documented constraints: proportions, color preferences, style modes, climate, lifestyle, comfort, and movement needs.

## Write Safety

- Draft first unless the user explicitly asks to edit the live vault.
- Do not overwrite item notes, indexes, or outfit logs without confirming the target file.
- When editing, keep the user's existing wiki-link or Markdown-link style intact.
- Preserve bilingual or mixed-language style when present.
