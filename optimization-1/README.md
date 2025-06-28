# Optimization 1 – Baseline Layup Design, Structural Characteristic, and Angles Optimization

Baseline design with initial assumptions and basic manufacturing constraints. Optimized the ply orientations to get an idea of which ply angles to use.

## Objectives

- Define primary tank geometry, internal pressure loads, and boundary conditions relevant to mounting.
- Apply material properties for carbon fiber/epoxy composites used in AFP (Automated Fiber Placement) manufacturing.
- Validate structural response under cryogenic pressure and multi-axial loading conditions using linear static FEA.
- Identify areas of stress concentration, overdesign, and key failure modes.
- Include ply orientations from 0 to +/- 90 degrees in 5-degree increments with SMEAR set to ON to maintain stacking-sequence independence.
- Analyze outputs to determine which iroentations have potential for achieving as much strength as necessary with as little material as possible. 

## Files

- `angles_opti.hm` – HyperMesh model containing geometry, mesh, ply definitions, materials, and load cases.
- `angles_opti_newvals.fem` – OptiStruct input file for solver execution (linear static analysis). note: *_newvals was later named to compare these results with a prior model that was not quite right
- `angles_opti_newvals_s1.h3d` – HyperView-compatible results file for stress, displacement, and failure criteria visualization.
- `angles_opti_newvals.out` – Text output log showing run status, convergence behavior, and summary of constraint checks.
- `images/` – Screenshots of the mesh, boundary conditions, and post-processed results (e.g., stress plots, displacement contours).

## Key Learnings

- Ply layup strategy lacked manufacturing-friendly steering constraints, motivating changes in fiber angles and drop-off rates in future models.
- Potentially useful ply orientations were chosen for further study.

## Next Steps

This model informed the development of `optimization-2`, which introduced what shapes these ply orientations can tank to potentially make the tank more efficient. 
