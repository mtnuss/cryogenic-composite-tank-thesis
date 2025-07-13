# Optimization 2 – Optimizing the Shapes

This model represents the second design iteration in the structural and manufacturing optimization of a composite cryogenic tank. Built on lessons learned from the baseline configuration in Optimization 1, this phase introduced the chosen ply orientations and was used to inform what shapes these orientations can take on the tank for potential mass and manufacturing time savings. 

## Objectives

- Optimize the chosen ply orientations from optimization 1 with SMEAR set to ON to maintain independence of stacking sequence.
- Determine which shapes different orientations can take on the tank.

## Files

- `widths_opti_patched.hm` – Updated HyperMesh model with only the relevant ply orientations
- `widths_opti_patched_newvals.fem` – OptiStruct solver deck incorporating updated element sets and control cards
- - `widths_opti_patched_newvals.out` – Output log file with constraint checks and convergence data
- `images/` – Mesh quality and shapes snapshots and updated stress/strain plots. Images of the proposed shapes to evaluate are included, with teh actual designs for each approach being shown in `optimization-3`

## Key Improvements

- Learned where certain orientations work the best on the tank

## Lessons Learned

These insights informed the final designs in `optimization-3`, which introduced three different optimized design ideas compared to a non-optimized, traditionally used approach in carbon fiber cryotanks. 

## Design Outcomes

- 0-Degree Band Approach: At the interface between the cylinder walls and the hemispherical domes, a tapered band of zero-degree plies (relative to the tank longitudinal axis) is applied of unknwon thickness to reinforce this interface. Proposed idea was to see if failure happens at the interface and if this can be successfully reinfroced to push design limits due to interface weakness. Layup consists of 0-degree band, +/-30s for the entire tank shape, and 90s for the cylindrical walls. 
- Quasi-Isotropic Approach: A fairly safe and traditional quasi-isotropic (sort-of isotropy) approach where 0s, +/-45s, and 90s are used for the entire tank shape. This looks at using computational laminate optimization to improve upon safe, more traditional approaches to making pressure vessels out of carbon-fiber reinforced composite (CFRC).
- Traditional Approach: A more daring approach to the safe, quasi-isotropic approach, where an attempt is made to save material where certain orientations may be too much for different areas of the tank. The walls are the weakest part of any pressure vessel of this shape, so they are reinforced with 90-degree plies for just the wall shape, while +/-30s take up the entire shape of the tank.
