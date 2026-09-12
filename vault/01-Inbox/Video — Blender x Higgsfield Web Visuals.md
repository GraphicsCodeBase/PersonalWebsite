---
source: transcript_video.txt (repo root)
type: video transcript / tutorial
relevance: hero visuals, background video, landing page motion
---

# Video — Blender × Higgsfield web visuals

> **PARKED 2026-09-12.** This makes cinematic *video*, not an interactive room. Not needed for the room concept, and Higgsfield starts at ~19 USD/month. Revisit at v3 if I ever want a video hero. -> [[Budget-and-Minimum-Blender]]

## What it covers
A workflow for making **precise, controlled AI video** for website hero sections:
1. Download Blender (free, blender.org) — latest version.
2. Install the Higgsfield Blender plugin + the "Higgsfield Bridge" MCP connector.
3. Block out the scene/camera moves in Blender (this is the *control* part — you decide composition and camera motion instead of hoping the AI guesses).
4. Send it to Higgsfield to render it into a finished-looking video.

**Why it matters here:** it's an answer to "how do people get those slick moving backgrounds on landing pages" without being a motion designer.

## How this could apply to my site
- Hero background loop behind the intro text
- Short looping visual per project card
- A one-off "showreel" clip for the about page

## Reality check before committing
- ⚠️ Cost: Higgsfield is a paid/credits product — check pricing before building around it.
- ⚠️ Performance: video backgrounds are heavy. Budget, poster frame, `preload="none"`, and a static image fallback on mobile.
- ⚠️ Accessibility: must respect `prefers-reduced-motion`; never autoplay with sound.
- ⚠️ Scope: this is a **v3 / polish** item. Do not let it block v1 shipping. → [[Feature-Backlog]]
- Alternative cheaper paths: CSS gradient mesh animation, a Three.js/R3F scene, or a looping SVG.

## Next action
- [ ] Decide: is a motion hero actually part of the brand, or a distraction? → [[Open-Questions]]

Links: [[Design-Inspiration]] · [[Resource-Dump]] · [[Roadmap]]
