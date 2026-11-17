# Domain Docs

How the skills (`/wayfinder`, `/domain-modeling`, `/grilling`) read and write this repo's domain documentation. Single-context layout.

## Before exploring, read these

- **`GLOSSARY.md`** at the repo root: game and Stormlight terms as *we* use them.
- **`docs/decisions.md`**: this repo's decision log. **It replaces `docs/adr/`.** Wherever a skill says "ADR", add an entry to `docs/decisions.md` instead, in the entry format given in `CLAUDE.md`, and never create `docs/adr/`.
- **`docs/brief.md`**: sources, inspirations, and each person's positions so far.

If one of these doesn't exist yet, carry on without it. `GLOSSARY.md` is created when the first term is settled.

## Use the glossary's vocabulary

When your output names a domain concept (an issue title, a ticket, a design note), use the term as `GLOSSARY.md` defines it. Lore terms follow the books (see Lore in `CLAUDE.md`). Where the game departs from them deliberately, the glossary says so.

## Flag decision conflicts

If your output contradicts an entry in `docs/decisions.md`, say so explicitly rather than silently overriding it:

> _Contradicts the 2026-11-20 decision (fixed story for the demo), but worth reopening because…_
