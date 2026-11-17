# Stormlight game — sources & inspirations brief

Status: **early exploration** (as of 2026-11-17). Nothing below is settled unless marked *agreed*.

**Primary source:** the 2026-11-17 design call between Burooj (**B**) and his co-designer Ashar (**A**, spelling unconfirmed). See [`sources/2026-11-17-call-transcript.md`](sources/2026-11-17-call-transcript.md), Gemini's transcript, which was checked against FluidVoice's. Timestamps like `[23:58]` point into it.

**Read this first if you're planning from this brief:**
- Whatever you produce goes back to Ashar for his reaction `[38:03]`.
- Ashar is sceptical of AI-generated ideas. He thinks the ideas must come from the two of them; AI only expands them `[05:17]` `[06:47]`.
- So present options with attribution rather than recommendations.
- Tags: (B) and (A) mark one person's view. Untagged lines are views both of them shared.

## The idea in one paragraph

A fan-made, story-led party RPG adapting Brandon Sanderson's *The Stormlight Archive*.
- Ashar's framing: "maybe the story inspires the mechanics" `[14:11]`.
- Both are new to game development and to storytelling, so they adapt an existing story rather than invent one (B `[14:30]`). Both intend to build with AI help (`[34:36]`–`[34:59]`).
- Start with a demo of one section of the books.
- If they enjoy playing it, ask Brandon whether it could ever be sold. Otherwise it stays an open fan project (B `[15:07]`).

## Source material (what we adapt)

| Source | What we take from it | Notes |
|---|---|---|
| **The Stormlight Archive** (Brandon Sanderson) | Story, characters, world, magic system: Surges, Orders of Knights Radiant, Ideals | *Agreed:* adapt one section of the books as the demo (A `[23:58]`). Going by the proposed opening, probably *The Way of Kings* (book 1). Ashar: it has "a lot of JRPG-ness" `[17:16]`. B agrees, and adds that Sanderson is a JRPG fan `[17:32]`. |
| **Cosmere Roleplaying Game** (Brotherwise Games, the official tabletop RPG, with a Stormlight handbook and world guide) | Ready-made translation of the books into mechanics: ability design per Surge, flora and fauna and world reference, skeleton adventures that still allow branching | B is sending Ashar links `[23:28]` `[24:31]`. (B) Mine it for ideas; don't copy it wholesale (`[17:49]` `[22:51]` `[24:42]`). Ashar is "not too much into tabletop stuff" `[24:39]`. B's claim that it makes swearing an Ideal a big level-up moment is **secondhand** ("from what I've heard") `[28:25]`. Check it in the handbook. |
| **Coppermind wiki** (coppermind.net) | Lore lookup | Not discussed on the call. It's the obvious lore reference for agents. |

### Lore corrections to the transcript

Read these before the opening-scene section below.
- Kaladin's Windrunner Surges are **Adhesion and Gravitation**, not "gravity and friction" `[28:25]`.
- His powers come from swearing **Ideals**, not "promises".
- The call's order, "first the spear, then flying" `[31:51]`, is roughly backwards:
  - In book 1 he uses Stormlight and Lashings and swears the Second Ideal near the end.
  - Syl becomes a Shardblade or Shardspear at the Third Ideal, in book 2.
- Shallan is a Lightweaver: Illumination and Transformation. Every Lightweaver can make illusions, so treat B's point that other Lightweavers don't make "clones" of themselves `[32:26]` loosely.
- The book's opening:
  - *The Way of Kings* opens with the Prelude, then the Prologue (Szeth killing Gavilar).
  - Chapter 1 shows Kaladin through Cenn's eyes, as a squadleader in Amaram's army.
  - Chapter 2 begins Kaladin's own point of view, already a slave. How he became one is told in flashbacks.
  - On bridge runs the danger is **Parshendi archers**.
  - Bridge Four doesn't meet a chasmfiend in book 1. Kaladin and Shallan meet one in the chasms in book 2.

## Game references: what to take, what to avoid

B named three reference points to steer by `[17:49]` `[19:31]`:
- FFVII Remake
- Expedition 33
- *Divinity: Original Sin* (an "environment-based" turn-based game)

