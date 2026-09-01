---
layout: page
title: Diffusion Simulator
description: Interactive browser-based 3D particle simulator for Fick's Laws of Diffusion using random walks
img: assets/img/projects/diffusion.jpg
importance: 3
category: research
---

An interactive, browser-based 3D particle simulator that models atomic diffusion governed by **Fick's Second Law**. Built as a learning tool alongside the Kinetics course at RPI (Prof. Jian Shi).

### Features

- **Three boundary condition cases** implemented via 3D isotropic random walks:
  - Semi-infinite solid with constant surface concentration
  - Instantaneous planar source
  - Thin-film on a semi-infinite substrate

- **Real-time overlays** of simulated concentration profiles vs. exact analytical solutions (erfc, Gaussian)

- **Interactive controls** for:
  - Jump frequency (Γ) and jump length (λ)
  - Number of simulated atoms
  - Simulation speed

### Implementation

Pure frontend — no installation required. All rendering is done in WebGL via Three.js, with KaTeX for LaTeX math display. The simulation domain is 10× the visible window to approximate infinite boundary conditions.

The histogrammed particle concentrations agree well with the analytical solutions, visually demonstrating how diffusion profiles evolve from sharp initial conditions toward equilibrium.

**Tools:** JavaScript (ES modules), Three.js v0.163.0, KaTeX, WebGL

<div class="repositories d-flex flex-wrap flex-md-row flex-column justify-content-between align-items-center">
  <a href="https://github.com/cocokane/DiffusionModels" target="_blank" rel="noopener noreferrer" class="btn btn-sm z-depth-0" role="button">
    <i class="fa-brands fa-github"></i> GitHub Repository
  </a>
</div>
