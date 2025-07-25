# Optimization 3 – Optimizing the Numbers of Layers

This directory contains the final and most advanced stage of structural optimization for a composite cryogenic pressure vessel, as presented in my M.S. thesis:  
**“Optimizing AFP Manufactured Composite-Based Cryogenic Tanks for Space-Based Missions.”**  
This phase implements manufacturability-aware modeling, advanced failure criteria, and multiple geometric variants to assess structural and mass performance trade-offs under real-world constraints given what was learned in the previous two optimization steps.

## Overview

Following the baseline and intermediate models in Optimization 1 and 2, this phase introduces:

- **Three geometric design variants**: `0-band`, `quasi-isotropic`, and `traditional`, each with different layup shapes and ply orientations to compare with each other and an un-optimized baseline tank.
- **Three distinct optimization criteria** applied to each geometry:
  - `maxstrain`: Linear strain limit-based failure prediction
  - `stresscriteria`: Traditional stress-based failure criteria (e.g., maximum von Mises or directional)
  - `tsaiwu`: Progressive failure theory using Tsai-Wu composite failure envelope

Each folder contains full HyperMesh model files, solver decks, post-processed results, and a dedicated `README.md` with insights into that specific simulation and outcome.

## Objectives

- Integrate all Design for Automated Fiber Placement (DfAFP) constraints directly into the ply architecture, including:
  - Minimum steering radius
  - Continuous manufacturing techniques
  - Ply symmetry and balance
- Evaluate and compare failure criteria across distinct geometries under identical loading conditions
- Optimize each configuration for structural performance, manufacturability, and mass efficiency
- Determine which configuration and failure method yielded the most robust design per mission constraints

## Directory Structure

```plaintext
├── optimization-3/
│   ├── 0-band/
│   │   ├── maxstrain/
│   │   |   ├── model.hm
│   │   │   ├── run.fem
│   │   │   ├── output.out
│   │   │   └── README.md
│   │   ├── stress/
│   │   │   ├── model.hm
│   │   │   ├── run.fem
│   │   │   ├── output.out
│   │   │   └── README.md
│   │   ├── tsaiwu/
│   │   │   ├── model.hm
│   │   │   ├── run.fem
│   │   │   ├── output.out
│   │   │   └── README.md
|   |   ├── images
|   |   |   ├── stresses.png
│   │   │   └── failureindices.png
│   |   └── README.md
│   ├── quasi-isotropic/
│   │   ├── maxstrain/
│   │   |   ├── model.hm
│   │   │   ├── run.fem
│   │   │   ├── output.out
│   │   │   └── README.md
│   │   ├── stress/
│   │   │   ├── model.hm
│   │   │   ├── run.fem
│   │   │   ├── output.out
│   │   │   └── README.md
│   │   ├── tsaiwu/
│   │   │   ├── model.hm
│   │   │   ├── run.fem
│   │   │   ├── output.out
│   │   │   └── README.md
|   |   ├── images
|   |   |   ├── stresses.png
│   │   │   └── failureindices.png
│   |   └── README.md
│   ├── traditional/
│   │   ├── maxstrain/
│   │   |   ├── model.hm
│   │   │   ├── run.fem
│   │   │   ├── output.out
│   │   │   └── README.md
│   │   ├── stress/
│   │   │   ├── model.hm
│   │   │   ├── run.fem
│   │   │   ├── output.out
│   │   │   └── README.md
│   │   ├── tsaiwu/
│   │   │   ├── model.hm
│   │   │   ├── run.fem
│   │   │   ├── output.out
│   │   │   └── README.md
|   |   ├── images
|   |   |   ├── stresses.png
│   │   │   └── failureindices.png
│   |   └── README.md
│   └── README.md
```

Summary

This final optimization phase resulted in understanding just how much of each ply orientation in their chosen shapes was needed for each case. This resulted in multiple final designs which were analyzed using FEM and compared to determine final masses and approximate manufacturing times using CNC machining software VCP/VCS by Vericut. h3d files are not included, as github does not support such large files. But these are obtained when you run the simulations if you are truly curious.