| Reference | Take | Avoid / caution |
|---|---|---|
| **Clair Obscur: Expedition 33** | The flow of combat (B `[17:49]`, A `[19:23]`) and the animation (A `[18:52]`); precision (B `[19:31]`); cinematic quality even in gameplay (B `[30:23]`); casual players got into it (A `[24:54]`); items reset at checkpoints, as in Souls-likes (A `[19:42]`); no character creation, the menu is the start screen (B `[25:19]`) | The party feels samey (A `[30:09]`). Verso and Maelle, two-thirds of your party, play alike (A `[30:56]`), and so does Gustave (B `[31:14]`). Players ignore the unique characters' wilder kits (`[31:19]`–`[31:35]`). Levelling doesn't *feel* like anything (A `[28:01]`). |
| **Final Fantasy VII Remake** | Tactical party play: you win by combining all the characters' skills (B `[01:02]`–`[01:27]`). Clearly distinct characters: Barret shoots, Aerith casts (B `[27:14]`, `[30:38]`). | — |
| **Persona 5** | Each party member has a distinct, fixed identity (B `[27:14]`) | The calendar structure gets formulaic; Ashar couldn't get into the P3 remake (A `[09:55]`). Hoarded consumables trivialise dungeons (`[20:01]`–`[20:28]`). Levelling doesn't feel like anything (A `[28:01]`). Ashar finds it even more samey than E33 `[30:20]`. |
| **Metaphor: ReFantazio** | Ashar cited it as a JRPG without a separate battle mode, then conceded B's point about the overworld/battle divide `[00:36]`. Note: it still has turn-based battles. It adds real-time field attacks on weaker enemies, so it's a hybrid. | — |
| **Divinity: Original Sin 2** | Environment-based, world-heavy CRPG framing for a story full of side characters (B `[17:49]` `[21:04]`). The "holy shit, what did I unlock?" level-up (A `[21:25]`). B thinks chapter transitions are more seamless than in Persona or E33 `[21:45]`. | Ashar: that seamlessness depends on the story, because DOS branches; B concedes "that's true" `[22:16]`–`[22:28]`. Two people can't do branching (A `[22:39]`). |
| **Baldur's Gate 3** | Same level-up satisfaction (A `[21:25]`) | Overwhelming on first open; we must stay casual (A `[24:54]`) |
| **Souls-likes / Elden Ring** | (A) Souls-like + JRPG was Ashar's opening idea: real-time dodging `[00:06]`–`[00:55]`. Items reset at checkpoints (A `[19:42]`). | Elden Ring–grade bosses are beyond us (A `[08:53]`) |
| **Pragmata** (Capcom) | Its hacking was "a niche mechanic… pretty fun, and it wasn't anything complicated" (A `[09:55]`). Aim for "what can be done in a simple way while also pushing some boundaries" (A `[08:53]`). | — |
| **God of War** | Drop straight into the game (B `[25:19]`) | — |
| **Hunter × Hunter** (Nen) | Within a hard magic system, users are creative with their powers; Surges allow the same (B `[32:26]`) | — |
| **Greatest Estate Developer** (manhwa), plus base building like FarmVille and Clash of Clans | Ashar's alternative pitch: build real estate projects, fight monsters in the overworld, "Clash of Clans, but… not boring" in a JRPG `[15:30]`–`[16:51]` | *Parked*: B wasn't drawn to it `[17:05]`, and Ashar was happy to start with Stormlight `[17:16]`. |

## Positions so far

*Agreed*
- **Adapt the books directly.** For the demo, follow one section of the books closely (A `[23:58]`, B `[24:03]`). Ashar joked they could later "retcon it… [and] be like, 'This is our story'" `[24:06]`.
- **Fixed story for the demo:** "we are only two people, so we have to be fixed story" (A `[22:39]`). B agreed (`[22:51]` `[24:03]`), after floating "a little bit of flexibility" via the Cosmere RPG's skeleton adventures `[23:28]`.
- **Casual-friendly**, like E33: Ashar's point, and B "completely agree[s]" (`[24:54]` `[25:19]`).
- **Level-ups should feel big.** This is Ashar's complaint about E33 and Persona `[21:25]` `[28:01]`; B: "that is very satisfying" `[21:36]`.
- **No consumable hoarding**; control the difficulty curve `[19:42]`–`[20:28]`.
- **Skeleton or prototype before theorising** (A `[33:02]`, B `[33:26]`).

*Likely shared, not confirmed*
- **Multiple playable characters, each clearly distinct.** B argues for it `[25:49]` `[30:46]`. Ashar's "I know what you mean" `[30:44]` and his E33-is-samey critique suggest agreement, but he also wants build variety (see class flexibility below).

