# Hand Tracking Core

> An interactive 3D holographic experience controlled with hand gestures using **Three.js** and **MediaPipe**.

## ✨ Overview

**Hand Tracking Core** is a WebGL experiment that combines procedural 3D graphics with real-time hand tracking.

The experience features animated orbital rings, holographic wireframes, glowing particles, post-processing effects, and gesture-based interaction through your camera.

## 🖐️ Gesture Controls

| Gesture           | Action                                          |
| ----------------- | ----------------------------------------------- |
| 🤏 Single Pinch   | Rotate the holographic object                   |
| 🤲 Two-Hand Pinch | Zoom in and out                                 |
| ✊ Fist            | Dive into the core and trigger a transformation |

## 🚀 Features

- Real-time hand tracking with MediaPipe
- Interactive 3D scene built with Three.js
- Animated orbital rings and particles
- Procedural glow, flare, halo, and light effects
- Holographic wireframe structures
- Bloom post-processing
- Chromatic aberration on desktop
- Mobile performance optimizations
- GPU-accelerated hand tracking

## 🛠️ Tech Stack

- **Three.js**
- **MediaPipe Hand Landmarker**
- **WebGL**
- **HTML5 / CSS3 / JavaScript**

## 📦 Installation

Clone the repository:

```bash
git clone https://github.com/YOUR_USERNAME/hand-tracking-core.git
cd hand-tracking-core
```

Run it using a local server:

```bash
npx serve
```

Then open the local URL provided by the server.

> Camera permission is required for hand tracking.

## 📱 Browser Support

Works best on modern browsers with support for:

- WebGL
- ES Modules
- `getUserMedia`
- Hardware acceleration

Recommended: **Chrome, Edge, Firefox, or Safari**.

## 🔮 Future Improvements

- [x] On-screen gesture tutorial
- [ ] Loading screen
- [ ] Better camera permission feedback
- [ ] Mouse and touch controls
- [ ] Gesture calibration
- [ ] Visual themes
- [ ] Screenshot and recording support
- [ ] Modular project structure

## 📄 License

This project can be distributed under the **MIT License**.

---

\<p align="center">
Built with Three.js, MediaPipe, and WebGL.
\</p>
