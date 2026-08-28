<div align="center">

# 🪐 Hand Tracking Core

**A real-time, gesture-controlled 3D orb rendered in WebGL. No mouse, no keyboard, just your hands.**

Built with **Three.js** and **MediaPipe Hand Landmarker**, running entirely in the browser.

[![Three.js](https://img.shields.io/badge/Three.js-000000?style=flat&logo=three.js&logoColor=white)](https://threejs.org/)
[![MediaPipe](https://img.shields.io/badge/MediaPipe-Hand%20Landmarker-4285F4?style=flat&logo=google&logoColor=white)](https://developers.google.com/mediapipe)
[![WebGL](https://img.shields.io/badge/WebGL2-990000?style=flat&logo=webgl&logoColor=white)](https://www.khronos.org/webgl/)
[![License: All Rights Reserved](https://img.shields.io/badge/License-All%20Rights%20Reserved-red.svg)](#-license)

[![Hand Tracking Core Demo](./assets/preview.gif)]


[![Live Demo](https://img.shields.io/badge/🟢_Live-esvius.github.io-black?style=for-the-badge)](https://esvius.github.io/hand-tracking-orb/)

</div>

---

## 📕 Overview

**Hand Tracking Core** turns your webcam into a controller. A glowing, multi-layered orb — orbiting electron rings, nested icosahedron wireframes, a procedural point-cloud network shell, and a bloom-lit core — responds live to your hand gestures, tracked entirely client-side with zero backend and zero installs.

No motion sensors, no external hardware. Just a browser and a camera.

## 🎮 Controls

| Gesture | Action |
|---|---|
| 🤏 Pinch with **one hand** | Rotate the orb |
| 🤏🤏 Pinch with **both hands** | Zoom in / out |
| ✊ **Make a fist** | Dive into the core and reveal its inner structure |

All gesture states use enter/exit thresholds (hysteresis) to stay stable and jitter-free, so tracking noise doesn't cause flickering between states.

## 🧠 How It Works

1. **MediaPipe Hand Landmarker** streams 21 3D landmarks per hand from the webcam feed, GPU-accelerated and running fully in-browser.
2. Landmark geometry is analyzed each frame to classify **pinch** and **fist** states independently per hand.
3. Recognized gestures drive target rotation, zoom, and camera-dive values, which are then smoothly interpolated (lerped) into the **Three.js** scene each render tick — so motion always feels fluid, never snapped.
4. The scene itself is composed of independently animated layers (orbit rings, wireframe shells, particle network, dust) rendered through an `EffectComposer` pipeline for bloom and color-fringing.

## 🛠️ Tech Stack

- **[Three.js](https://threejs.org/)** — scene graph, WebGL rendering, post-processing (`EffectComposer`, `UnrealBloomPass`, custom chromatic aberration shader)
- **[MediaPipe Hand Landmarker](https://developers.google.com/mediapipe)** — real-time, GPU-accelerated hand landmark detection
- **Vanilla JS / ES Modules** — no framework, no bundler, no build step

## 🚀 Getting Started

```bash
git clone https://github.com/esvius/hand-tracking-orb.git
cd hand-tracking-orb
```

Camera access requires a secure context, so serve the folder rather than opening the file directly:

```bash
npx serve .
# or
python -m http.server 3000
```

Then open `http://localhost:3000`, grant camera permission, and start moving your hands.

## 📋 Requirements

- A browser with WebGL2 + WebRTC support (Chrome or Edge recommended)
- A webcam
- A reasonably modern GPU for smooth 60fps bloom rendering

## 🗺️ Roadmap

- [ ] Additional gestures (swipe, spread) for extra interactions
- [ ] Configurable color themes for the orb
- [ ] Touch/mouse fallback controls for devices without a camera

## 🤝 Contributing

This is a personal, closed-source project external contributions and pull requests are not currently accepted.

## 📄 License

**All Rights Reserved.** This repository is source-available for viewing only — no permission is granted to use, copy, modify, or distribute this code without explicit written consent from the author. See [LICENSE](LICENSE) for details.

---

<div align="center">

Made with 🤍 by [**esvius**](https://github.com/esvius)

</div>