*Proposed by one side*
- (B) Cinematic, like E33: no character creation, the menu is the start screen, the way you enter *God of War* (`[25:19]` `[30:23]`). Ashar only said "Mhm" (`[25:47]` `[30:36]`), though he praised E33's animation `[19:23]`.
- (B) Tie level-ups to swearing Radiant Ideals, so each one changes how the character plays `[28:25]`. Ashar's only response was a minimal "Yep" to Kaladin's power changing with each oath (`[31:50]` `[32:25]`).
- (B) Give the game modes that push players to use each character's wilder abilities. This is the fix for E33 feeling samey `[31:51]`.
- (B) With AI, there are no cost constraints, so characters can shift drastically `[28:25]`. **This is an assumption nobody has tested.** Ashar's later point cuts against it: "you don't know what the AI is even capable of" `[36:14]`.

*Open / disputed*
- **Combat model.** Undecided `[00:09]`–`[01:27]` `[17:49]`. Options:
  - Souls-like real-time dodging: Ashar leaned this way `[00:55]`.
  - FFVII Remake's tactical party play: B, "it could be tactical also" `[01:02]`.
  - E33's turn-based combat with timed reactions.
  - DOS-style environment-based turn-based combat (B `[17:49]`).
  - Note: Ashar's demo plan has a "transition into the battle phase" (`[35:23]` `[37:04]`), which assumes a separate battle mode, the JRPG divide B described at `[00:31]`.
- **Class flexibility.**
  - Ashar wants build variety: switch class at level-up, or at least subclasses (`[26:10]`–`[26:38]` `[28:01]`).
  - B wants fixed classes but allows variety in moves: "Shallan uses illusions; she won't suddenly start flying" `[26:51]` `[27:14]`.
  - B's middle option: choose abilities within a character's Surges at each level-up `[28:25]`.
- **Does it need to be new?**
  - B: use AI to map what's already been done, so they can find the new space (`[07:05]` `[07:49]`).
  - Ashar: a game doesn't need to be new to be fun, just "a little different", since many JRPGs are samey `[07:59]`.
- **How to use AI.**
  - B proposed a grilling session (Matt Pocock's grilling skill) as a mirror `[02:39]` `[06:50]`.
  - Ashar called it "so overrated": "you can either be creative or… let me have another human ask me 100 questions" (`[02:48]` `[03:01]`).
  - Ashar: the ideas have to come from them, and they need to know what AI can actually do before prototyping (`[05:17]` `[36:14]` `[36:32]`).
  - B: explore with several prototypes, and find where AI struggles so they can build scaffolding there (`[36:06]` `[36:38]`). An agent can also fill their game-dev gaps `[08:21]`.
  - Ashar: they know game design from playing games, though he concedes design is bounded by what's feasible (`[08:38]`–`[08:53]`).

## First prototype

**Both build the demo scene with AI, each on their own branch** (`[34:14]`–`[34:36]`).
- Ashar's clarification: not just ideas but "actually doing the demo scene… within Unreal" (`[34:59]`–`[35:23]`).
- Engine: Unreal is Ashar's choice. B hasn't responded to it.

**B's part, which he agreed to** (`[33:31]` `[34:03]` `[34:14]`):
- Write the story and the opening scene.
- Work out how to build the level purely with AI, and share the GitHub.
- B also wants to explore through multiple prototypes `[36:06]`.

**Ashar's build order.** He narrowed it during the call: at `[33:02]` it included "some basic battle mechanics"; by `[37:04]` it was "you don't even need to go to the battle".
1. Environment and characters
2. Character movement
3. Transition into the battle phase
4. Later: battle, level-up, quest system

**The opening scene, as described on the call:**
- "It can start with like him becoming a slave" (B `[25:19]`).
- "He's a bridge builder… the bridge brigade runs into some monsters or something like that. I don't know." (A `[33:31]`)
- "Monsters" was loose wording. Following the book means Sadeas's bridge crews (Bridge Four) under Parshendi arrows, with Kaladin already a slave. Swapping in a creature encounter is a design choice to make. See the lore corrections above.

## Next steps / commitments from the call

- [ ] B drafts the story and the demo's opening scene (`[33:31]` `[34:03]` `[34:14]`).
- [ ] B sends Ashar the Cosmere RPG links `[23:28]` `[24:31]`.
- [ ] Each prototypes the demo scene with AI on their own branch in this GitHub repo, and they compare (`[34:14]`–`[34:59]`).
- [ ] B runs a Wayfinder session on this recording and shares the link with Ashar for his reaction (`[37:52]`–`[38:03]`).
