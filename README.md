# ONE Guest Cards

Parallel refine schema for sheathed guest helpers.

This repository is a **roster and a workshop**. It holds markdown cards, a refine rubric, and a registry. It is not a runtime. It is not an invite. It is not the public stamp.

The public rule lives in a different repo: [ONE-trust-colophon](https://github.com/noahnemo-rgb/ONE-trust-colophon). Copy that stamp into products. Copy **one ready card** into a product only when HITL invites that helper onto that product.

Plane: `saas`  
Edition: `2026-09-12`  
Steward: Noah Nemo

## Why this is a second repo

- The colophon is a stamp. It should stay small and age by edition.
- Guest cards will grow and churn. A product should not inherit a nursery it did not invite.
- Rule vs roster. `GUEST_SHEATH.md` in the colophon is the short public rule. This repo is the catalog of cards.

## What a card is

A markdown file with YAML frontmatter. One role per file. `fusion: false` always.

Selecting a card is not identity fusion. Copying a card into a product is not identity fusion. Invitation is a later HITL act on one product.

## Status

`draft` → `ready` → `invited` | `refused` | `deferred`

Only `ready` cards may be copied. Only HITL moves a card to `invited`.

## Parallel refine

One Cursor slice may open N cards, apply `SCHEMA.md`, and update `REGISTRY.md`. That is the parallelism: many files, one review pass. No local model farm. No third-party operator runtime on this laptop.

## Tree

Files live at the repository root, not in a nested folder.

```text
SCHEMA.md                 fields + rubric
REGISTRY.md               one row per card
cards/_template.card.md
cards/examples/named-helper.example.card.md
reviews/                  dated refine notes (optional)
.cursor/rules/guest-cards.mdc
```

## Allowed backends on a card

Puter.js · OpenRouter BYOK · Google AI Studio · NVIDIA Build

Keys never live in this repo. Keys live in the destination product’s `.env` / host secrets, or on-device BYOK.

## Install into a product (later, one card)

When HITL invites:

1. Card status must be `ready`.
2. Copy that one file into the product (for example `brand/guests/<slug>.card.md`).
3. Do not submodule this repo.
4. Mark the card `invited` here and name the product slug in `products_invited`.
5. Label the helper in that product’s UI from the colophon disclosure lines.

## License

CC BY 4.0. Share and adapt with attribution to Noah Nemo and sheathed co-creators.
