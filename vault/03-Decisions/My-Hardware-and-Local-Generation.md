# My Hardware -> Local AI Generation Plan

> Checked 2026-09-12.
> **Machines:** Desktop RTX 2070 Super (8GB, Turing) · Razer Blade 14, RTX 3070 Ti laptop (8GB, Ampere)
> **Verdict: I can generate 3D models locally for free. No subscription needed.**

---

## The headline
8GB on both cards. That is enough for **shape-only generation** with low-VRAM settings, and not enough for comfortable **texture generation**.

**That limitation does not matter for this project.** The room is stylised low-poly with flat colours from my own palette -> [[Style-Language]]. AI-generated PBR textures would actively fight the look and get thrown away. I want bare meshes, and bare meshes are exactly what 8GB delivers.

Getting the cheap half for free and not needing the expensive half is a good position to be in.

---

## Use the Blade for generation, not the desktop
Equal VRAM, but **not equal cards** for this job:

| | Desktop 2070 Super | Blade 14 / 3070 Ti |
|---|---|---|
| VRAM | 8GB | 8GB |
| Architecture | Turing (2018) | **Ampere (2020)** |
| bf16 support | Weak | **Yes** |
| Modern attention kernels (flash-attn etc.) | Often Ampere+ only | **Supported** |
| Risk of "unsupported GPU" dependency pain | Higher | Lower |

**-> Generate on the Blade.** Watch thermals; a laptop will throttle on a long batch. Plug it in, prop it up, don't do it on a duvet.
**-> Use the desktop for Blender, the browser, and dev work**, which neither card will struggle with at all.

---

## Actual VRAM numbers for Hunyuan3D 2.1
Official requirements are heavier than the marketing suggests:

| Task | Official VRAM |
|---|---|
| Shape generation | ~10 GB |
| Texture generation | ~21 GB |
| Shape + texture | ~29 GB |

**8GB gets there anyway, via:**
- `--low_vram_mode` flag - activates offloading
- **INT8 quantisation** - specifically recommended for 8GB cards (FP8/FP16 also available, more experimental)
- **Shape-only generation** - skips the expensive half entirely (and this is what I want)
- **Hunyuan3D-2GP** - community fork using MMGP offloading, runs shape generation on as little as 6GB
- Close the browser and other GPU apps first; they quietly eat VRAM

## Lighter alternatives worth trying first
- **TripoSR** - very lightweight image-to-mesh, far below 8GB, near-instant. Good first experiment because setup pain is minimal.
- **TRELLIS 2** - higher quality, heavier. Likely a stretch at 8GB; try after the others.

---

## Fallback: rent a GPU instead of subscribing
If local setup fights back, rent GPU time by the hour (Runpod, Vast.ai and similar) rather than buying a monthly plan. A big card is typically well under a pound an hour, so an evening of generating every prop I need costs about the price of a coffee, versus ~20 USD/month for a subscription I'd barely use. *Check current rates before committing.*

---

## The plan
1. **Try [[AI-Model-Generation-Options]] route #5 first** - AI-written Three.js/Blender-Python geometry. Zero setup, zero VRAM, perfectly style-consistent. If boxy furniture from code looks good enough, I may never need any of this.
2. If I want real meshes: **TripoSR on the Blade** as the low-pain first experiment.
3. If I want better quality: **Hunyuan3D 2.1, shape-only, INT8 + `--low_vram_mode`**, or the 2GP fork.
4. Recolour every output to my palette before it enters the room. Non-negotiable.
5. **Spend nothing.** If local generation is a dead end, rent an hour of GPU, not a year of subscription.

## Reality check before sinking an evening into setup
Local AI setup on Windows can be genuinely annoying (Python versions, CUDA, dependency hell). Budget **one evening** for it. If it isn't working by the end of that evening, fall back to CC0 kits and code-generated geometry - the room does not depend on this working. -> [[3D-Asset-Pipeline]]

Links: [[AI-Model-Generation-Options]] · [[Budget-and-Minimum-Blender]] · [[3D-Asset-Pipeline]]
