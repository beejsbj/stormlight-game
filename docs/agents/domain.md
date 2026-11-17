# Domain Docs

How the skills (`/wayfinder`, `/domain-modeling`, `/grilling`) read and write this repo's domain documentation. Single-context layout.

## Before exploring, read these

- **`GLOSSARY.md`** at the repo root: game and Stormlight terms as *we* use them.
- **`docs/adr/`**: read the ADRs that touch the area you're working in. Each one names who decided it (B, A, or both).
- **`docs/brief.md`**: sources, inspirations, and each person's positions so far.

If one of these doesn't exist yet, carry on without it. `/domain-modeling` creates `GLOSSARY.md` and `docs/adr/` when the first term or decision is settled.

## Use the glossary's vocabulary

When your output names a domain concept (an issue title, a ticket, a design note), use the term as `GLOSSARY.md` defines it. Lore terms follow the books (see Lore in `CLAUDE.md`). Where the game departs from them deliberately, the glossary says so.

## Flag ADR conflicts

If your output contradicts an existing ADR, say so explicitly rather than silently overriding it:

> _Contradicts ADR-0002 (fixed story for the demo), but worth reopening because…_
