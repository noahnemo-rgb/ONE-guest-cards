# Registry

HASEOS sheathed-guest roster. Example row is not an invite.

No row is invited until HITL sets status to invited and names a product in products_invited.

One row per card. Status is the source of truth until HITL says otherwise.

## How to add a row

- Add a registry row in the same slice as the card file.
- Columns: id, slug, display_name, vendor, standing, status, fusion, invite_scope, review_by.
- standing is always sheathed-guest.
- fusion is always false.
- invite_scope is a list of product slugs that MAY receive a copy. Empty list means none yet.
- Do not set status to invited in the same slice that creates the card.

| id | slug | display_name | vendor | standing | status | fusion | invite_scope | review_by |
|---|---|---|---|---|---|---|---|---|
| ogc-20260912-named-helper-example | named-helper-example | Named helper (example) | — | sheathed-guest | draft | false | [] | 2026-12-11 |
| ogc-idea-forge-niche-scout | idea-forge-niche-scout | Idea Forge Niche Scout | OpenAI (API-compatible harness) | sheathed-guest | draft | false | [] | 2026-12-14 |

Never put secrets in this table.
