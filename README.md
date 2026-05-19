# cesium-playground 🌍

A frontend learning project to display satellites in deferred time on an interactive 3D globe using **CesiumJS** and **satellite.js**.

This sandbox prepares the integration of the `SatelliteViewer.vue` component into the full redesign of [orekit.org](https://www.orekit.org).

---

## Goals

- Learn CesiumJS in vanilla HTML/JS before integrating it into Vue 3 / Nuxt
- Manipulate TLE (Two-Line Element) data on the frontend
- Prepare the connection with the Orekit project's FastAPI backend

---

## Roadmap

| Step | Description | Status |
|------|-------------|--------|
| 1 | Display a CesiumJS globe in a simple HTML page | ✅ Done |
| 2 | Place a fixed point on the globe (manual position) | ✅ Done |
| 3 | Load TLE data and compute a position with satellite.js | ✅ Done |
| 4 | Display a real satellite on the globe (ISS) | ✅ Done |
| 5 | Display multiple satellites from a Celestrak group | ✅ Done |
| 6 | Add a time slider (move forward/backward in time) | ✅ Done |
| 7 | Connect the globe to the Orekit FastAPI TLE endpoint | 🔧 In progress |

---

## Tech Stack

- **CesiumJS** — 3D globe rendering (WebGL)
- **satellite.js** — client-side TLE propagation (SGP4 algorithm)
- **HTML / CSS / JS vanilla** — no framework, for learning purposes
- *(future)* **Vue 3 / Nuxt 3** — integration into the real Orekit project

---

## Prerequisites

- A modern browser (Chrome or Firefox recommended)
- Python 3 (to run the local dev server)
- A free **Cesium Ion** token: [ion.cesium.com](https://ion.cesium.com)

---

## Getting Started

```bash
git clone <repo-url>
cd cesium-playground
python3 -m http.server 8080
```

Then open **http://localhost:8080** in your browser.

> ⚠️ Do not open `index.html` directly with `file://` — CesiumJS requires an HTTP server to load its assets.

---

## Project Structure

```
cesium-playground/
├── README.md
├── index.html          # Step 1 — Basic globe
├── step2.html          # Step 2 — Fixed point
├── step3.html          # Step 3 — TLE position calculation
├── step4.html          # Step 4 — ISS on the globe
├── step5.html          # Step 5 — Satellite group
├── step6.html          # Step 6 — Time slider
└── step7.html          # Step 7 — FastAPI connection
```

> Each step is a standalone HTML file to make progression and code review easier.

---

## Project Context

This playground is part of the full redesign of [orekit.org](https://www.orekit.org), built as a two-person final project.

- Backend: Python / FastAPI / PostgreSQL / SQLAlchemy — *Virginie*
- Frontend: Nuxt 3 / @nuxt/content / CesiumJS — *Allix*
- Code freeze: **July 6, 2026**
- Exam: **July 21, 2026**

---

## Resources

- [CesiumJS Documentation](https://cesium.com/learn/cesiumjs/ref-doc/)
- [satellite.js on npm](https://www.npmjs.com/package/satellite.js)
- [Celestrak — TLE data source](https://celestrak.org)
- [Orekit — orbital mechanics library](https://www.orekit.org)
