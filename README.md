## 📘 Project Overview

**MacBook Landing Page** – a React‑based showcase that combines **Three.js** (via `@react-three/fiber`) and **GSAP** scroll animations.  
The page displays a 3D MacBook model that rotates as the user scrolls, while feature boxes fade/slide in sync with the scroll timeline. It’s a learning sandbox for:

- React + Three.js integration
- GSAP + ScrollTrigger animations in a 3D scene
- Responsive handling with `react-responsive`

---

## 🚀 Getting Started

### Prerequisites

| Tool       | Minimum version |
| ---------- | --------------- |
| Node.js    | 18.x            |
| npm / yarn | 8.x             |
| React      | 18.x            |
| Three.js   | 0.160.x         |
| GSAP       | 3.12.x          |

### Installation

```bash
# clone the repo
git clone https://github.com/your-username/macbook-landing-page.git
cd macbook-landing-page

# install dependencies
npm install   # or `yarn install`
```

### Run locally

```bash
npm run dev   # Vite/Next/CRA dev server (depends on your setup)
```

Open `http://localhost:3000` (or the port shown in the console) to view the landing page.

---

## 🛠️ Core Features

| Feature                    | Implementation                                                                     |
| -------------------------- | ---------------------------------------------------------------------------------- |
| **3D MacBook model**       | Loaded with `@react-three/fiber`; responsive scaling via `react-responsive`.       |
| **Scroll‑driven rotation** | GSAP `timeline` + `ScrollTrigger` attached to `#f-canvas`.                         |
| **Feature boxes**          | Positioned absolutely over the canvas; animated via CSS/GSAP (extendable).         |
| **Video pre‑loading**      | `useEffect` creates hidden `<video>` elements for each feature video to avoid lag. |
| **Suspense fallback**      | Shows a loading message while the GLTF model is being fetched.                     |

---

## 📂 Project Structure (relevant files)

```
src/
├─ components/
│  ├─ Features.jsx          ← main page component (canvas + boxes)
│  ├─ ModelScroll.jsx       ← GSAP + Three.js logic
│  └─ models/
│     └─ Macbook.jsx        ← GLTF model loader
├─ three/
│  └─ StudioLights.jsx      ← HDRI / three‑point lighting setup
├─ store/
│  └─ macbookStore.js       ← Zustand (or similar) for texture state
└─ constants/
   ├─ features.js           ← feature text & video paths
   └─ featureSequence.js    ← ordered video data
```

---

