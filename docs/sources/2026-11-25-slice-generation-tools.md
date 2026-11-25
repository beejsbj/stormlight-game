# Slice generation tools: stills, consistency, image→3D, terms

Research for issue #4, "Which tools can make game-moment stills for slices?" (child of map #1, a solo (B) map). Read 2026-11-25. Everything labelled **Fact** is from the owning vendor's own page, cited inline. Everything labelled **Judgement** is mine (the agent's), not sourced, and not agreed with anyone.

**Not legal advice.** Terms pages change; each URL below was read on 2026-11-25. Re-read the one you rely on.

## Short answer

- **No vendor documents "looks like a game frame."** That quality is a prompting-and-testing question, not a feature. What the docs do establish is which tools accept camera language, wide aspect ratios and multiple reference images (the raw ingredients for in-engine-looking stills and for consistency). See the table.
- **Consistency** is best served today by *multi-reference editing* (Gemini "Nano Banana" family, Midjourney's Edit model, OpenAI's image model, FLUX.2) for cheap, no-training work, and by *trained models* (Scenario, Leonardo Elements) if references drift across many slices.
- **Image → 3D** is real but is a *blockout/reference* path, not a finished game asset (judgement; vendors don't state quality). Multi-view input (turnaround) is supported by Meshy (1–4 images), Rodin (up to 5), and Tripo ("Multi-Views to 3D").
- **Terms matter more than usual here.** Three findings that affect a *public* repo:
  1. **Leonardo free plan: Leonardo owns the outputs** (ToS cl. 8.7). Paid plan: you own them.
  2. **Midjourney: images are public and remixable by default**, and Midjourney keeps a perpetual licence to everything you generate (ToS §4).
  3. **Canva: don't remove provenance/C2PA metadata, and don't pass AI output off as human-made** (AI Product Terms). Gemini images carry a SynthID watermark.
  Also: Canva's own help says US-style law may give AI output *no copyright at all*. You can "own" it contractually and still be unable to stop anyone copying it (see "Copyright caveat").

## Comparison table

Stills tools. "Refs" = how many reference images the tool accepts as input. Ownership is *as between you and the vendor*.

| Tool | Current model (read 2026-11-25) | Refs for consistency | Wide/cinematic ratios | Output ownership (paid) | Notable restriction for a public fan project |
|---|---|---|---|---|---|
| **Canva AI** (image generation) | Not verified. Canva's May 2025 post says Canva AI blends in-house models, Leonardo's Phoenix, and OpenAI/Anthropic partnerships; "Create an image" runs on Dream Lab. No current model list found. | Uploaded style references (Canva newsroom); Canva's connector tool accepts several reference images (tool schema, no stated cap). No documented character-lock feature. | 16:9, 3:2, 2:1, others (tool schema) | You own Output, except output that incorporates Canva library content. Outputs "may not be unique." | Help says "Don't reference known brands, characters, or people in your prompts (unless you have express permission)." Don't strip C2PA metadata. |
| **Gemini / Nano Banana** (Google) | Nano Banana 2.1 (`gemini-nano-banana-2.1`, recommended for new projects), Nano Banana 2, Nano Banana 2 Lite, Nano Banana Pro (`gemini-3-pro-image`), Nano Banana (`gemini-2.5-flash-image`) | Up to 14 mixed reference images; character-consistency inputs: up to 4 (2.1 / 2) or 5 (Pro); Pro also takes up to 3 style refs. Multi-turn editing recommended. | 14 ratios incl. 16:9, 21:9; 1K/2K/4K | Google "won't claim ownership" (API terms). Google may generate the same or similar for others. | Prohibited Use Policy: no violating others' IP rights. SynthID watermark on all generated images. API terms are for professional/business use. |
| **Midjourney** | V8.2 (default since 2026-07-24); V8.1 added HD (2K) | **Edit model: up to 4 reference images** (replaces Omni Reference, Character Reference); Style Reference, Moodboards, Personalization | Up to 14:1 (4:1 in HD) | You own Assets (paid plans; Pro/Mega if company revenue >$1M). Free: see note. | Public and remixable by default; **Stealth only on Pro/Mega**. Perpetual sublicensable licence to Midjourney. |
| **Leonardo.Ai** (Canva-owned) | Hosts many third-party models (FLUX.1 Kontext, Nano Banana, Seedream listed in API docs) | Elements (LoRA), image-prompt guidance, per-model uploaded-image recipes | Not checked | **Paid: yours. Free: Leonardo's** (cl. 8.7) | Public Content can be used to train AI. Don't generate "impersonations of any real person." |
| **OpenAI image model** | Docs name `gpt-image-2.5-*` and "GPT-Image-2.6 Sunburst/Flare" on one page (naming conflict, confirm live) | Edits accept reference images; max not stated in the page I could read. Docs admit consistency of recurring characters can be weak. | Not checked | "You… own the Output" (Terms of Use), not extending to others' output | Usage Policies prohibit infringing others' IP and using someone's likeness without consent. Nothing on artists' names. |
| **FLUX.2 / FLUX 3** (Black Forest Labs) | FLUX 3 is "latest"; FLUX.2 "remains fully supported" | Up to 8 (API) / 10 (playground) references; "maintain a character's identity… across multiple generations." | Not checked | **Not found on pages I could read** (legal page 404) | Open-weight [dev]: "Free (non-commercial)." klein 4B Apache 2.0; klein 9B Non-Commercial. Check licence before any commercial use. |
| **Scenario** (game-asset platform) | Hosts Gemini, GPT Image, Flux 2, Seedream, others; trains custom models | **Trains Style and Consistent-Character models** (Pro plan or above, ≥5 images); or use references (Scenario's page: GPT Image up to 10, Gemini up to 14) | Not checked | "You own your generated assets" (ToS short version, v2.1.1, 2026-07-16) | Each provider's content policy still applies. Terms say no deepfakes of real people. Self-serve: Scenario may use your content to improve its services. |

**Midjourney free-plan note:** the ToS I read (effective 2026-05-27) says "You own all Assets You create" and only carves out the revenue rule; I did not find a free/paid split in this version, unlike what secondary sources claim. Midjourney's pricing pages (not read) may still gate access.

Image → 3D tools:

| Tool | Version read | Input | Output | Ownership of output |
|---|---|---|---|---|
| **Meshy** | Meshy 7.1 (image → 3D) | Single image, or 1–4 images of the same object from different angles (first = front view). `pose_mode` a-pose / t-pose for characters. | GLB, OBJ, FBX, STL, USDZ, 3MF; PBR maps; quad or triangle retopology (default 30k polys); rigging and animation in app | Paid: private, commercial, "You own the output" (pricing page). **Free: CC BY 4.0** and the (Czech) terms say Meshy owns free-plan outputs; sources conflict. Meshy may train on non-Enterprise inputs/outputs unless you opt out. |
| **Tripo** | H3.1 (`v3.1-20260211`), P2.0 (native quad topology) | Image to 3D; "Multi-Views to 3D" (number of views not stated) | GLB, FBX, OBJ, USDZ; Auto Rig; retopology as a post step | Paid users "generally have all rights"; **free users: "Tripo retains all rights"** (terms updated 2025-07-11) |
| **Rodin / Hyper3D** | Gen-2.5 | 1–5 images of the same object; "no prescribed pose or camera angle" | GLB, FBX, OBJ, USDZ, STL; PBR; quad or raw topology; up to 12K textures | ToS: "we will not limit your use of such Output"; no representation on copyrightability. API files retained 7 days. |
| **Hunyuan3D 2.1** (Tencent, open weights) | 2.1 (no 3.x repo found) | Single image | GLB, PBR texture synthesis; 10–29 GB VRAM | "Tencent claims no rights in Outputs." **Licence does not apply in the EU, UK or South Korea**; >1M MAU needs a licence. |
| **TRELLIS** (Microsoft, open source) | TRELLIS (arXiv 2412.01506); TRELLIS.2 not found | Single image; multi-image conditioning added (tuning-free, "may not give the best results") | Radiance fields, Gaussians, meshes; GLB export; ≥16 GB NVIDIA GPU | MIT licence on code/models; no output terms stated |

## Part 1: Which tools make a still that reads as a game moment?

### What the sources establish (Fact)

- **Gemini** (`aistudio.google.com/docs/image-generation`, no page date): the docs advise "photographic and cinematic language," with `wide-angle shot`, `macro shot`, `low-angle perspective` as examples. Output at 1K/2K/4K in ratios up to 21:9. Image models are "thinking" models; multi-turn conversation is "the recommended way to iterate." For consistency: "include previously generated images in subsequent prompts."
- **Midjourney** (`docs.midjourney.com`, Edit Model article, updated 2026-08-28): "Generate new images using up to 4 reference images (replacing Omni Reference and Character Reference)." Includes "Changing Perspective" ("let's see this image from the front / from behind") and retexturing with Style References. Compatible with V8.1 and V8.2. Tip from the docs: if attributes get mixed between characters, "combine your characters into a single reference image."
- **Canva**: "Create an image… Powered by Dream Lab… now guided by your own uploaded style references" (newsroom, 2025-05-11). Canva's connector (the one available inside Claude) takes `imageReferences` (several) and ratios from 1:1 up to 2:1. It does **not** let you pick the model, and I found no documented character-lock.
- **FLUX.2** (`docs.bfl.ml`): identity "(face, clothing, proportions, and style)" holds "across multiple generations" via multi-reference editing.
- **Scenario** (`help.scenario.com`): "Try reference images first. You may not need to train at all… Upload a few clean images of the character, such as a front view, a turnaround or an expression sheet." Training a Character Model needs a paid plan and at least 5 images; 5–15 well-varied images work better than 20+ redundant ones.

### What I could not establish

- No primary source says any tool produces an "in-engine," HUD-less gameplay-frame look. Nothing in the docs compares tools on that.
- I did not generate test images. Everything about which tool *looks* most like a game is untested.
- Canva's current image model list; Leonardo's character-reference feature (docs index shows Elements and image guidance, no dedicated page); OpenAI's reference-image maximum.

### Judgement (mine, untested)

- Start with **Gemini** (cheap multi-reference, explicit camera language, 16:9/21:9, 4K) and **Midjourney** (strongest style-reference tooling, V8.2 aesthetic emphasis). Add **Scenario** if you want one place to try several models and, later, train a character model from your own approved generations.
- **Canva** is the weakest fit for this job based on what's documented (no model choice, no character lock). It's best as a layout/compositing surface, which is a different task from generating the slice.
- A fair test would be one fixed kit of three prompts: *(a)* wide third-person gameplay frame at the chasm edge, *(b)* over-the-shoulder cutscene still, *(c)* medium close-up of the character. Run it across Gemini, Midjourney and one of Scenario/FLUX, then react. This matches the map's generate → react → narrow rhythm.
- Prompt words worth trying for the look (untested): "third-person gameplay camera," "real-time render," "no UI," "shallow depth of field," "stylised realism." Describe the *qualities* of inspirations in your own words, per the map's Copyright note.

## Part 2: Consistency across many generations

| Method | Tools | Effort | Notes |
|---|---|---|---|
| Multi-reference in the prompt | Gemini (≤14, with ≤4–5 character refs), Midjourney Edit (≤4), FLUX.2 (≤8–10), OpenAI, Scenario's hosted models | None; no training | Fact: Midjourney and Google both say multi-turn / feeding prior outputs back helps. Judgement: drift over dozens of slices is likely; keep a canonical sheet and always re-attach it. |
| Style reference / moodboard | Midjourney (Style Reference, Moodboards, Personalization), Canva (style references), Gemini Pro (≤3 style refs) | Low | Locks *look*, not identity. |
| Trained model (LoRA-type) | Scenario (Character/Style models; Flux 2, Z-Image, Qwen bases), Leonardo (Elements) | Needs a dataset of your own approved images; paid plan on Scenario | Judgement: worthwhile only once a character or place has a settled sheet; training on unsettled art locks in the wobble. |

Fact worth keeping in view: the sheet you feed back in is itself a generation. Under the terms below you "own" it, but see the copyright caveat.

## Part 3: Image → 3D

### Facts

- **Multi-view / turnaround input** is supported by Meshy (1–4 images, first is front), Rodin (1–5), Tripo ("Multi-Views to 3D"; count not stated), and TRELLIS (experimental). Hunyuan3D 2.1's public docs show single-image only.
- **Game-pipeline outputs** exist: quad retopology (Meshy, Tripo P2.0, Rodin), PBR maps (Meshy, Rodin, Hunyuan), auto-rigging (Tripo, Meshy). Meshy's default retopology target is 30,000 polygons.
- **Aggregators:** Leonardo's API lists Meshy 7, Rodin V2 and Tripo H3.1 as available models; Scenario's help centre has a "3D Generation" collection (31 articles; not opened).
- **Retention:** Meshy API outputs are deleted three days after generation (non-Enterprise); Rodin API files are kept 7 days. Download promptly.

### Not found

- No vendor states how well it handles stylised characters vs humans, or A-/T-pose accuracy, beyond Meshy's `pose_mode` parameter and Rodin's marketing line that it makes "nearly ready-to-use characters, props, collectibles, and stylized 3D assets."
- Hunyuan3D 3.x, TRELLIS.2 and Tripo's view-slot rules were not verifiable.

### Judgement (mine)

- Expect a **starting mesh**, not a shippable one: plan for cleanup, retopology and rigging by hand or tool. This is general knowledge about the category, not drawn from these vendors' pages. A single AI image gives the model a guess about the back and sides; a turnaround removes the guess.
- **What to prepare as input:** a clean, evenly lit character on a plain background in A-pose or T-pose, with front/side/back views that match each other. A Gemini or Midjourney sheet generated for this purpose is the cheapest source. Environments and props are easier than expressive hero characters.
- The slice stays a *concept* for now. The map says the engine and AI build workflow are pinned, so don't pick a 3D tool on the strength of this note.

## Part 4: Ownership, licensing and restrictions (public fan repo)

### Copyright caveat (Fact + judgement)

- Canva's help: "Currently, many jurisdictions (including the US) do not give copyright protection to AI-created works… you may be limited in your ability to stop other people from using or copying these works" (`canva.com/help/using-magic-studio-safely-and-legally/`). That is Canva's statement of the law, not a legal ruling.
- Judgement: for a public repo this cuts two ways. The tool terms below mostly grant you what rights *exist*, and may leave you with none enforceable. Conversely, don't assume AI output is clear of other people's rights, since every vendor disclaims non-infringement.

### Per tool

**Canva** (AI Product Terms, effective 2026-06-26; Acceptable Use Policy updated 2025-08-07)
- *Fact:* "you own your Output, except for any Output that modifies or incorporates Licensed Content." "Outputs may not be unique." "You may use your Output for any lawful purpose… at your own risk."
- *Fact:* prohibited: misleading anyone that output is human-generated; removing "any provenance or metadata tags… including… C2PA metadata"; bypassing safety features.
- *Fact:* AUP bars content that "violates the rights of any individual or third party, including their intellectual property."
- *Fact (help centre):* "Don't reference known brands, characters, or people in your prompts"; "use descriptive and generic prompts."
- *Fact:* inputs may be shared with Canva's "Technology Partners"; your privacy settings control use for improving AI.
- *Implication (judgement):* naming Kaladin, Shardblades etc. in a Canva prompt is exactly what Canva's help tells you not to do. This lines up with the map's own rule to describe qualities in your own words.

**Gemini / Google**
- *Fact:* Gemini API Additional Terms (effective 2026-03-23): "Google won't claim ownership over that content"; "Google may generate the same or similar content for others"; "You're responsible for your use of generated content." Use is "for professional or business purposes, not for consumer use" (API/AI Studio).
- *Fact:* Generative AI Prohibited Use Policy (last modified 2024-12-17) bars use that "Violates the rights of others, including… intellectual property rights," and impersonation intended to deceive. It has no clause on artists' names.
- *Fact:* "All generated images include a SynthID watermark" (Gemini API docs).
- *Not verified:* the Gemini **app** (consumer) output terms. The old "Generative AI Additional Terms" page says it no longer applies since 2024-05-22; the current Google Terms of Service weren't read. Only API/AI Studio terms are confirmed above.

**Midjourney** (ToS effective 2026-05-27)
- *Fact:* "You own all Assets You create… to the fullest extent possible under applicable law," subject to third-party rights; companies over $1M annual revenue need Pro or Mega. Ownership "persists even if… You downgrade or cancel."
- *Fact:* you grant Midjourney "a perpetual, worldwide, non-exclusive, sublicensable… irrevocable copyright license" to your Inputs and Assets.
- *Fact:* "By default, Your Content is publicly viewable and remixable." Stealth is a Pro/Mega feature and doesn't apply in shared Discord spaces.
- *Fact:* "You may not use the Service to try to violate the intellectual property rights of others, including copyright, patent, or trademark rights." You indemnify Midjourney for third-party claims arising from your use.
- *Not found:* any rule in the ToS about using artists' names in prompts.

**Leonardo.Ai** (ToS updated 2026-01-19)
- *Fact:* paid: IP "will vest in you upon creation"; **free: ownership of Output "will vest in us"** (cl. 8.7).
- *Fact:* paid users choose public or private. Public Content may be used by Leonardo for "training AI models… or for any commercial purpose." Private Content is not used for training without written consent.
- *Fact:* bans "impersonations of any real person."

**OpenAI** (Terms of Use effective 2026-01-01; Usage Policies effective 2026-11-20)
- *Fact:* "you (a) retain your ownership rights in Input and (b) own the Output," not extending to other users' output; "to the extent permitted by applicable law."
- *Fact:* Usage Policies prohibit "attempts to infringe on intellectual property rights of others" and using "someone's likeness… without their consent." Neither page mentions living artists' styles.

**FLUX / Black Forest Labs**
- *Not found:* output ownership terms (the legal page I tried returned 404). Licence of the open weights is the issue: [dev] "Free (non-commercial)"; klein 9B "FLUX Non-Commercial License"; klein 4B Apache 2.0. The [dev] licence text was not read.

**Scenario** (Terms v2.1.1, 2026-07-16)
- *Fact:* "You own your generated assets. Use them commercially, sell them, modify them." Self-serve plans: Scenario "may use your content and anonymized insights to improve our Services and AI — never sold, never shared with other customers."
- *Fact (help centre):* each hosted model's provider enforces its own content policy; named copyrighted characters are a common block trigger. Scenario's own guidance is "Describe visually, do not name."

**3D tools**
- *Meshy:* see table; the free-plan ownership statements conflict between the pricing page ("You own the output" plus CC BY 4.0 attribution) and the terms (paraphrased from the Czech translation, which says Meshy owns free-plan outputs). Treat free-plan output as **attribution-required at minimum**.
- *Tripo:* free-plan outputs belong to Tripo; paid users "generally have all rights." Terms published by Holymolly Ltd, Hong Kong law.
- *Rodin:* "we make no representations… as to the copyrightability of any Output." §6.3 bars users from "sell[ing], resell[ing] or commercially us[ing] the Content," and it is unclear whether "Content" covers outputs. Ask before commercial use.
- *Hunyuan3D 2.1:* the licence "DOES NOT APPLY IN THE EUROPEAN UNION, UNITED KINGDOM AND SOUTH KOREA"; using it there "is unlicensed and unauthorized." Outputs may not be used to improve other AI models.
- *TRELLIS:* MIT licence; the licence says nothing about outputs.

### Artist names and fan-content policies

- *Fact:* none of the primary pages I read (Canva, Google, OpenAI, Midjourney, Leonardo, Scenario, BFL) contains an explicit prohibition on putting a living artist's name in a prompt. Canva, Scenario and OpenAI/Google restrict named *characters, brands and real people*.
- *Judgement:* the map's rule (never name a living artist; describe qualities) is stricter than any vendor's, and it is the right shape for a public repo. Vendor silence doesn't make artist-name prompting safe.
- *Not researched:* whether Dragonsteel/Brandon Sanderson publishes a fan-content policy that covers AI-generated imagery or games. That is a separate question from tool terms and probably deserves its own ticket.

## Gaps and cautions

- **Fetch blocked, read via browser:** Canva, Midjourney, Leonardo and Scenario pages returned 403/404 to the automatic fetcher; I read them in a browser session instead. Pages are as rendered 2026-11-25.
- **Model-summarised sections:** the long Gemini and OpenAI image-generation pages, and the later sections of the Meshy, Tripo and Rodin terms, were read via a summarising fetcher, not verbatim. Quotes are verbatim only where marked as quoted, but aspect-ratio tables and reference-count details should be spot-checked on the live pages before depending on them.
- **Meshy terms** were read in the Czech translation (English prevails per the page); the points marked "paraphrased" are my reading of that translation.
- **Not tested:** no images or 3D models were generated for this note.
- **Naming drift:** OpenAI's and Google's model names change fast (the OpenAI page itself names both 2.5 and 2.6). Check the live model ID before building a workflow on one.
- **Missing:** Adobe Firefly, Stability, Ideogram, Recraft and others were not researched.

## Sources

Image generation
- Gemini API image generation (redirects to aistudio.google.com): https://ai.google.dev/gemini-api/docs/image-generation
- Gemini API models: https://ai.google.dev/gemini-api/docs/models
- Gemini API Additional Terms: https://ai.google.dev/gemini-api/terms
- Google Generative AI Prohibited Use Policy: https://policies.google.com/terms/generative-ai/use-policy
- Google Generative AI Additional Terms (superseded 2024-05-22): https://policies.google.com/terms/generative-ai
- Canva AI Product Terms: https://www.canva.com/policies/ai-product-terms/
- Canva Acceptable Use Policy: https://www.canva.com/policies/acceptable-use-policy/
- Canva, "How to use Magic Studio safely and legally": https://www.canva.com/help/using-magic-studio-safely-and-legally/
- Canva newsroom, AI launches (2025-05-11): https://www.canva.com/newsroom/news/canva-ai-launches/
- Canva newsroom, MCP and video (2026-11-23): https://www.canva.com/newsroom/news/canva-mcp-video-generation/
- Midjourney Terms of Service: https://docs.midjourney.com/hc/en-us/articles/32083055291277-Terms-of-Service
- Midjourney Edit Model: https://docs.midjourney.com/hc/en-us/articles/48495453462797-Edit-Model
- Midjourney Version: https://docs.midjourney.com/hc/en-us/articles/32199405667853-Version
- Leonardo.Ai Terms of Service: https://leonardo.ai/terms-of-service
- Leonardo API docs (Elements, deprecations, pricing FAQ): https://docs.leonardo.ai/
- OpenAI image generation guide: https://developers.openai.com/api/docs/guides/image-generation
- OpenAI Terms of Use: https://openai.com/policies/terms-of-use/
- OpenAI Usage Policies: https://openai.com/policies/usage-policies/
- Black Forest Labs docs: https://docs.bfl.ai/ and https://docs.bfl.ml/flux_2/flux2_overview.md
- BFL character consistency guide: https://docs.bfl.ml/guides/usecases_editing_character_consistency.md
- Scenario Terms and Conditions: https://www.scenario.com/terms-and-conditions
- Scenario, content policy by model: https://help.scenario.com/articles/8779329416-content-policy-copyright-what-each-model-allows
- Scenario, train a consistent character model: https://help.scenario.com/articles/4280773511-train-a-consistent-character-model

Image → 3D
- Meshy docs: https://docs.meshy.ai/ ; multi-image: https://docs.meshy.ai/en/api/multi-image-to-3d ; pricing and licensing: https://docs.meshy.ai/en/webapp/pricing ; terms (Czech): https://www.meshy.ai/cs/terms-of-use
- Tripo developer docs and terms: https://developers.tripo3d.ai/ and https://developers.tripo3d.ai/en/terms
- Hunyuan3D 2.1: https://github.com/Tencent-Hunyuan/Hunyuan3D-2.1 (LICENSE in repo)
- Microsoft TRELLIS: https://github.com/microsoft/TRELLIS
- Hyper3D Rodin: https://hyper3d.ai/features/api and https://hyper3d.ai/legal/terms
