# ONE Guest Cards — parallel refine schema

Plane: saas. Files only. Not a runtime. Not an invite.

A card is a markdown file. Many cards may be revised in one Cursor slice.
Selecting a card ≠ fusion. Copying a card into a product ≠ fusion.
Invitation is a later HITL act on one product.

We do not run a third-party operator runtime to refine cards. Parallel here means many files in one review pass. A card’s full body is loaded only when HITL selects it. Selection ≠ fusion.

## Status

`draft` → `ready` → `invited` | `refused` | `deferred`

Only `ready` cards may be copied into a product.
Only HITL moves a card to `invited`.

## Invariants

- `fusion: false`
- `standing: sheathed-guest`
- `backends` ⊆ Puter.js, OpenRouter BYOK, Google AI Studio, NVIDIA Build
- `keys_location`: destination product env or on-device BYOK
- No secrets in this repo
- No Senior Sovereign, infant, or other-workshop ranks on a card or in product copy
- Customer surfaces still say **named helper** / **sheathed guest**, never workshop ranks
- No submodule into products; copy the one file
- One role per card

## Card fields

```yaml
id: ogc-YYYYMMDD-slug
slug: kebab-case
display_name: string
vendor: string
role: one short role
standing: sheathed-guest
fusion: false
status: draft | ready | invited | refused | deferred
backends: []
keys_location: on-device user-pays | destination-product-env
invite_scope: []          # product slugs that MAY receive a copy
products_invited: []      # filled only after HITL invite
issued: YYYY-MM-DD
review_by: YYYY-MM-DD     # ≤ 90 days from last refine
```

Body sections (required):

- Purpose
- May
- Must not
- Disclosure line (the sentence the product UI may print)
- Refuse test (how HITL or the product knows to refuse this helper)

## Rubric (every refine pass)

1. Purpose is one sentence a first-time visitor could understand.
2. May / must-not are observable, not poetic.
3. Vendor is named.
4. Backend is on the allowed list.
5. `fusion` is still `false`.
6. No keys, tokens, or hostnames from another plane.
7. Works as a helper on a checkout-adjacent product without preaching.
8. `review_by` is within 90 days.
9. Customer-facing words remain named helper / sheathed guest.

Fail any one item and the card stays `draft` or moves to `refused` / `deferred`.

## Parallel refine (one slice)

1. Read `REGISTRY.md`.
2. Open N `draft` (or due-for-review) cards.
3. Apply the rubric to each.
4. Update frontmatter dates and status.
5. Update the registry row.
6. HITL commits and pushes from the Lenovo.

Do not invite from a refine slice. Invite is a separate HITL sentence naming one card and one product.
