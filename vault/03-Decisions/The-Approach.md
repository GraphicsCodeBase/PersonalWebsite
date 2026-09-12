# The Approach (LOCKED 2026-09-12)

> This is the decided way I'm building the room. Not a list of options any more - the options are settled. If I find myself re-arguing this at midnight, re-read it instead.

---

## The one-sentence version
**I write the website code. The Blade generates the 3D assets. Nothing gets bought.**

---

## Division of labour
| Job | Where | Why |
|---|---|---|
| **Website code** - Three.js scene, camera, raycast clicks, UI, the 2D fallback site | Desktop, with AI assistance | This is my actual skill. Code is the part I can move fast on and the part AI helps most reliably with. |
| **3D asset generation** - the props and furniture | **Razer Blade 14 (3070 Ti, Ampere)** | Ampere handles modern ML tooling far better than the desktop's Turing card, despite both being 8GB -> [[My-Hardware-and-Local-Generation]] |
| **Arranging the room** | Blender, 6 operations only | Interior decorating, not modelling -> [[Budget-and-Minimum-Blender]] |
| **Style, textures, poster art, screen contents** | AI image generation | Flat 2D art carries most of the personality and costs nothing |

**Total spend: zero.** Optional custom domain later, ~10-15 per year.

---

## The asset workflow (the loop I'll repeat per object)
1. **Decide the object** from the object -> content map -> [[Concept — The House]]
2. **Concept image first** - generate a 2D image of the object in my locked style. Cheap, fast, and this is where style consistency is won -> [[Style-Language]]
3. **Image -> 3D on the Blade** - shape only, no textures (textures need ~21GB and I don't want them anyway)
4. **Clean + recolour** in Blender to my palette. Every asset, no exceptions - the shared palette is what makes mixed-source assets look like one room
5. **Export .glb** with Draco compression
6. **Drop into the repo** and hook it up in code with a raycast click handler
7. **Check the scene budget** - under 5 MB total, 10 MB hard ceiling

Repeat. Each pass adds one working object to the room.

## Asset sources, in order of preference
1. **AI-written code geometry** - boxy furniture built from Three.js primitives. Free, tiny, perfectly consistent, no pipeline at all. *Try this first for the room shell, desk, shelves.*
2. **CC0 kits** (Kenney, Quaternius, Poly Pizza) recoloured to my palette
3. **Locally generated meshes on the Blade** - for the organic/personal things nothing else covers
4. Paid AI - **only** as a one-month burst, later, if ever

---

## Rules that keep this from going wrong
1. **Ship the plain 2D content site before building the room.** It's the mobile version and the safety net. -> [[Roadmap]] Phase 1
2. **Skip lighting baking for v1.** Flat colours + Three.js lights. Baking is Phase 4 polish.
3. **Recolour everything to one palette.** This is the single biggest defence against AI style drift.
4. **One evening budget for local AI setup.** If it fights back, fall back to kits and code geometry. The room does not depend on it.
5. **Buy nothing.** If I'm shopping for tools or hardware, I'm procrastinating.
6. **One room, finished.** More rooms are expansions, shipped later.

---

## What I do *not* need
- ~~Higgsfield~~ - makes video, not rooms. Parked.
- ~~AI texture generation~~ - the style wants flat palette colours.
- ~~Advanced Blender~~ - 6 operations covers it.
- ~~Any subscription~~ - free tools and my own GPU cover the whole project.

Links: [[Concept — The House]] · [[Roadmap]] · [[My-Hardware-and-Local-Generation]] · [[AI-Model-Generation-Options]] · [[Budget-and-Minimum-Blender]]
