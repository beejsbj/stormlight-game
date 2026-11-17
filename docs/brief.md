# Stormlight game — sources & inspirations brief

Status: **early exploration** (as of 2026-11-17). Nothing below is settled unless marked *agreed*.
Primary source: the 2026-11-17 design call between Burooj (S2) and his co-designer (S1) — see
[`sources/2026-11-17-call-transcript.md`](sources/2026-11-17-call-transcript.md). Timestamps like `[23:57]` point into it.

## The idea in one paragraph

A fan-made, story-led party RPG adapting Brandon Sanderson's *The Stormlight Archive*. Both of us
are new to game development and to storytelling, so we adapt an existing story rather than invent one, and build it with
AI. Start with a demo of one section of the books; if we enjoy playing it, ask the rights holder
whether it could ever be sold. Otherwise it stays an open fan project. `[14:29]`

## Source material (what we adapt)

| Source | What we take from it | Notes |
|---|---|---|
| **The Stormlight Archive** (Brandon Sanderson) | Story, characters, world, magic system (Surges, Orders of Knights Radiant, Ideals/oaths) | *Agreed:* adapt one section of book 1 as the demo `[23:57]`. Sanderson is a JRPG fan; the books already read "gamey" `[17:27]`. |
| **Cosmere Roleplaying Game** (Brotherwise Games, official tabletop RPG; Stormlight handbook + world guide) | Ready-made translation of the books into mechanics: ability design per Surge, flora/fauna/world reference, **Ideals as level-up moments**, skeleton adventures that still allow branching | Burooj is sending links `[24:31]`. Mine for ideas; don't copy wholesale. `[17:57]` `[22:51]` `[28:27]` |
| **Coppermind wiki** (coppermind.net) | Lore lookup | Not discussed on the call; the obvious reference for agents. |

**Rights:** this is unlicensed fan work. Don't plan commercial use without Dragonsteel's permission.

## Game references: what to take, what to avoid

| Reference | Take | Avoid / caution |
|---|---|---|
| **Clair Obscur: Expedition 33** | Combat *flow* and precision; animation; cinematic quality even in gameplay; accessible to casual players `[18:20]` `[24:55]`; items reset at checkpoints (Souls-like) `[19:42]`; no character creation, menu is the start screen `[25:13]` | Party feels samey: Verso/Maelle/Gustave share move language; players ignore the unique characters' wilder kits `[30:02]–[31:51]` |
| **Final Fantasy VII Remake** | Tactical party play: you win by combining all characters' skills `[01:09]`; strongly distinct characters (Barret shoots, Aerith casts) `[27:44]` | — |
| **Persona 5** (and P3 Reload, P4 remake) | Each party member has a distinct, fixed identity `[27:14]` | Calendar structure gets formulaic `[10:11]`; consumable hoarding trivializes dungeons `[20:00]`; levelling doesn't *feel* like anything `[28:16]` |
| **Metaphor: ReFantazio** | Counter-example to the "separate battle mode" JRPG split `[00:36]` | — |
| **Divinity: Original Sin 2** | Level-up "what did I just unlock?" feeling `[21:24]`; seamless chapter transitions, more immersive than Persona/E33 `[21:36]`; environmental, world-heavy CRPG framing for a side-character-rich world `[21:02]` | Heavy branching is out of scope for two people `[22:39]` |
| **Baldur's Gate 3** | Same level-up satisfaction `[21:24]` | Overwhelming on first open; we must stay casual `[24:55]` |
| **Souls-likes / Elden Ring** | Checkpoint resets; real-time dodge as one combat option `[00:42]` | Elden Ring–grade bosses are beyond our means `[09:01]` |
| **Pragmata** (Capcom) | One niche, simple, fun signature mechanic (its hacking) beats a long feature list `[09:31]` | — |
| **God of War** | Drop straight into the game, cinematic start `[25:13]` | — |
| **Hunter × Hunter** (Nen) | Within a hard magic system, characters use powers creatively; Stormlight Surges allow the same `[32:20]` | — |
| **Greatest Estate Developer** (manhwa), Clash of Clans / FarmVille-style base building | S1's alternative pitch: build real estate projects, fight monsters in the overworld `[15:30]` | *Parked*: Burooj wasn't drawn to it `[17:05]`; Stormlight chosen `[17:24]` |

## Positions so far

*Agreed*
- Adapt the books directly; story stays mostly fixed and streamlined. Maybe a little flexibility later. `[23:32]`
- Stay casual-friendly and cinematic, like E33. `[24:55]` `[25:13]`
- Multiple playable characters, each strongly distinct. `[25:43]` `[30:43]`
- Level-ups should feel big and change how a character plays. Tie them to Radiant Ideals. `[28:27]` `[29:27]`
- No consumable hoarding; control the difficulty curve. `[20:28]`
- Prototype before theorycrafting. `[33:02]`

*Open / disputed*
- **Combat model.** Options: E33's turn-based with timed reactions; FFVII Remake's party-tactical real-time; Souls-like dodge; DOS2-style environmental turn-based. Undecided. `[00:09]–[01:39]` `[18:20]`
- **Class flexibility.** S1 wants build variety and subclasses `[26:09]` `[28:01]`. Burooj wants fixed identities: Shallan never flies `[26:55]`. Possible middle (from the Cosmere RPG): fixed Order and Surges, with a choice among abilities inside them at each level-up `[28:57]`.
- **How to use AI.** S1: ideas must come from us; learn what AI can actually do before prototyping `[05:17]` `[35:58]`. Burooj: use AI (e.g. a grilling session) as a mirror and map of what exists; explore with several cheap prototypes, find where AI struggles and build scaffolding there `[06:49]` `[36:37]`.

## First prototype (agreed scope) `[33:31]` `[37:00]`

1. **Opening scene:** Kaladin as a slave, sold into Sadeas's bridge crews (Bridge Four). The bridge crew runs into a threat: a bridge run or a chasmfiend.
2. **Environment + characters + movement** working first.
3. **Then the transition into battle**, so we can see that the full loop is possible.
4. Later: battle depth, level-up, quests.

**Who does what (as of the call):** Burooj writes the opening story and explores an AI-driven build on his
own branch of this repo. S1 builds the demo scene in **Unreal** with AI help `[34:59]`. Compare branches afterwards.

## Corrections to the transcript

- Kaladin's Windrunner Surges are **Adhesion and Gravitation**, not "gravity and friction" `[28:57]`.
- His powers come with swearing **Ideals**, not "promises" `[31:51]`. Use the books for the order in which he gains abilities. The call's version is loose.
- Shallan is a Lightweaver (Illumination + Transformation).
