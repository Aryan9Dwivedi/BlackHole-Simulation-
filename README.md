# 🌌 black_hole — Black Hole Simulation (Gravitational Lensing + GPU Geodesics)

A visual black hole simulation project focused on **gravitational lensing**, **ray-tracing**, and **spacetime curvature**.

> 🎥 Project walkthrough video (explains the code + visuals):  
> https://www.youtube.com/watch?v=8-B6ryuBkCM

---

## ✨ Highlights

- **2D Gravitational Lensing** (easy entry point)
- **3D Black Hole Simulation** accelerated using a **GPU compute shader**
- **Geodesic integration** performed on GPU for speed (heavy math offloaded from CPU)
- Modular structure with core logic living inside `src/`

---

## 🧠 What this project simulates

### ✅ Implemented
- **Gravitational lensing (2D + 3D)**
- **3D geodesic computation using GPU (compute shader)**
- **Black hole visuals + lensing behavior based on ray tracing principles**

### 🗺️ Planned / Extended Ideas
1. **Ray-tracing**: enhance the gravity simulation to simulate realistic lensing rays  
2. **Accretion disk**: simulate an accretion disk using ray tracing + halos  
3. **Spacetime curvature**: visualize the “trapdoor in spacetime” using a curvature grid  
4. *(Optional)*: try to run everything in real-time 😄

---

## 📁 Project Structure

```text
black_hole/
├─ src/
│  ├─ 2D_lensing.cpp        # 2D lensing (CPU)
│  ├─ black_hole.cpp        # 3D simulation driver
│  └─ ...                   # helpers / rendering / utilities (project dependent)
├─ shaders/
│  └─ geodesic.comp         # GPU compute shader (geodesic integration)
├─ CMakeLists.txt
└─ README.md
