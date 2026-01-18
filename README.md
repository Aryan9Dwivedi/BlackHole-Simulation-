# 🌌 black_hole — Black Hole Simulation (Gravitational Lensing + GPU Geodesics)

A C++ black hole simulation project focused on **gravitational lensing**, **ray tracing**, and **GPU-accelerated geodesic integration**.  
The goal is to visually demonstrate how light behaves near extreme gravity and build an interactive, physics-inspired black hole renderer.

This repository contains both:
- **2D lensing (CPU)** — simple, easy to understand, great for learning/debugging
- **3D lensing (GPU)** — accelerated using a compute shader for performance

---

## ✨ Key Features

### ✅ Implemented
- **2D gravitational lensing** (CPU-based)  
- **3D black hole simulation** with **GPU compute shader acceleration**
- **Geodesic computation** on the GPU for faster ray bending / trajectory calculations
- **Uniform Buffer Object (UBO) pipeline** for passing simulation parameters from CPU → GPU
- Clean project structure built around **CMake** and dependency management via **Vcpkg**

### 🚧 Planned / Roadmap
This project was built as a progression-style simulation where complexity increases step-by-step:

1. **Ray Tracing**
   - Add ray tracing to the gravity simulation to simulate more realistic lensing
2. **Accretion Disk**
   - Simulate a glowing accretion disk using ray-traced rays + halo effects
3. **Spacetime Curvature Visualization**
   - Visually demonstrate the “trapdoor in spacetime” using a grid distortion method
4. **Optional: Real-time Mode**
   - Optimize to run smoothly in real-time (if possible)

---

## 🎯 What This Project Demonstrates

Black holes distort spacetime so strongly that light rays passing near them bend dramatically.  
This creates visible effects such as:

- **gravitational lensing**
- **Einstein ring–like distortion**
- bending and warping of background geometry
- compact bright rings near the event horizon (future enhancement)

This simulation aims to represent these effects visually using a combination of:
- CPU reference implementation (2D)
- GPU compute shader implementation (3D)

---

## 📽️ Output Expectations (What You Should See)

Depending on the version you run:

### 2D Mode
- A simplified 2D representation of lensing
- Light-like trajectories bending around a black hole mass

### 3D Mode
- A more complex scene where rays travel in 3D space
- Curvature effects computed faster using the GPU
- Better performance (especially at higher resolutions / more rays)

---

## 📁 Repository Structure

> Everything important lives inside `src/` and `shaders/`.

```text
black_hole/
├─ src/
│  ├─ 2D_lensing.cpp         # 2D gravitational lensing (CPU)
│  ├─ black_hole.cpp         # 3D simulation entry point
│  └─ ...                    # helpers/utilities (varies by setup)
├─ shaders/
│  └─ geodesic.comp          # GPU compute shader for geodesic integration
├─ CMakeLists.txt
└─ README.md
