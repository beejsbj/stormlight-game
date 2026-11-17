# Stormlight game — sources & inspirations brief

Status: **early exploration** (as of 2026-11-17). Nothing below is settled unless marked *agreed*.

**Primary source:** the 2026-11-17 design call between Burooj (**B**, S2 in the transcript) and his co-designer (**S1**). The transcript is at [`sources/2026-11-17-call-transcript.md`](sources/2026-11-17-call-transcript.md). Timestamps like `[23:57]` point into it. A cleaner Gemini transcript may replace it, and if so the timestamps may shift slightly.

**Read this first if you're planning from this brief:**
- Whatever you produce goes back to S1 for his reaction `[38:03]`.
- S1 is sceptical of AI-generated ideas. In his view, the ideas have to come from the two of them `[05:17]` `[06:46]`.
- So present options with who held which view, rather than recommendations. Tags like (B) or (S1) mark whose view a line is. Untagged lines are views both of them shared.

## The idea in one paragraph

A fan-made, story-led party RPG adapting Brandon Sanderson's *The Stormlight Archive*. Both of us are new to game development and to storytelling, so we adapt an existing story rather than invent one, and build it with AI help `[14:29]`. Start with a demo of one section of the books. If we enjoy playing it, ask Brandon whether it could ever be sold `[14:59]`. Otherwise it stays an open fan project.

## Source material (what we adapt)

| Source | What we take from it | Notes |
|---|---|---|
| **The Stormlight Archive** (Brandon Sanderson) | Story, characters, world, magic system: Surges, Orders of Knights Radiant, Ideals | *Agreed:* adapt one section of the books as the demo `[23:57]`. Given the proposed opening, likely from *The Way of Kings* (book 1). B: the books already feel JRPG-like, and Sanderson is a JRPG fan `[17:27]`. |
| **Cosmere Roleplaying Game** (Brotherwise Games, the official tabletop RPG, with a Stormlight handbook and world guide) | It already turns the books into game mechanics: ability design per Surge, flora and fauna and world reference, starter adventures that still allow branching | B is sending S1 links `[24:31]`. Mine it for ideas; don't copy it wholesale `[17:57]` `[22:51]`. B's claim that it makes swearing an Ideal a big level-up moment is **secondhand** ("from what I've heard") `[28:27]`. Check it in the handbook. |
| **Coppermind wiki** (coppermind.net) | Lore lookup | Not discussed on the call. It's the obvious reference for agents. |

### Lore corrections to the transcript

Read these before the opening-scene section below.
- Kaladin's Windrunner Surges are **Adhesion and Gravitation**, not "gravity and friction" `[28:57]`.
- Kaladin gains powers by swearing **Ideals**, not "promises".
- The order on the call, "first the spear, then flying" `[31:51]`, is roughly backwards:
  - In book 1 he uses Stormlight and Lashings, and swears the Second Ideal near the end.
  - Syl becomes a Shardblade or Shardspear when he swears the Third Ideal, in book 2.
- Shallan is a Lightweaver: Illumination and Transformation.
- The book's opening structure:
  - *The Way of Kings* does **not** open on Kaladin. It opens with the Prelude, then Szeth killing Gavilar, then Cenn in Amaram's army.
  - Kaladin as a slave starts in chapter 2.
  - On bridge runs the danger is **Parshendi archers**. Bridge Four meets a chasmfiend in the chasms in book 2, not book 1.

## Game references: what to take, what to avoid

B, S1 and an unnamed environment-based turn-based game were proposed as the main points to steer by `[19:26]`. B's three are FFVII Remake, Expedition 33, and an environment-based turn-based game, probably DOS2. S1 asked "do you mean Divinity?" `[20:56]`, so even he wasn't sure.

| Reference | Take | Avoid / caution |
|---|---|---|
| **Clair Obscur: Expedition 33** | Combat flow and timing precision (B `[19:26]`); animation (S1 `[19:23]`); cinematic feel even in gameplay (B `[30:15]`); casual players got into it (S1 `[24:55]`); items refill at checkpoints, as in Souls-likes (S1 `[19:42]`); no character creation, the menu is the start screen (B `[25:13]`) | Party feels samey: Verso, Maelle and Gustave share a moveset, and players ignore the unique characters' wilder kits (`[30:02]`–`[31:51]`). Levelling doesn't *feel* like anything (S1 `[28:16]`). |
| **Final Fantasy VII Remake** | Tactical party play: you win by combining every character's skills (B `[01:09]`); clearly distinct characters, e.g. Barret shoots and Aerith casts (B `[27:44]`) | — |
| **Persona 5** | Each party member has a distinct, fixed identity (B `[27:14]`) | Calendar structure gets formulaic; S1 couldn't get into the P3 remake (S1 `[10:11]`). Hoarded consumables make dungeons trivial (`[20:00]`–`[20:28]`). Levelling doesn't feel like anything (S1 `[28:16]`). |
| **Metaphor: ReFantazio** | S1 cited it to argue that a JRPG need not separate exploration from battle `[00:36]`. Note: it still has turn-based battles. It adds real-time field attacks on weaker enemies, so it's a hybrid. | — |
| **Divinity: Original Sin 2** | The "what did I just unlock?" level-up feeling (S1 `[21:24]`). Chapters flow into each other more smoothly than in Persona or E33 (B `[21:36]`). A world-heavy CRPG fits a story with many side characters (B `[21:02]`). | S1: that smoothness comes from branching, and we can't afford branching with two people `[22:16]`–`[22:39]`. |
| **Baldur's Gate 3** | Same level-up satisfaction (S1 `[21:24]`) | Overwhelming the first time you open it; we must stay casual (S1 `[24:55]`) |
| **Souls-likes / Elden Ring** | Checkpoint resets; real-time dodging as one possible combat model `[00:42]` | Elden Ring–grade bosses are beyond us (S1 `[09:01]`) |
| **Pragmata** (Capcom) | A niche but simple mechanic that's fun, its hacking (S1 `[09:31]`). Aim for "what can be done in a simple way while also pushing some boundaries" (S1 `[09:01]`). | — |
| **God of War** | Drop the player straight into the game (B `[25:13]`) | — |
| **Hunter × Hunter** (Nen) | Inside a hard magic system, users get creative with their powers, and Surges allow the same (B `[32:20]`) | — |
| **Greatest Estate Developer** (manhwa), plus base building like Clash of Clans or FarmVille ("farmwheel" in the transcript is a guess) | S1's alternative pitch: build real estate projects, fight monsters in the overworld `[15:30]`–`[16:59]` | *Parked*: B wasn't drawn to it `[17:05]`, and S1 agreed to start with Stormlight `[17:24]`. |

