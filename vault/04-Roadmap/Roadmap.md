# Roadmap — The Room 🗺️

> Phases, not dates. Each phase ends in something I could show someone.
> **Golden rule: the room is the reward, the content is the job.** Build the boring content site first so the 3D can never become the reason nothing ships.
> Revised 2026-09-12 after the house/room concept -> [[Concept — The House]]
> **Approach is locked:** I write the code, the Blade generates the assets, nothing gets bought. -> [[The-Approach]]

---

## Phase 0 — Decide the feel (1-2 short sessions)
**Goal:** know what I'm making before I make it.
- [ ] Watch the reference video once at speed, no building -> [[Video — Cute Room Portfolio (Blender + Threejs)]]
- [ ] Answer the personality questions in [[Style-Language]]
- [ ] Pick a style lane + palette
- [ ] Build one **image reference board** (AI image gen) — the visual source of truth
- [ ] Draw the room on paper. Badly. Where is the desk, the shelf, the window?
- [ ] Decide the object -> content map -> [[Concept — The House]]

**Done when:** I have one picture and one list that say "this is the room."

---

## Phase 1 — The boring site that actually works (2-3 sessions)
**Goal:** a real, live, useful site with zero 3D. This is the safety net *and* the mobile version forever.
- [ ] Scaffold + deploy an ugly one-pager to a public URL
- [ ] Write the bio and 3 project writeups -> [[Content-Plan]]
- [ ] Contact links
- [ ] Make it decent on mobile

**Done when:** I could put the URL on a CV today and not wince. **Do not start Phase 3 before this is true.**

---

## Phase 2 — One object, on screen, in a browser (1-2 sessions)
**Goal:** de-risk the whole 3D idea cheaply before committing weeks. **All code, no asset pipeline yet.**
- [ ] Three.js scene running in the site
- [ ] **Try code geometry first** — a desk and shelf built from Three.js primitives in my palette. If this looks good enough, a chunk of the room needs no pipeline at all.
- [ ] Load a single .glb (from a free kit — don't model anything yet)
- [ ] Orbit the camera around it
- [ ] Click it -> something happens
- [ ] Check it on my phone

**Done when:** I've proven I can do this. If this phase is miserable, switch to **Route C: pre-rendered rooms** -> [[3D-Asset-Pipeline]]

---

## Phase 3 — Build the room (3-5 sessions, the big one)
**This is where the Blade comes in.** Follow the asset loop in [[The-Approach]] — one object per pass.
- [ ] One evening: set up local generation on the Blade (TripoSR first, then Hunyuan3D shape-only if needed) -> [[My-Hardware-and-Local-Generation]]
- [ ] Assemble the room from code geometry + kit assets, all recoloured to my palette
- [ ] Generate the 2-3 custom personal objects on the Blade
- [ ] Bake the lighting
- [ ] Export optimised .glb (Draco, under 5 MB) -> checklist in [[3D-Asset-Pipeline]]
- [ ] Hook up raycast clicks on the mapped objects
- [ ] Hover states so clickable things look clickable
- [ ] Loading screen

**Done when:** I can click the desk and my projects appear.

---

## Phase 4 — Make it feel like a home (2-3 sessions)
This is where it stops being a tech demo.
- [ ] Smooth camera transitions between objects
- [ ] Content panels styled to match the room's world
- [ ] Little motion: a slowly spinning chair, a flickering screen, curtains
- [ ] Sound? (optional, muted by default, always)
- [ ] One easter egg that rewards poking around

---

## Phase 5 — Ship it properly (1-2 sessions)
- [ ] Mobile: serve the 2D site or a lighter scene — decide and test
- [ ] `prefers-reduced-motion` + keyboard access
- [ ] Lighthouse pass, meta tags, OG image (a render of the room!)
- [ ] Custom domain
- [ ] Share it

---

## Phase 6 — Expansions (forever, never blocking)
- [ ] A second room behind a door
- [ ] Day/night toggle
- [ ] Snippets drawer
- [ ] Seasonal decoration changes
- [ ] Whatever's top of [[Idea-Dump]] that week

---

## Rules that protect this project
1. **Phase 1 ships before Phase 3 starts.** Non-negotiable.
2. If a phase stalls twice, cut its scope in half.
3. One room finished beats three rooms started.
4. If the 3D becomes a slog for 3 sessions running, take Route C and still have a beautiful site.
