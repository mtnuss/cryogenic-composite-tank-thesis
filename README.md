# Cryogenic Composite Tank Optimization

This repository contains structural optimization models developed during my M.S. thesis at the University of Washington, titled, "Optimizing AFP Manufactured Composite-Based Cryogenic Tanks for Space-Based Missions”. The project focused on the design and performance optimization of a carbon fiber composite cryogenic pressure vessel for spacecraft propulsion systems.

The work includes mesh generation, material and boundary condition setup, solver input decks, and results visualizations. Each optimization iteration represents a distinct design phase, incorporating lessons learned and progressively improving manufacturability, performance, and structural efficiency.

## Repository Structure

```plaintext
cryogenic-composite-tank-thesis/
├── optimization-1/
│   ├── model.hm
│   ├── run.fem
│   ├── results.h3d
│   ├── output.out
│   ├── images/
│   │   ├── mesh.png
│   │   └── stress_plot.png
│   └── README.md
├── optimization-2/
│   ├── model.hm
│   ├── run.fem
│   ├── results.h3d
│   ├── output.out
│   ├── images/
│   │   ├── mesh.png
│   │   └── displacement_plot.png
│   └── README.md
├── optimization-3/
│   ├── design-a/
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
│   ├── design-b/
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
│   ├── design-c/
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
│   └── README.md   # Summary of optimization-3 iteration across all designs and methods
├── benchmark/
│   ├── stresses.png
|   ├── README.md
├── model/
│   ├── tank.png
|   ├── README.md  # Summary of the model and assumptions made
├── README.md       # Main project overview
```

## How to Use

- **Software Requirements:**  
  These models are built for use with Altair HyperWorks 2022.1 or later.
  - Open `.hm` files in **HyperMesh**
  - View `.h3d` files in **HyperView**
  - Run `.fem` files in **OptiStruct** if solver access is available

- **Images Folder:**  
  Each optimization folder includes a set of `.png` images that provide a quick look at the mesh quality, boundary conditions, and result plots (stresses and failure indices).

## Project Background

This project explored three iterations of composite tank design with increasing structural and manufacturing performance:

- **Optimization 1:** Baseline design with initial assumptions and basic manufacturing constraints. Optimized the ply orientations to get an idea of which ply angles to use. 
- **Optimization 2:** With a set of potential ply directions to use, this optimization takes a closer look at those orientations to see which shapes they should take on the tank.
- **Optimization 3:** Final optimization step with known orientations and their shapes to see how many layers are needed to create final designs after interpretations of results.
- **Benchmark Industry Quasi-Isotropic Approach:** Model under the same loading conditions made with the same Toray T700GC material. Made up of full-shape 0s, +/-45s, and 90s to be just strong enough to not fail while maintaining composite balance and symmetry. Made to assess the value of layup optimization. 

Resultant FEA models after the third optimization step resulted in a **~30% mass reduction** and **~40% projected manufacturing time savings** compared to an industry-standard quasi-isotropic benchmark, earning top thesis recognition for innovation in aerospace composite structures.

## License

You may reuse or reference this work for educational and non-commercial purposes. If you use these models or visuals in your own work, please credit the original author.

---

Feel free to reach out via [LinkedIn](https://www.linkedin.com/in/matthewtnuss/) or [email](mailto:matthewtnuss@outlook.com) 
