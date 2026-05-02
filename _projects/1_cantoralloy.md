---
layout: page
title: CantorAlloy MLIP
description: Active-learning-based machine-learned interatomic potential for the CoCrFeMnNi high-entropy alloy
img: assets/img/projects/cantoralloy.jpg
importance: 1
category: research
related_publications: false
---

The CoCrFeMnNi Cantor alloy is a canonical high-entropy alloy (HEA) with exceptional mechanical properties. Developing accurate interatomic potentials for such multi-component systems is challenging due to the vast compositional and configurational space.

This project develops a **Moment-Tensor Potential (MTP)** for the equiatomic Cantor alloy using an **active learning workflow** that minimizes expensive DFT calculations while ensuring broad coverage of the relevant configuration space.

### Workflow

1. **Initial dataset**: 240 structures (200 train / 40 test) across 6 categories — defect-free at 300/600/900 K, dislocation, stacking fault, and vacancy configurations — all 108-atom SQS supercells
2. **DFT labeling**: VASP with PBE/PAW (500 eV cutoff, 15×15×15 k-mesh)
3. **Active learning**: Extrapolation-grade (Γ) thresholding to iteratively select high-value frames and retrain the MTP
4. **Validation**: Uniaxial tension, melting point, nanoindentation, equation of state (EOS), and NVT/NPT stability — all via LAMMPS

### Key Results

- Production model: `mtp8-rb10` (descriptor order 8, radial basis 10) — found stable where other configurations were not
- Validated on large simulation boxes (23,328 atoms, 18×18×18 FCC supercell) for tension and indentation
- Benchmarked against MEAM potential across all validation targets

**Tools:** LAMMPS, VASP, MLIP/MTP package, Python, NumPy, Matplotlib

<div class="repositories d-flex flex-wrap flex-md-row flex-column justify-content-between align-items-center">
  <a href="https://github.com/cocokane/CantorAlloyMLIP" target="_blank" rel="noopener noreferrer" class="btn btn-sm z-depth-0" role="button">
    <i class="fa-brands fa-github"></i> GitHub Repository
  </a>
</div>
