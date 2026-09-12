# Session Log

> One block per sitting. Future-me reads the last entry to reload context in 30 seconds.

## 2026-09-12 (session 6) - approach locked
- **Did:** Turned the research into a decision -> [[The-Approach]]
- **THE PLAN:** I write the website code; the **Blade** generates the 3D assets; nothing gets bought.
- Recorded the division of labour, the per-object asset loop, the asset source priority (code geometry -> CC0 kits -> local generation), and six rules that keep it from going wrong.
- Dropped the Mac mini question - not part of this project.
- **Next time:** style lane + reference board, then the Three.js code-geometry test.

---

## 2026-09-12 (session 5) - hardware answered
- **Did:** Confirmed hardware: desktop 2070 Super 8GB + Razer Blade 14 3070 Ti 8GB -> [[My-Hardware-and-Local-Generation]]
- **Answered:** **I never need to pay for AI 3D generation.** 8GB covers shape-only generation locally.
- **Happy accident:** texture generation needs ~21GB and I *don't want it* - flat palette colours are the style. The half I can't run is the half I'd throw away.
- **Key decision:** generate on the **Blade**, not the desktop - equal VRAM but Ampere handles modern ML tooling far better than Turing.
- **Learned:** Hunyuan3D 2.1 officially wants ~10GB for shape; INT8 + `--low_vram_mode`, or the Hunyuan3D-2GP fork, bring it to 8GB. TripoSR is the low-pain first try.
- **Guardrail set:** one evening budget for local AI setup. If it fights back, fall back to CC0 kits + code geometry. The room does not depend on it.

---

## 2026-09-12 (session 4) - AI model generation survey
- **Did:** Mapped seven routes for AI-made models -> [[AI-Model-Generation-Options]]
- **Key insight:** raw text-to-3D prop-by-prop is the *trap* - it is the obvious route and the one that wrecks style consistency.
- **Key insight:** **image-to-3D** beats text-to-3D because the style gets decided once in 2D, cheaply, then the 3D follows.
- **Underrated option found:** have AI write **Three.js/Blender-Python code** that builds boxy furniture. Free, tiny files, perfectly consistent, and it plays to my strengths as a coder.
- **To check:** my GPU VRAM. 6GB+ means free unlimited self-hosted generation (Hunyuan3D / TRELLIS).
- **Next time:** try the code-geometry route before spending anything.

---

## 2026-09-12 (session 3) - budget + skill floor
- **Did:** Answered what this costs and how little Blender I can get away with -> [[Budget-and-Minimum-Blender]]
- **Key decision:** **Parked the Higgsfield video entirely.** It makes video, not rooms, and it is the only expensive thing on the list.
- **Key decision:** **Skip lighting baking for v1.** Hardest Blender skill; flat colours + Three.js lights look fine on stylised low-poly. Baking becomes a Phase 4 upgrade.
- **Key decision:** Blender is only a *furniture arranger* - 6 operations, ~2 hours, no modelling.
- **Learned:** whole project ships for zero cost (Blender + CC0 kits + Three.js + free hosting). Domain optional.
- **Learned:** if I ever buy AI credits, **burst for one month and cancel** rather than subscribing while still planning. Meshy free tier is CC BY 4.0 - needs attribution.
- **Next time:** style lane + reference board, then install Blender and practise the 6 ops on a Kenney kit.

---

## 2026-09-12 (session 2) - the concept landed
- **Did:** Locked the big idea - the site is a small house/room that represents me and how my brain is organised; every object is both a piece of me and a nav item. Added [[Concept — The House]], [[Style-Language]], [[3D-Asset-Pipeline]] and rewrote [[Roadmap]] around it.
- **Key decision:** scope is **one room for v1**, not a house. More rooms are expansion packs.
- **Key decision:** build the plain 2D content site *first* (Phase 1) so the 3D can never be the reason nothing ships. It doubles as the mobile version.
- **Learned:** the reference video is a diorama you orbit and click, not a walkable FPS - much more achievable. Its real trick is **baked lighting** in Blender.
- **Learned:** AI's best use here is the **2D style board and textures**, not generating the whole room - AI props drift in style, which is the one thing this concept can't afford.
- **Next time:** answer the personality questions in [[Style-Language]], pick a lane, make a reference image board.
- **Blocked on:** nothing. The next step costs an hour and no money.

---

## 2026-09-12 (session 1)
- **Did:** Set up this Obsidian vault — brief, idea dump, backlog, roadmap, decisions, inbox. Filed the Blender × Higgsfield video transcript as a resource.
- **Learned:** The motion-hero idea is real but expensive; parked at Phase 5.
- **Next time:** Start with [[Now-Next-Later]] → dump ideas, then answer the audience question in [[Brief]].
- **Blocked on:** nothing.

---
