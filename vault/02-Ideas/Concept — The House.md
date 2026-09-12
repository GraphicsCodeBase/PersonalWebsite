# Concept — The House 🏠

> **The core idea:** you don't browse my site, you walk into my home. The space *is* the person — how my brain is organised, what I care about, my style. Every object is a piece of me and doubles as navigation.

Status: 🟢 This is now the spine of the project. Everything else serves it.
Reference: [[Video — Cute Room Portfolio (Blender + Threejs)]]

---

## Why this works
A normal portfolio says "here are my projects." A room *shows* how you think without telling. The visitor explores instead of scrolling, and exploration is memorable — which is the entire point of a personal site.

## The one-line pitch
*"A little house that's a map of my head — poke around it."*

---

## Scope decision: room first, house later
A full walkable multi-room house is a 6-month project. **One really good room is a 4-6 week project and hits 90% of the emotional impact.**

- **v1 — one room.** The room. Orbit/look around, click objects, content appears.
- **v2 — the room gets deeper.** More interactive objects, day/night, sound, easter eggs.
- **v3 — more rooms.** A door that opens into a second space. Each new room is an *expansion pack*, shipped when I feel like it.

This way I'm never "halfway through a house" — I'm always finished, with optional extras.

---

## Object -> content map (the fun part)
Each object carries a piece of me *and* is a nav item. Brainstorm freely, cut later.

| Object in room | What it represents | What clicking it opens |
|---|---|---|
| Desk + monitor | What I build | **Projects** — the main event |
| Bookshelf | What I've learned / am learning | Reading, courses, resources |
| Corkboard / whiteboard | What's in my head right now | **Now** page — current obsessions |
| Sticky notes / drawer | Fragments, half-thoughts | **Snippets** library |
| Posters / wall art | Taste, interests, humour | About / personality bits |
| Window | Where I am, where I'm going | Location, what's next, goals |
| Door / mailbox | Reaching me | Contact, GitHub, links |
| Something odd on the shelf | The thing that makes me *me* | An easter egg — a hobby, a joke, a story |

**Prompt for me to answer:** what 3 objects would someone actually find in my real room that say the most about me? Those go in first. -> [[Open-Questions]]

## Rules for the metaphor
- Every object is either **clickable and meaningful** or **set dressing** — nothing in between. Fake-clickable objects feel broken.
- Clickable things must *look* clickable (hover glow, slight lift, cursor change).
- The room must answer "who is this person and can they code" in 40 seconds even if the visitor clicks nothing.
- Cosy > impressive. The emotional target is *someone's home*, not a tech demo.

---

## Interaction model (pick one — this drives everything)
| Model | Feel | Cost | Mobile |
|---|---|---|---|
| **Orbit diorama** (like the video) | Dollhouse you spin and poke | Low | Good |
| **Fixed camera + transitions** | Cinematic, you snap between viewpoints | Low | Good |
| **Scroll-driven camera path** | Guided tour, storytelling | Medium | OK |
| **Free first-person walk** | Actually "walking in" | High | Bad |

**My lean:** orbit diorama for v1 with *camera snap-to-object* on click. It's the video's proven path, it's phone-friendly, and it still feels like stepping into a space.

---

## Non-negotiables (learned from every 3D portfolio that fails)
- **A 2D fallback site must exist** with the same content. Recruiters open things on phones on trains. -> [[Roadmap]] Phase 2
- Loading screen, and the room must appear in **under ~5 seconds**. Every second past that loses people.
- `prefers-reduced-motion` respected; no forced auto-camera-spin for people who get motion sick.
- Keyboard-navigable content. The 3D can be mouse-only; the *information* cannot.

Links: [[Style-Language]] · [[3D-Asset-Pipeline]] · [[Roadmap]] · [[Brief]]
