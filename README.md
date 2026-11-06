# Eight-piece skull for 3D printing

Original non-voxelized triangle meshes of **Hoolock-hoolock-f-AMNH-83425-cranium-einscan**, the source model used by the Assembly_Sim eight-piece skull task.

## Download and print

Download this repository using **Code → Download ZIP**. Send the ZIP or the eight files in [`stl/`](stl/) to your printing provider.

- Print **one copy of each** `piece_0.stl` through `piece_7.stl`.
- Import STL coordinates as **millimeters**. The assembled bounding box is approximately **103.96 × 95.36 × 150.00 mm (X × Y × Z)**.
- 150 mm is a convenient export size, **not a verified anatomical size**. To change it, apply the same scale factor to every piece (for example, 200/150 for a 200 mm maximum dimension). Do not independently normalize each piece.
- Pieces retain their assembled relative coordinates. For separate printing, arrange each piece on the build plate and choose its orientation and supports in the slicer.
- These are the original fracture surfaces. No assembly clearance, connectors, wall thickening, smoothing, or mesh repairs have been added. The provider should inspect thin features, support requirements, and mating fit before printing. Watertightness alone does not guarantee printability or easy physical assembly.

## Files

- [`original/view_gt.glb`](original/view_gt.glb): unchanged original assembled scene with eight separate meshes, preserving the source coordinates and colors.
- [`stl/`](stl/): eight binary STL files with original triangle geometry, uniformly scaled; STL does not preserve colors.
- [`mesh-report.json`](mesh-report.json): per-piece dimensions, triangle counts, mesh checks, and source SHA-256.
- [`SHA256SUMS`](SHA256SUMS): integrity hashes for the model files and report.

All eight exported STL files were reloaded and verified as watertight with consistent face winding. Triangle counts and bounds were checked against the transformed source meshes. No voxelization or simplification was performed.

| File | Dimensions X × Y × Z (mm) | Triangles |
| --- | --- | --- |
| [piece_0.stl](stl/piece_0.stl) | 31.69 × 44.21 × 47.44 | 92,580 |
| [piece_1.stl](stl/piece_1.stl) | 42.41 × 45.96 × 29.46 | 103,214 |
| [piece_2.stl](stl/piece_2.stl) | 32.27 × 32.27 × 30.71 | 57,754 |
| [piece_3.stl](stl/piece_3.stl) | 37.89 × 28.16 × 31.78 | 64,738 |
| [piece_4.stl](stl/piece_4.stl) | 53.59 × 68.88 × 55.85 | 267,006 |
| [piece_5.stl](stl/piece_5.stl) | 25.04 × 30.06 × 29.28 | 44,168 |
| [piece_6.stl](stl/piece_6.stl) | 52.87 × 39.87 × 39.00 | 119,576 |
| [piece_7.stl](stl/piece_7.stl) | 96.88 × 93.82 × 150.00 | 789,418 |

## Provenance

The source was preserved from the CRAG result case `morphosource_v2/Hoolock-hoolock-f-AMNH-83425-cranium-einscan/view_gt.glb`. The Assembly_Sim eight-piece voxelized layout identifies this case as its source. This repository contains the non-voxelized source geometry and direct STL exports.

The original specimen's physical units and redistribution license were not supplied with the preserved files. No new license or ownership claim is asserted here.
