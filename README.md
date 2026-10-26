<div align="center">
  <img src="https://raw.githubusercontent.com/islomf2010-dot/islomf2010-dot/main/assets/banner.svg" alt="Creative Technologist Studio Banner" width="100%" />
</div>

<br/>

## Introduction

I am a **Creative Technologist** building real-time graphics, cinematic web experiences, and interactive software systems.

My work centers on the intersection of mathematical procedural generation, custom shader pipelines, physical simulation, and low-latency interaction design. Rather than assembling template interfaces or loading multi-megabyte static 3D models, I design lightweight, in-browser graphics systems where visual geometry, lighting, and acoustic synthesis are computed dynamically at runtime.

---

## Selected Work

### 01. AFTERLIGHT — The World Between Frames
**An interactive cinematic WebGL film in six acts, rendered within a single WebGL context with zero downloaded assets.**

[![AFTERLIGHT Preview](https://raw.githubusercontent.com/islomf2010-dot/afterlight/main/docs/banner.png)](https://islomf2010-dot.github.io/afterlight/)

* **Live Demonstration:** [islomf2010-dot.github.io/afterlight](https://islomf2010-dot.github.io/afterlight/)
* **Repository:** [github.com/islomf2010-dot/afterlight](https://github.com/islomf2010-dot/afterlight)
* **Verified Technologies:** `Three.js` · `React Three Fiber` · `@react-three/postprocessing` · `GLSL Shaders` · `Web Audio API` · `GSAP / Lenis` · `Vitest` · `Playwright`
* **Architectural Differentiator:** 
  * **Runtime Hardware Probing & Zero-Asset Synthesis:** Executes a device capability probe at boot (`detectWebGL()`, concurrency, memory, pointer heuristics) to configure a safe GPU budget or gracefully route unaccelerated devices to a readable view. All procedural ocean surfaces (Gerstner waves), simplex noise fog, 2,400 reassembling mesh fragments, and multi-oscillator acoustic drones are generated in memory without external asset requests.

---

### 02. AFTERFORM — Generative Architecture Studio
**An interactive 3D studio algorithmically composing abstract brutalist and minimalist structures from pseudo-random seeds.**

[![AFTERFORM Hero](https://raw.githubusercontent.com/islomf2010-dot/afterform/main/docs/hero.png)](https://islomf2010-dot.github.io/afterform/)

* **Live Demonstration:** [islomf2010-dot.github.io/afterform](https://islomf2010-dot.github.io/afterform/)
* **Repository:** [github.com/islomf2010-dot/afterform](https://github.com/islomf2010-dot/afterform)
* **Verified Technologies:** `Three.js` · `React Three Fiber` · `InstancedMesh` · `Zustand` · `TypeScript` · `Vite` · `Vitest` · `Playwright`
* **Architectural Differentiator:**
  * **Constrained Spatial Grammar & Single-Draw-Call Instancing:** Implements strict modular grid coordinates (`CELL = 2.0m`, `STOREY = 1.15m`) with allocated volumetric budgets for enclosures, bridges, and gateways. Renders hundreds of geometric elements through batched `InstancedMesh` matrices while supporting real-time material parameter mutation (concrete roughness, glass transmission, procedural stone).

---

### 03. Ferrari F40 — The Reveal
**A scroll-scrubbed cinematic study examining the 1987 Ferrari F40 through a frame-accurate, deterministic camera walk.**

[![Ferrari F40 Key Art](https://raw.githubusercontent.com/islomf2010-dot/ferrari-f400/main/public/media/f40-keyart.jpg)](https://ferrari-f400.vercel.app)

* **Live Demonstration:** [ferrari-f400.vercel.app](https://ferrari-f400.vercel.app)
* **Repository:** [github.com/islomf2010-dot/ferrari-f400](https://github.com/islomf2010-dot/ferrari-f400)
* **Verified Technologies:** `GSAP ScrollTrigger` · `Custom H.264 Video Pipeline` · `React` · `TypeScript` · `Vite` · `Playwright`
* **Architectural Differentiator:**
  * **Sub-Pixel Clock Synchronization:** Replaces continuous video playback with normalized scroll distance as the exclusive clock. A single GSAP scrub loop drives video frame seeking (thresholded at `1/48s` to prevent decoding churn), synchronized typography opacities, and studio lighting cues with zero WebGL overhead, backed by automated `prefers-reduced-motion` fallbacks.

---

### 04. School 13 — Roguelite Survival Engine
**A 2D top-down survival game engine featuring zero-allocation object pools, procedural industrial breakbeat audio, and adaptive AI dialogue.**

[![School 13 Title Art](https://raw.githubusercontent.com/islomf2010-dot/school-13/main/public/assets/ui/title_key_art.png)](https://islomf2010-dot.github.io/school-13/)

* **Live Demonstration:** [islomf2010-dot.github.io/school-13](https://islomf2010-dot.github.io/school-13/)
* **Repository:** [github.com/islomf2010-dot/school-13](https://github.com/islomf2010-dot/school-13)
* **Verified Technologies:** `HTML5 Canvas 2D` · `Web Audio API` · `Google Gemini API` · `TypeScript` · `React 19` · `Vite` · `Node.js Test Runner`
* **Architectural Differentiator:**
  * **Zero-Allocation Pools & Step-Sequenced Synthesizer:** Operates a fixed 60 Hz canvas loop utilizing pre-allocated object arrays (420 projectiles, 420 particles, 110 decals) to eliminate Garbage Collection pauses during combat. An integrated 136 BPM procedural step sequencer dynamically adjusts tempo and Biquad lowpass filtering during time-dilation mechanics.

---

## Technical Focus

| Domain | Verified Stack & Methodologies |
| :--- | :--- |
| **Creative Development** | Mathematical procedural generation, deterministic PRNG seed architectures, generative spatial massing, cinematic scrollytelling. |
| **3D Graphics & Rendering** | Three.js, React Three Fiber (R3F), Custom GLSL Shaders (Vertex & Fragment), `InstancedMesh` batching, procedural UV mapping, postprocessing pipelines. |
| **Frontend Engineering** | React 19, TypeScript (strict mode), Zustand state management, HTML5 Canvas 2D, Vite production bundling, modern CSS architecture. |
| **Animation & Interaction** | GSAP (ScrollTrigger & Timeline scrubbing), Lenis smooth scroll orchestration, pointer and touch interaction models, frame-accurate seeking. |
| **Tools & Testing** | Vitest (unit & deterministic math assertions), Node.js native test runner (`node:test`), Playwright (headless browser E2E), Linux / Arch environment. |

---

## Engineering Approach

1. **Zero-Bloat Fidelity:** Prioritize procedural generation, mathematical surfaces, and shader pipelines over multi-megabyte 3D asset downloads. Complex scenes should initialize reliably without network bottlenecks.
2. **Performance-Aware Rendering:** Maintain a target 60 FPS by measuring real draw calls, budgeting geometric instances, and implementing hardware capability probes to select appropriate rendering tiers at boot.
3. **Intentional Interaction Design:** Interaction must serve functional navigation and spatial comprehension. Scroll and pointer inputs are treated as physical controls rather than superficial triggers.
4. **Reliable Architecture:** Maintain clean separation between state management, physics simulation, and rendering loops. Codebases are reinforced with automated unit and end-to-end test suites.
5. **Accessible & Responsive Resilience:** Provide explicit fallbacks for devices with constrained GPU resources, touch-only interfaces, and visitors requesting `prefers-reduced-motion`.

---

## Current Experiments

* **Relativistic Ballistic Computation & Modal Acoustics:** Coupling 4th-order symplectic orbital integrators with Boolean collision logic gates and physical standing-wave string synthesis (`KEPLER-LOOM`).
* **Spatial Vision & Physics Bridges:** Real-time markerless hand tracking using MediaPipe Tasks Vision connected to 2D rigid-body constraint engines (`hand-tracking-physics` & `genesis`).
* **Native Desktop Graphics:** Cross-platform audio visualizer investigating volumetric 3D typography on Tauri 2 and Rust (`noctra`).

---

## Contact

* **GitHub:** [@islomf2010-dot](https://github.com/islomf2010-dot)
