# Tech Stack — decisions & open choices

> One line per decision, always with a **why**. This stops me re-arguing the same choice at midnight.

## Decided
| Area | Choice | Why | Date |
|---|---|---|---|
| Version control | Git + GitHub | Already set up in this repo | 2026-09-12 |
| Notes | Obsidian vault in-repo | Plans live next to the code | 2026-09-12 |
| **Overall approach** | I write the code; the Blade generates the assets; nothing gets bought | Plays to my strengths, costs nothing -> [[The-Approach]] | 2026-09-12 |
| **Asset generation machine** | Razer Blade 14 (3070 Ti, Ampere) | Ampere handles ML tooling far better than the desktop's Turing card | 2026-09-12 |
| **Texture approach** | Flat palette colours, no AI textures, no baking for v1 | Suits the stylised look; dodges the hardest Blender skill and the 21GB VRAM wall | 2026-09-12 |
| **Asset priority order** | Code geometry -> CC0 kits -> locally generated meshes | Cheapest and most style-consistent first | 2026-09-12 |
| Budget | Zero, domain optional | Free tools + my own GPU cover everything | 2026-09-12 |

## Undecided (each of these is a candidate for a [[Decision Record]] note)
| Area | Options | Leaning | Blocking? |
|---|---|---|---|
| Framework | Plain HTML/CSS/JS · Astro · Vite + vanilla · Next.js | Vite or Astro | Yes — blocks starting |
| 3D library | **Three.js** · React Three Fiber · Babylon.js · pre-rendered (no 3D) | Three.js (matches the reference video) | Soon |
| Asset source | CC0 kits · own Blender models · AI text-to-3D | Kits first → [[3D-Asset-Pipeline]] | Soon |
| Model format | .glb + Draco/meshopt | .glb | Settled in practice |
| Styling | Vanilla CSS · Tailwind · CSS modules | — | No |
| Hosting | GitHub Pages · Vercel · Netlify · Cloudflare Pages | — | No |
| Domain | Buy one? which registrar? | — | No |
| Content source | Markdown files · hardcoded · CMS | — | No |
| Snippets storage | Markdown + build step · JSON · GitHub Gists API | — | No (v2) |
| Analytics | None · Plausible · Cloudflare · Umami | — | No |

## Quick orientation (my read, not a decision)
- **Plain HTML/CSS/JS** — zero build, zero lock-in, most learning about fundamentals. Gets painful once you have many project pages sharing a layout.
- **Astro** — sweet spot for a content/portfolio site: writes like HTML, ships almost no JS, markdown pages are first-class, can drop in React/Svelte islands later.
- **Next.js** — most job-relevant on a CV, but heaviest for a static portfolio.
- **Vite + vanilla JS** — what the reference video effectively uses. Simplest thing that runs Three.js well. Strong candidate given the 3D is the centrepiece.
- **Three.js vs React Three Fiber** — R3F is lovely *if* I'm already in React. If not, plain Three.js is fewer moving parts and every tutorial (including my reference video) speaks it.
- Hosting for any of them: GitHub Pages is free and already tied to this repo; Vercel/Cloudflare are also free at this size and easier for previews.

## Note on the 3D
The heavy lifting isn't the library, it's **asset discipline** — baked lighting, compressed textures, small .glb files. A well-optimised scene in any library beats a sloppy one in the "best" library. -> [[3D-Asset-Pipeline]]

## Rule of thumb
Pick the boring option unless learning the exciting one **is** the point of the project. If it is, write that down in [[Brief]] as a goal.
