---
name: book-bloom-garden
description: Build or extend a reading garden where completed books become seeds, reviews sprout plants, and review likes create flowers. Use for this project's interactions, animations, sharing, or multiplayer evolution.
---

# Book Bloom Garden

Read the repository README and current implementation before editing. The starter lives at `index.html` in the repository root. Preserve the user's language and visual direction.

## Product rules

- A completed book creates a seed, not a fully grown plant.
- Saving a nonempty review creates a sprout.
- A like on a saved review adds a flower. The current prototype explicitly simulates likes; never describe them as real visitors.
- Editing an existing review preserves its existing flowers.
- Visible flower caps must not silently cap the stored count.

## Current implementation

One self-contained HTML file with inline CSS, SVG plants and JavaScript; no external assets or dependencies. Data is stored under localStorage key `bookgarden-v1`; preserve compatibility or provide a migration. User text must be inserted using textContent or equivalent escaping. Export is a local JSON download; do not claim import exists.

Use gentle animation and respect prefers-reduced-motion. Make interaction usable with keyboard and narrow screens. Keep reviews readable and distinguish saved data from unsaved edits.

## Extending to multiplayer

Choose a backend only when the user requests shared data. Specify ownership and access for gardens, reviews and likes. Authenticate writers, validate ownership server-side and enforce a unique user-review like relationship. Derive flower counts from valid likes. Never embed service credentials in client code or publish personal reading data as demo content.

Sharing a static HTML file alone does not implement multiplayer. A deployed URL alone does not prove anonymous visitors can access it: verify audience and a real browser visit. Report hosting limitations without blaming application code absent evidence.

## Verification

Exercise seed creation, empty-review rejection, first-review sprouting, subsequent review editing, like flowering and refresh persistence. Confirm export contains the saved records. For multiplayer changes additionally test two distinct users, repeated likes and unauthorized edits. State any verification that could not run.
