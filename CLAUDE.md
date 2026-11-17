# Stormlight game workspace

This repo is the shared **workspace** for two people designing a fan RPG adapted from *The Stormlight Archive*: Burooj (**B**) and Ashar (**A**). For what the game is and the layout, read `README.md`. For where the design stands, read `docs/brief.md`.

## Attribution: the core rule

Two people, who often disagree. Ashar is sceptical of AI-generated ideas: the ideas have to come from them.
- **Tag one person's view** with (B) or (A), and cite where it came from: a transcript timestamp `[MM:SS]`, an issue, or a commit.
- **Mark something as agreed** only when both have said so.
- **Bring options and questions, attributed to whoever raised them,** rather than your own recommendations. Clearly label any idea of your own as yours.

## Where things go

Create a file or folder from this list if it doesn't exist yet. Keep to this layout rather than inventing new top-level folders.
- **Decisions** → `docs/decisions.md`, newest first. Each entry gives the date, the decision, who decided it (B, A, or both), why, and a source link.
- **Design bible** → `docs/bible/`, one file per topic, e.g. `characters.md`, `combat.md`, `art-direction.md`.
- **Raw inputs** (transcripts, research notes) → `docs/sources/`, named with the date first: `YYYY-MM-DD-topic.md`.
- **Images, renders, models** → `assets/`, grouped by subject.
- **Tasks and follow-ups** → GitHub issues (`gh issue`), never a checklist file.
- **Engine and game code** → a separate game repo, not this one.

## Lore

Stormlight lore is checked against the books, with coppermind.net for lookups. When a call or an idea gets the lore wrong, record the correction next to it instead of silently fixing it. Intentional departures from the books are allowed, but list them in `docs/decisions.md`.

## Agent skills

Project skills live in `.claude/skills/`: `wayfinder`, plus the skills it calls (`grilling`, `domain-modeling`, `research`, `prototype`). They are vendored from mattpocock/skills at commit 5863806. To update, re-copy them; don't edit them in place.

### Issue tracker

GitHub Issues on this repo, via `gh`. Wayfinder maps are issues labelled `wayfinder:map`, with tickets as sub-issues. See `docs/agents/issue-tracker.md`.

### Domain docs

Single-context: `GLOSSARY.md` at the root, and decisions in `docs/decisions.md` rather than `docs/adr/`. See `docs/agents/domain.md`.
