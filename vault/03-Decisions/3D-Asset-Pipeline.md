# 3D Asset Pipeline — how do I get the models without becoming a 3D artist?

> ✅ **Settled 2026-09-12 -> [[The-Approach]].** This note is the reasoning behind that decision; the decision itself lives there.
>
> **The constraint:** I don't have time to learn Blender modelling properly. I want AI/automation to carry the asset work.
> **The honest answer:** AI helps a lot, but not where people expect. Read this before spending money on a text-to-3D subscription.

---

## The thing nobody tells you about "AI 3D models"
Text-to-3D tools (Meshy, Tripo, Rodin, Luma, Hunyuan3D) will genuinely give you a chair in 30 seconds. The problems only show up *after*:

1. **Style drift.** Ten AI props = ten slightly different art styles. The whole point of my room is a *consistent design language that feels like me*. This is the single biggest risk to the concept.
2. **Messy geometry.** Dense meshes, weird topology, oversized textures. Fine for one prop, painful for a whole scene on mobile.
3. **They don't bake.** The cute-room look comes from **baked lighting** — one texture per object with the light painted in. AI models arrive with their own UVs and materials that fight that workflow.
4. **Architecture is the easy bit anyway.** Walls, floor, desk surface, shelves = boxes. Boxes take 20 minutes in Blender and don't need AI at all.

**Conclusion: don't outsource the *style* to AI. Outsource the *grunt work*.**

---

## Where AI genuinely earns its place here
| Use | Tool type | Why it's good |
|---|---|---|
| **Design language / concept art** | Image gen (Midjourney, Firefly, Nano Banana, SDXL) | Nail the look in 2D *before* touching 3D. Cheap, fast, iterate 50 times. This is the highest-value AI use in this whole project. |
| **Texture / material generation** | Image gen + tiling tools | Wood grain, poster art, book covers, screen contents |
| **One-off hero props** | Text/image-to-3D (Meshy, Tripo, Rodin) | The 2-3 weird personal objects that don't exist in any asset pack |
| **Photo -> 3D of my real stuff** | Image-to-3D / photogrammetry | Turn an actual object from my desk into a model. *Very* on-theme. |
| **Code + shaders + glue** | Claude / LLM | Three.js setup, raycasting, camera transitions, loaders, the 2D fallback |
| **Copy drafting** | LLM | Project writeups, about text |

---

## The three realistic routes to a finished room
### Route A — CC0 asset kits + light kitbashing ⭐ *recommended start*
Grab a **stylistically unified low-poly pack** and arrange it. No modelling, just moving boxes around.
- Sources: **Kenney.nl**, **Quaternius**, **Poly Pizza**, **Poly Haven** (all CC0/free), Sketchfab (check licences)
- Pros: consistent style out of the box, game-ready, fastest path to something real
- Cons: it's someone else's style, not *mine* — mitigate by recolouring everything to my own palette and adding 2-3 custom personal objects
- Blender needed: minimal — import, arrange, recolour, export

### Route B — Simple modelling + AI textures
Build boxy furniture myself (genuinely easy at this style level), let AI make the textures/posters/screen art.
- Pros: fully my style, small files, bakes cleanly
- Cons: needs ~a weekend of Blender fundamentals
- The video I linked teaches exactly this path

### Route C — Pre-rendered, no realtime 3D at all
Render the room as a few high-quality **still images** (from Blender, or purely from AI image gen), then overlay clickable hotspots in plain HTML/CSS.
- Pros: gorgeous, loads instantly, works on every device, zero Three.js
- Cons: can't freely orbit — you snap between fixed views (still feels great, think point-and-click adventure games)
- **This is the escape hatch if 3D stalls.** Do not forget it exists.

**Plan: start at A, steal from B, keep C in my back pocket.**

---

## Non-negotiable technical checklist for any asset that enters the room
- [ ] Exported as **.glb**, compressed with **Draco** or **meshopt**
- [ ] Textures in **KTX2/basis** or at worst compressed WebP, 1-2k max
- [ ] **Baked lighting** where possible — realtime lights are the #1 perf killer
- [ ] Whole-scene budget: aim **under 5 MB total**, hard ceiling 10 MB
- [ ] Recoloured to my palette -> [[Style-Language]]

## Cost check before committing
- AI 3D tools: mostly credit-based subscriptions. Do a **free-tier test with one prop** before paying anything.
- Asset kits: free.
- Blender: free.
- **Action:** test-drive one text-to-3D tool with a single object and judge the result honestly against Route A. -> [[Open-Questions]]

Links: [[Concept — The House]] · [[Style-Language]] · [[Tech-Stack]]
