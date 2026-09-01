---
layout: page
title: LJ Force-Field Parameterization
description: Active-learning framework (GA + GPR) for efficient Lennard-Jones parameter optimization — published in JCTC
img: assets/img/projects/ljparamopt.jpg
importance: 2
category: research
related_publications: true
---

Classical force fields are fundamental to molecular dynamics (MD) simulations, but parameterizing Lennard-Jones (LJ) parameters is expensive — brute-force grid search over parameter space requires thousands of costly MD runs.

This framework combines **Genetic Algorithms (GA)** with **Gaussian Process Regression (GPR)** to intelligently navigate LJ parameter space, converging to optimal values with far fewer MD evaluations.

### How It Works

1. **Initialization**: Generate 200 initial LJ parameter sets within ±5% of OPLS reference values
2. **MD evaluation**: Run GROMACS simulations for each parameter set; compute density and pair radial distribution functions (RDFs) vs. AIMD reference
3. **Active learning loop**:
   - Train GPR on evaluated parameters
   - GA uses GPR as a surrogate to predict better candidates
   - Run MD on top candidates; update training data
   - Repeat until convergence

### Results

- Applied to sulfone-based molecules (DMSO₂, DPSO₂)
- Optimized LJ parameters **outperform published OPLS parameters** in reproducing density and OO/SS pair RDFs
- Accepted in the *Journal of Chemical Theory and Computation* (DOI: [10.1021/acs.jctc.5c00061](https://doi.org/10.1021/acs.jctc.5c00061))

**Tools:** Python, GROMACS 2022.4, scikit-learn (GPR), DEAP (genetic algorithms)

<div class="repositories d-flex flex-wrap flex-md-row flex-column justify-content-between align-items-center">
  <a href="https://github.com/cocokane/LJ_paramopt_framework" target="_blank" rel="noopener noreferrer" class="btn btn-sm z-depth-0" role="button">
    <i class="fa-brands fa-github"></i> GitHub Repository
  </a>
</div>
