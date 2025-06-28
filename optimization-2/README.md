# Optimization 2 – Optimizing the Shapes

This model represents the second design iteration in the structural and manufacturing optimization of a composite cryogenic tank. Built on lessons learned from the baseline configuration in Optimization 1, this phase introduced the chosen ply orientations and was used to inform what shapes these orientations can take on the tank for potential mass and manufacturing time savings. 

## Objectives

- Optimize the chosen ply orientations from optimization 1 with SMEAR set to ON to maintain independence of stacking sequence.
- Determine which shapes different orientations can take on the tank.

## Files

- `widths_opti_patched.hm` – Updated HyperMesh model with only the relevant ply orientations
- `widths_opti_patched_newvals.fem` – OptiStruct solver deck incorporating updated element sets and control cards
- `widths_opti_patched_newvals_des.h3d` – Post-processed results file for analysis in HyperView
- `widths_opti_patched_newvals.out` – Output log file with constraint checks and convergence data
- `images/` – Mesh quality and shapes snapshots and updated stress/strain plots

## Key Improvements

- Learned where certain orientations work the best on the tank

## Lessons Learned

These insights informed the final designs in `optimization-3`, which introduced three different optimized design ideas compared to a non-optimized, traditionally used approach in carbon fiber cryotanks. 
