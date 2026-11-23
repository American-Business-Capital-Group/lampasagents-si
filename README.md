# Lampas SI — Standalone Site (Phase 2, v1.00)

Lampas's own front door: a hand-built static site (plain HTML/CSS/JS, no
framework, no build step) for the recursive agentic engine on the Pyr Neural
Network. It talks to the **same live Prometheon SI gateway** (Alienware,
port 8811) and the same accounts as prometheon.si — one backend, two front
doors. The gateway client (`docs/gateway-client.js`) is byte-identical to
the Ignis bundle's copy.

## Repo target

- **Repository:** `American-Business-Capital-Group/lampasagents-si`
- **GitHub Pages source:** `/docs` on the default branch (the `docs/` folder
  in this directory is the complete publish bundle / site root)
- **Custom domain:** `lampasagents.si` (`docs/CNAME`, exact)
- **DNS step:** in the coordinator's `PUBLISH_STEPS.md` — not performed by
  this build.

## Bundle contents (`docs/`)

| File | Purpose |
|---|---|
| `index.html` | Home — what Lampas is, the Fence, pilot status stated plainly |
| `how-it-works.html` | ROMA pattern, the Fence check, depth/budget governance, staging vs production |
| `console.html` | Login (gateway auth) + run console locked to platform `lampas`, Fence panel from gateway `/health` |
| `gateway-config.js` | Gateway discovery candidates (`window.PROMETHEON_GATEWAYS`); coordinator rewrites the `FUNNEL_URL_PENDING` entry |
| `gateway-client.js` | Shared gateway client — identical file in both Phase 2 bundles |
| `site.css` | Brand Kit v3.13 styling (black/gold/chrome, Cinzel + Inter) |
| `logo-lockup.png` | Supplied Prometheon SI logo lockup, unmodified |
| `CNAME`, `.nojekyll` | GitHub Pages custom domain + no-Jekyll markers |

Brand: Brand Kit v3.13, tagline "Powering human achievement.", ticker
"Full Beta Release 2/1/2027", footer "v1.00" + the ABCG copyright line.
Not announced anywhere; the only external calls are the gateway and
Google Fonts.
