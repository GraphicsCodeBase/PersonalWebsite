# Options for Letting AI Make the Models

> Checked 2026-09-12. The field moves fast - re-verify before paying for anything.
> **The recurring risk with all of these: style drift.** Ten AI props = ten art styles, and a consistent look is the whole point of the room. Every option below is judged on that.

---

## The seven routes

### 1. Text-to-3D (type a prompt, get a mesh)
The obvious one. Type "wooden desk lamp", get a model in seconds.

| Tool | Best at | Free tier | Notes |
|---|---|---|---|
| **Tripo AI** | Speed + clean **low-poly** topology (its Smart Mesh is reportedly ~2s vs minutes elsewhere) | Yes, limited | Aimed at game devs - low-poly output suits this project best |
| **Meshy** | Most production-ready all-rounder; clean meshes, good texturing, easy export | 100 credits/mo (~5 models) | Smoothest UI; 20 USD/mo Pro |
| **Hyper3D Rodin** | Hyper-real *characters/humans* | Limited | Wrong tool for furniture and props |
| **Hunyuan3D (Tencent)** | Open model, high fidelity | Free / self-host | More concept-stage than finished pipeline |

- Good for: quick one-off props
- Bad at: matching an existing style, clean topology for a whole scene
- **Licence trap:** Meshy and Tripo free tiers output **CC BY 4.0** - attribution required for anything published

### 2. Image-to-3D (the better version of #1)
Generate or draw a concept image first, *then* convert it to 3D.

**This is the fix for style drift.** Make all the concept images in one AI image session with one consistent prompt style, then convert them all. The look is decided in 2D where iteration is free and fast, and the 3D just follows.

- Supported by Meshy, Tripo, Rodin, Hunyuan3D, TRELLIS
- **Recommended as the default AI route for this project**

### 3. Photo-to-3D of my actual stuff
Photograph a real object from my desk, convert it to a model.

- Wildly on-theme: the room literally contains *my* things
- Same tools (image-to-3D), or photogrammetry apps
- Best reserved for the 2-3 signature personal objects -> [[Concept — The House]]

### 4. Self-hosted open models (free, if I have the GPU)
Run **Hunyuan3D 2.1**, **TRELLIS 2**, or **TripoSR** on my own machine.

- Cost: **zero**, unlimited generations, no licence strings
- Needs: NVIDIA GPU. Roughly **6GB VRAM** for shape only, **12-16GB** for shape + texture
- Or rent GPU time by the second instead of subscribing
- **Open question: do I have a GPU that clears this bar?** -> [[Open-Questions]]

### 5. AI writes *code* that builds the geometry ⭐ underrated
Stylised furniture is boxes, cylinders and rounded corners. That is code. Ask an LLM for Three.js geometry or a Blender Python script, and get a desk, shelf and lamp generated procedurally.

- **Free, infinitely tweakable, and perfectly style-consistent** (same code, same proportions, same palette everywhere)
- Tiny file sizes - no meshes to download at all
- Plays to my actual strength: I read code, not topology
- Limit: fine for boxy/simple, useless for organic shapes (a plant, a cat, a crumpled hoodie)
- **Strong candidate for the room shell and basic furniture**, with AI meshes only for the tricky organic props

### 6. AI driving Blender directly (MCP / plugins)
Connect an LLM to Blender via an MCP bridge so it manipulates the scene by instruction - "place a lamp on the desk, rotate the chair 30 degrees". The Higgsfield video used the same pattern for its own bridge.

- Removes the "learn the UI" problem without removing Blender's power
- Still experimental and fiddly to set up; expect to babysit it
- Worth one evening of experimentation, not a foundation to depend on

### 7. AI for everything *except* the meshes
Skip AI geometry entirely. Use free CC0 kits for shapes, and AI for:
- The **style reference board** (highest-value AI use in this project)
- **Textures**: wood, fabric, wallpaper
- **Poster art, book covers, screen contents** - all flat images, all trivially AI-generated, and all the stuff that actually carries personality
- Code glue, copy, project writeups

**This is the cheapest and most reliable path to a room that looks like a coherent place.**

---

## Ranked for *this* project
| # | Route | Cost | Style consistency | Verdict |
|---|---|---|---|---|
| 1 | **#7 AI for textures/art + CC0 kits for shapes** | Free | Excellent | **Start here** |
| 2 | **#5 AI-generated code geometry** | Free | Excellent | Best fit for my skills - try early |
| 3 | **#2 Image-to-3D from consistent concept art** | Free tier, then ~20/mo | Good if disciplined | For the signature props |
| 4 | **#4 Self-hosted open model** | Free w/ GPU | Good | If the GPU clears the bar |
| 5 | #3 Photo-to-3D of my own objects | Free tier | Variable | 2-3 hero objects only |
| 6 | #6 AI driving Blender | Free | n/a | One evening experiment |
| 7 | #1 Raw text-to-3D, prop by prop | Credits | **Poor** | The trap. Avoid as a main strategy |

## The rule that makes any of these work
Whatever the source, **recolour every asset to my one palette** before it enters the room. A single shared palette will hide a multitude of style mismatches. -> [[Style-Language]]

## Next actions
- [ ] Check my GPU VRAM -> decides whether route #4 is free-and-unlimited
- [ ] Try route #5 first: ask for a Three.js desk + shelf in my palette, see if the look is acceptable
- [ ] Do not pay for anything until the room exists in rough form -> [[Budget-and-Minimum-Blender]]

Links: [[3D-Asset-Pipeline]] · [[Budget-and-Minimum-Blender]] · [[Style-Language]] · [[Concept — The House]]
