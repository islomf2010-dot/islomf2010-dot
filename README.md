<div align="center">
  <img src="https://raw.githubusercontent.com/islomf2010-dot/islomf2010-dot/main/assets/banner.svg" alt="Engineering Studio Banner" width="100%" />
</div>

<br/>

## Overview

> **Creative Technologist building interactive worlds, cinematic interfaces, and real-time graphics for the web.**

I engineer in-browser visual systems where graphics, audio, and physics operate as a unified runtime process. Rather than relying on heavy pre-packaged 3D assets or generic web templates, my work emphasizes mathematical procedural generation, custom GLSL shader pipelines, deterministic clock synchronization, and low-latency interaction design.

Every project in this archive is designed to be lightweight, responsive, and resilient across diverse hardware profiles.

---

## Selected Work

### 01. AFTERLIGHT — The World Between Frames
**An interactive cinematic WebGL film in six seamless scenes, synthesized entirely at runtime within a single WebGL context.**

```
[ ARCHITECTURE: 6 SCENES ] ──► [ SINGLE WEBGL CONTEXT ] ──► [ PROCEDURAL SOUND ENGINE ] ──► [ ZERO ASSET DOWNLOADS ]
```

* **Live Demonstration:** [islomf2010-dot.github.io/afterlight](https://islomf2010-dot.github.io/afterlight/)
* **Source Repository:** [github.com/islomf2010-dot/afterlight](https://github.com/islomf2010-dot/afterlight)
* **Core Stack:** `Three.js` · `React Three Fiber` · `@react-three/postprocessing` · `GLSL Shaders` · `Web Audio API` · `GSAP / Lenis` · `Playwright`
* **Key Engineering Feature:** 
  * **Runtime Hardware Probing & Zero-Asset Synthesis:** Inspects GPU capabilities, thread concurrency, and viewport metrics at startup to configure a safe rendering tier. All geometry, water surfaces, atmospheric noise, particles, and acoustic drones are generated procedurally on the GPU and Web Audio thread—requiring zero external 3D models or audio samples.

---

### 02. AFTERFORM — Generative Architecture Studio
**An interactive spatial laboratory algorithmically generating brutalist and minimalist structural studies from pseudo-random seeds.**

* **Live Demonstration:** [islomf2010-dot.github.io/afterform](https://islomf2010-dot.github.io/afterform/)
* **Source Repository:** [github.com/islomf2010-dot/afterform](https://github.com/islomf2010-dot/afterform)
* **Core Stack:** `Three.js` · `React Three Fiber` · `Zustand` · `TypeScript` · `Vite` · `Vitest`
* **Key Engineering Feature:**
  * **Constrained Spatial Grammar & Instanced Rendering:** Generates architectural massing snapped to strict modular units (`CELL = 2m`, `STOREY = 1.15m`) with strict volume budgets for enclosures, bridges, and gateways. Renders hundreds of geometric modules in batched `InstancedMesh` draw calls with dynamic real-time material parameters (concrete roughness, glass transmission, procedural stone).

---

### 03. Ferrari F40 — The Reveal
**A scroll-scrubbed cinematic study exploring the 1987 Ferrari F40 through a deterministic, frame-accurate camera trajectory.**

* **Live Demonstration:** [ferrari-f400.vercel.app](https://ferrari-f400.vercel.app)
* **Source Repository:** [github.com/islomf2010-dot/ferrari-f400](https://github.com/islomf2010-dot/ferrari-f400)
* **Core Stack:** `GSAP ScrollTrigger` · `Custom H.264 Video Pipeline` · `React` · `TypeScript` · `Vite`
* **Key Engineering Feature:**
  * **Sub-Pixel Clock Synchronization:** Replaces traditional continuous playback with scroll position as the sole master clock. Synchronizes camera motion, studio light rigs, and contextual narrative overlays with zero WebGL overhead, backed by closed-GOP keyframe streams and strict `prefers-reduced-motion` fallbacks.

---

### 04. School 13 — Roguelite Survival Engine
**A 2D top-down survival game engine featuring spatial entity partitioning, procedural industrial audio synthesis, and reactive AI narrative integration.**

* **Live Demonstration:** [islomf2010-dot.github.io/school-13](https://islomf2010-dot.github.io/school-13/)
* **Source Repository:** [github.com/islomf2010-dot/school-13](https://github.com/islomf2010-dot/school-13)
* **Core Stack:** `HTML5 Canvas 2D` · `Web Audio API` · `Google Gemini API` · `TypeScript` · `React 19`
* **Key Engineering Feature:**
  * **Procedural Breakbeat Synthesizer & State Loop:** Drives combat with a 136 BPM procedural step-sequenced industrial audio engine that dynamically shifts frequency filters and tempo during ultimate ability states (e.g., time dilation), rendered at a fixed 60 FPS update rate with automated sprite caching and telegraph hazard zones.

---

## Technical Focus

```
┌── REAL-TIME GRAPHICS & SHADERS ────────────────────────────────────────────────────────┐
│  • Three.js / React Three Fiber (R3F)           • Custom GLSL Shaders (Vertex & Fragment)│
│  • InstancedMesh & Draw Call Optimization       • Postprocessing & Atmospheric Pipelines │
│  • Procedural Mesh Generation & UV Mapping      • GPU Particle & Simulation Fields       │
└────────────────────────────────────────────────────────────────────────────────────────┘

┌── MOTION & INTERACTION ENGINEERING ────────────────────────────────────────────────────┐
│  • GSAP (ScrollTrigger & Timeline Scrubbing)   • Lenis Smooth Scrolling Orchestration   │
│  • Frame-Accurate Scrubbing & Video Sync       • Pointer, Drag, and Spring Physics      │
│  • Computer Vision Bridges (MediaPipe)         • Strict Reduced-Motion Accessibility    │
└────────────────────────────────────────────────────────────────────────────────────────┘

┌── AUDIO & COMPUTATIONAL SYSTEMS ───────────────────────────────────────────────────────┐
│  • Web Audio API (Multi-Oscillator Synthesis)  • Procedural Ambient Drones & Breakbeats │
│  • Spatial Audio & Frequency Modulation        • Symplectic Orbit & Collision Integrators│
│  • Deterministic PRNG Seed Architectures       • State Machines & Spatial Partitioning  │
└────────────────────────────────────────────────────────────────────────────────────────┘

┌── CORE ENGINEERING & WORKFLOW ─────────────────────────────────────────────────────────┐
│  • React 19 / TypeScript                       • Vite Build Tooling & Rollup Chunking   │
│  • Vitest (Unit & Deterministic Math Testing)  • Playwright (End-to-End Browser Tests)  │
│  • Tauri 2.0 (Rust Desktop Integration)        • Linux / Arch Operating Systems         │
└────────────────────────────────────────────────────────────────────────────────────────┘
```

---

## Engineering Philosophy

1. **Zero-Bloat Fidelity:** Prioritize procedural generation, mathematical algorithms, and shaders over multi-megabyte 3D asset downloads. High-end experiences should load instantaneously on standard connections.
2. **Deterministic Performance:** Maintain steady 60 FPS by profiling draw calls, managing instancing budgets, and incorporating hardware capability probes during startup to select appropriate rendering tiers.
3. **Intentional Interaction:** Motion should never serve as empty decoration. Scroll and gestures should function as physical mechanisms that grant visitors agency over the scene.
4. **Resilient Degradation:** Build graceful fallbacks for devices with constrained GPU resources, touch-only interfaces, and visitors requesting reduced motion.

---

## Active Research & Experiments

* **Relativistic Ballistic Computation & Modal Acoustics:** Investigating orbital mechanics coupled to Boolean collision logic gates and standing-wave physical string synthesis ([KEPLER-LOOM](https://github.com/islomf2010-dot)).
* **Local Vision & Spatial Physics:** Real-time markerless hand tracking through WebGL2 compute passes and rigid body constraint bridges.
* **Native Desktop Graphics:** Cross-platform music visualization exploring volumetric 3D typography on Tauri 2 and Rust ([NOCTRA](https://github.com/islomf2010-dot)).

---

## Contact & Code Repositories

* **GitHub:** [github.com/islomf2010-dot](https://github.com/islomf2010-dot)
* **Status:** Open to technical collaborations, creative engineering commissions, and graphics experiments.
