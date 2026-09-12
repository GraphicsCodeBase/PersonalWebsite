# Budget + The Minimum Blender I Actually Need

> Two questions answered: **how do I use the videos without learning Blender properly**, and **what does this cost me?**
> Prices checked 2026-09-12. Credit-based AI tools change pricing often - re-check before paying.

---

## First: the two videos do different jobs
| Video | What it gives me | Verdict |
|---|---|---|
| **[[Video — Cute Room Portfolio (Blender + Threejs)]]** | The actual build: room -> web, clickable objects | **This is the manual. Follow it.** |
| **[[Video — Blender x Higgsfield Web Visuals]]** | Cinematic AI *video* clips | **Skip for now.** It makes a video, not a room. Also the single most expensive thing on the list. Park until v3. |

Cutting video 2 from the plan saves ~19 USD/month immediately and removes a whole toolchain.

---

## How to use video 1 without learning Blender
The course has two halves. **I only need to properly follow the second half.**

| Half | What it teaches | My plan |
|---|---|---|
| Blender half | Modelling the furniture from scratch | **Mostly skip** - use CC0 kits and just arrange them -> [[3D-Asset-Pipeline]] |
| Three.js half | Loading, camera, raycast clicks, hover, loading screen | **Follow properly** - this is the real skill and it is code, which I am fine with |

### Watch it like this
1. **First pass, 1.5-2x speed, no building.** Just map the pipeline.
2. Note timestamps for exactly three things: **material/colour setup**, **export settings**, **raycasting**.
3. Second pass: build along, but at the modelling sections, import a kit asset instead of modelling it.

---

## The minimum Blender - 6 operations, about 2 hours
This is genuinely all I need to arrange a room from pre-made assets. No modelling, no sculpting, no UV unwrapping, no rigging.

| # | Operation | How |
|---|---|---|
| 1 | Import an asset | File > Import > glTF/FBX/OBJ |
| 2 | Move / rotate / scale | `G` / `R` / `S`, then move mouse, click to confirm. Add `X`/`Y`/`Z` to lock an axis |
| 3 | Duplicate | `Shift+D` |
| 4 | Recolour | Material Properties > Base Color |
| 5 | Delete / select | `X` to delete, click to select, `A` for all |
| 6 | Export | File > Export > glTF 2.0 (.glb), tick **Draco compression** |

**That is interior decorating, not 3D modelling.** Anything harder than this is a signal I have wandered off the plan.

### The one hard part, and how to dodge it
The tutorial **bakes lighting** into textures. Baking is the genuinely fiddly bit (UV unwrapping, bake settings, fixing seams) and it is where people quit.

**For v1: skip baking.** Flat colours + one directional light + ambient light in Three.js looks great on stylised low-poly and costs nothing to set up. Baking is a **Phase 4 polish upgrade**, not a requirement.

-> This single decision removes most of the Blender difficulty.

---

## Three routes, if I want to avoid Blender even further
| Route | What it is | Cost | Trade-off |
|---|---|---|---|
| **A - Blender as a furniture arranger** (chosen) | The 6 operations above | **Free forever** | ~2h learning curve, but zero lock-in and full control |
| **B - Spline** | Browser-based 3D design, drag-and-drop, no Blender at all | Free (3 files, **watermarked** web export) / 12-15 USD per month to remove watermark | Easiest start; heavier runtime, more lock-in, watermark on free |
| **C - Assemble in code** | Load kit props in Three.js, position with x/y/z numbers. Use the free browser-based three.js editor to drag them into place | **Free** | No 3D app to learn, but positioning by numbers is tedious |

**Chosen: A.** Free, no watermark, no subscription, and the 2 hours pay for themselves.

---

## The money

### The whole project, realistically: **0**
| Thing | Cost |
|---|---|
| Blender | Free |
| CC0 asset kits (Kenney, Quaternius, Poly Pizza) | Free |
| Three.js | Free |
| Hosting (GitHub Pages / Vercel / Cloudflare Pages) | Free |
| Custom domain | Optional, ~10-15 per year |

**Total to ship the room: nothing, or ~12 per year if I want a proper domain.**

### Optional AI spend (only if I want custom props)
| Tool | Free tier | Paid | Worth it? |
|---|---|---|---|
| **Meshy** (text/image -> 3D) | 100 credits/month = ~5 models (20 credits each). Output is **CC BY 4.0 - needs attribution** | 20 USD/mo Pro = 1,000 credits (~50 models) + private licence | Only when I know exactly which props I need |
| **Higgsfield** (AI video) | - | 19 USD/mo Starter (270 credits), Plus 47-59, Ultra 99-129 | **No. Not needed for this project.** |
| **Spline** | 3 files, watermarked export | 12 USD/mo annual, 20 for Pro | Only if route B |
| Image gen (style board, textures, posters) | Free tiers are plenty | - | Yes, use it - highest value AI in this project |

### The money-saving tactic: **burst, do not subscribe**
Do not pay monthly while still planning. Build the room with free kits first. *Then*, in one single month, subscribe to one AI 3D tool, generate every custom prop needed in a weekend, export them, and **cancel**. One paid month instead of a year of them.

### Watch the licence
Meshy free tier outputs are **CC BY 4.0** - fine for a personal site, but it needs a credits/attribution line somewhere. Paid tiers give a private licence. Same check applies to any Sketchfab asset.

---

## Decision summary
- Skip the Higgsfield video and its subscription.
- Skip baking for v1 - it is the hardest Blender skill and not needed yet.
- Learn 6 Blender operations, not Blender. ~2 hours.
- Build with free CC0 kits. Zero cost.
- Spend on AI only in one concentrated burst, later, if at all.

Links: [[3D-Asset-Pipeline]] · [[Roadmap]] · [[Tech-Stack]] · [[Concept — The House]]