## Positions so far

*Agreed*
- Adapt the books directly. For the demo, follow one section of the books closely (S1 `[23:57]`, with B's agreement). Later they may "retcon it… [and] be like this is our story" (S1 `[24:06]`). That means taking the story their own way later, not building branches.
- Stay casual-friendly and cinematic, like E33 (`[24:55]` `[25:13]`).
- Level-ups should feel big. That's S1's complaint about E33 and Persona `[28:16]`, and B agrees `[21:36]`.
- No hoarding consumables; keep control of the difficulty curve `[20:00]`–`[20:28]`.
- Build a small skeleton or prototype before theorising further (S1 `[33:02]`, B `[33:26]`).
- Multiple playable characters, each clearly distinct. B argues for it `[25:43]` `[30:43]`. S1's agreement is implied by his E33-feels-samey criticism `[30:56]`, though he also wants build variety. See below.

*Proposed by one side, no answer yet*
- (B) Tie level-ups to swearing Radiant Ideals, so a level-up can change how a character plays `[28:27]`–`[29:27]`.
- (B) Give the game modes or systems that push players to use each character's wilder abilities. This is the fix for E33 feeling samey `[31:51]`.
- (B) With AI, cost is no constraint, so characters can change drastically `[29:27]`. **This is an assumption. Nobody has tested it.**

*Open / disputed*
- **Combat model.** Options: E33's turn-based with timed reactions; FFVII Remake's real-time party tactics; Souls-like dodging; DOS2-style turn-based play built on the environment. Undecided `[00:09]`–`[01:39]` `[18:20]`.
- **Class flexibility.**
  - S1 wants build variety: switch class at level-up, or at least subclasses `[26:09]` `[28:01]`.
  - B wants fixed identities: "Shallan won't suddenly start flying" `[26:55]`. Within that, B suggests a choice of abilities inside a character's Surges at each level-up `[28:57]`.
- **Does it need to be new?**
  - B: use AI to map what's already been done, so we can find the new space (`[07:19]` `[07:49]`).
  - S1: a game doesn't need to be new to be fun, just "a little different", since many JRPGs are samey `[07:59]`.
- **How to use AI.**
  - B proposed a grilling session (Matt Pocock's grilling skill) as a mirror for their thinking `[02:41]` `[06:49]`. S1 called it "so overrated" `[02:48]`.
  - S1: the ideas have to come from us, and we need to know what AI can actually do before prototyping (`[05:17]` `[35:58]` `[36:31]`). He accepts AI for expanding an idea once they have it.
  - B: explore with several cheap prototypes, find where AI struggles and build scaffolding there (`[36:09]` `[36:37]`). An agent can also fill their game-dev gaps `[08:20]`.
  - S1 replies that they know game design from playing games, but concedes that design is limited by what's feasible (`[08:31]`–`[09:01]`).

## First prototype

**S1's proposed build order** for his Unreal build. He narrowed the scope during the call: at `[33:02]` it included "basic battle mechanics", by `[37:00]` it was "you don't even need to go to the battle":
1. Environment and characters.
2. Character movement.
3. The switch into battle, to prove the whole loop works.
4. Later: battle depth, level-ups, quests.

**The opening scene**, as described on the call: Kaladin "becoming a slave" `[25:43]`, "he's a bridge builder… the bridge brigade runs into some monsters or something" (S1 `[33:31]`).
- "Monsters" was S1's loose wording.
- Following the book would mean Sadeas's bridge crews (Bridge Four) under Parshendi arrows. Swapping in a creature encounter would be a design choice. See the lore corrections above.

**B's track:** write the opening story, and explore an AI-driven build through multiple prototypes `[34:02]` `[35:39]` `[36:09]`.

## Next steps / commitments from the call

- [ ] B sends S1 the Cosmere RPG links `[23:27]` `[24:31]`.
- [ ] Each sets up a branch in this GitHub repo with their attempt, and they compare (`[34:14]` `[34:35]`).
- [ ] B runs a Wayfinder session on this recording and shares the link with S1 for his reaction (`[37:52]`–`[38:03]`).
- [ ] S1 builds the demo scene in Unreal `[34:59]`.
