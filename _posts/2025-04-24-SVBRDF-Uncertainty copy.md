---
title: "TetWeave: Isosurface Extraction using On-The-Fly Delaunay Tetrahedral Grids for Gradient-Based Mesh Optimization"
layout: publication
categories:
  - Publications
tags:
  - Object reconstruction
  - Meshing
  - Geometry
  - Optimization
  - Machine Learning
last_modified_at: 2025-05-05T10:21:00-01:00
venue: "SIGGRAPH 2025 (ToG)"
abstract: "We introduce TetWeave, a novel isosurface representation for gradient-based mesh optimization that jointly optimizes the placement of a tetrahedral grid used for Marching Tetrahedra and a novel directional signed distance at each point. TetWeave constructs tetrahedral grids on-the-fly via Delaunay triangulation, enabling increased flexibility compared to predefined grids. The extracted meshes are guaranteed to be watertight, two-manifold and intersection-free. The flexibility of TetWeave enables a resampling strategy that places new points where reconstruction error is high and allows to encourage mesh fairness without compromising on reconstruction error. This leads to high-quality, adaptive meshes that require minimal memory usage and few parameters to optimize. Consequently, TetWeave exhibits near-linear memory scaling relative to the vertex count of the output mesh — a substantial improvement over predefined grids. We demonstrate the applicability of TetWeave to a broad range of challenging tasks in computer graphics and vision, such as multi-view 3D reconstruction, mesh compression and geometric texture generation."
authors: "A. Binninger, <b>R. Wiersma</b>, Philipp Herholz, Olga Sorkine-Hornung"
type: "Article"
doi: "10.1145/3730851"
pdf: "https://alexandrebinninger.com/TetWeave/paper/TetWeave.pdf"
projectpage: "https://alexandrebinninger.com/TetWeave/"
code: "https://github.com/AlexandreBinninger/TetWeave"
img: "https://alexandrebinninger.com/TetWeave/media/teaser.jpg"
bib: "@article{Binninger:TetWeave:2025,<br />
  title={TetWeave: Isosurface Extraction using On-The-Fly Delaunay Tetrahedral Grids for Gradient-Based Mesh Optimization},<br />
  author={Binninger, Alexandre and Wiersma, Ruben and Herholz, Philipp and Sorkine-Hornung, Olga},<br />
  note={SIGGRAPH 2025 issue},<br />
  year={2025},<br />
  issue_date = {July 2025},<br />
  publisher = {Association for Computing Machinery},<br />
  address = {New York, NY, USA},<br />
  doi={10.1145/3730851},<br />
  journal = {ACM Trans. Graph.},<br />
  month = {7}<br />
}"
---
