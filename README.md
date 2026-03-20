# 🚀 Lunar Shuttle Sim

A **mobile-first, browser-based 3D space shuttle simulator** built with Three.js. Launch from Earth, achieve orbit, perform a trans-lunar injection burn, and land on the Moon — all with realistic(ish) physics and a beautiful procedural visual style.

> **Play it instantly** — just open `index.html` in any modern browser. No install, no build step, no dependencies to download.

---

## 🎮 How to Play

### Mission Phases

| Phase | What to do |
|---|---|
| **LAUNCH** | Fire engines and lift off. Keep your attitude pointing upward. |
| **ASCENT** | Continue burning — pitch gradually eastward to build orbital velocity. |
| **ORBIT** | You're in low Earth orbit. Prepare for the big burn. |
| **TRANS-LUNAR INJECTION** | Fire engines prograde to escape Earth's sphere of influence. |
| **COAST** | Engine off. Time warp auto-activates. Drift to the Moon. |
| **LUNAR APPROACH** | Re-orient retrograde and brake into lunar orbit. |
| **LANDING** | Slow descent — land gently on the golden pad. |
| **MISSION COMPLETE** | 🌕 Eagle has landed! |

### Controls

#### Keyboard
| Key | Action |
|---|---|
| `Space` | **Main thrust** (hold to fire engines) |
| `↑ ↓` | Pitch up / down |
| `← →` | Yaw left / right |
| `Q` / `E` | Roll left / right |
| `R` | Fine RCS thruster burst |

#### Mobile (Touch)
- **🔥 button** — Main thrust (hold)
- **D-pad arrows** — Pitch & yaw
- **↺ / ↻** — Roll
- **⚙ SAS** — Toggle auto-stabilization
- **📷** — Cycle camera views (Chase → Cockpit → Orbital)

### Tips
- **Manage your fuel** — you only have 100% and need enough for braking at the Moon
- **SAS on** during coast phase keeps you stable automatically
- **Orbital view** (📷 ×3) gives you a big-picture view of the Earth→Moon trajectory
- The **golden pad** on the lunar surface is your landing target — aim for it!
- Time warp kicks in automatically during the coast phase to skip the long transit

---

## ✨ Features

- **Procedural Earth** — Painted land masses, ocean, ice caps, cloud wisps, and a multi-layer atmospheric glow — no texture URLs, everything is canvas-generated
- **Procedural Moon** — Cratered lunar surface with rim highlights
- **8,000-star field** — Color-accurate stars with blue giants and orange dwarfs
- **Engine plume particle system** — Dynamic additive-blended particles that scale with throttle
- **SRB separation sparks** — Pyrotechnic burst when solid rocket boosters detach at 45 km
- **Full HUD telemetry** — Altitude, velocity, fuel, throttle bar, G-force, mission time, apoapsis/periapsis estimator, distance to Moon
- **Mission phase banners** — Dramatic on-screen callouts at each mission milestone
- **Pulsing landing pad** — Glowing golden target on the lunar surface
- **3 camera modes** — Chase, cockpit, and orbital
- **Auto time-warp** — 50× speed during coast phase so you don't wait 3 days

---

## 🛸 Physics Model

The game uses a simplified but feel-good physics model:

- **Two-body gravity** — Earth + Moon gravity wells both act on the shuttle simultaneously
- **Inverse-square law** — Gravity falls off correctly with distance `g ∝ 1/r²`
- **Atmospheric drag** — Exponential drag below 100 km altitude
- **Fuel consumption** — Proportional to throttle level
- **Orbital mechanics** — Apoapsis/periapsis computed from vis-viva energy equation

---

## 🛠 Tech Stack

| Technology | Role |
|---|---|
| [Three.js r160](https://threejs.org) | 3D rendering (loaded from CDN) |
| HTML5 Canvas | Procedural texture generation |
| Vanilla ES Modules | No build tools, no bundler |
| CSS3 | Mobile-first HUD + touch controls |
| Web Audio API | *(future: engine sound cues)* |

**Single file.** Everything — game engine, physics, textures, UI — lives in `index.html`. Drop it anywhere and it runs.

---

## 📱 Mobile Support

Tested on:
- iOS Safari (iPhone/iPad)
- Android Chrome
- Desktop Chrome/Firefox/Edge

Optimized for portrait **and** landscape. Touch controls auto-show on mobile; keyboard controls work on desktop.

---

## 🌌 Branches

| Branch | Contents |
|---|---|
| `main` | Stable release |
| `game-dev` | Active development — new features, physics tweaks, visual experiments |

---

## 📸 Screenshots

*(Open the game and take your own — it looks better in motion!)*

---

## 🪐 Roadmap

- [ ] Realistic Hohmann transfer orbit planner
- [ ] Sound effects (engine roar, SRB sep bang, landing thud)
- [ ] Save/load mission state
- [ ] Multiple missions (ISS rendezvous, Mars flyby)
- [ ] Multiplayer spectator mode
- [ ] WebXR VR support

---

## License

MIT — fly free 🚀
