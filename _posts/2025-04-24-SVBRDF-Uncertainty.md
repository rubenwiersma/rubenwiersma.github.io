---
title: "Uncertainty for SVBRDF Acquisition using Frequency Analysis"
layout: publication
categories:
  - Publications
tags:
  - Material Acquisition
  - SVBRDF
  - Uncertainty
  - Entropy
last_modified_at: 2025-04-24T10:21:00-01:00
venue: "SIGGRAPH 2025"
abstract: "This paper aims to quantify uncertainty for SVBRDF acquisition in multi-view captures. Under uncontrolled illumination and unstructured viewpoints, there is no guarantee that the observations contain enough information to reconstruct the appearance properties of a captured object. We study this ambiguity, or uncertainty, using entropy and accelerate the analysis by using the frequency domain, rather than the domain of incoming and outgoing viewing angles. The result is a method that computes a map of uncertainty over an entire object within a millisecond. We find that the frequency model allows us to recover SVBRDF parameters with competitive performance, that the accelerated entropy computation matches results with a physically-based path tracer, and that there is a positive correlation between error and uncertainty. We then show that the uncertainty map can be applied to improve SVBRDF acquisition using capture guidance, sharing information on the surface, and using a diffusion model to inpaint uncertain regions."
authors: "<b>R. Wiersma</b>, J. Philip, M. Hasan, K. Mullia, F. Luan, E. Eisemann, V. Deschaintre"
type: "Article"
doi: "10.1145/3721238.3730592"
# pdf: "https://graphics.tudelft.nl/~klaus/papers/Gravo_MG.pdf"
projectpage: "https://svbrdf-uncertainty.github.io"
code: "https://svbrdf-uncertainty.github.io"
img: "/assets/img/publications/svbrdf_uncertainty.jpg"
bib: "@inproceedings{wiersma2025svbrdfuncertainty,<br />
  author = {Wiersma, Ruben and Philip, Julien and Hašan, Miloš and Mullia, Krishna and Luan, Fujun and Eisemann, Elmar and Deschaintre, Valentin},<br />
  title = {Uncertainty for SVBRDF Acquisition using Frequency Analysis},<br />
  year = {2025},<br />
  isbn = {979-8-4007-1540-2/2025/08},<br />
  publisher = {Association for Computing Machinery},<br />
  address = {New York, NY, USA},<br />
  url = {https://doi.org/10.1145/3721238.3730592},<br />
  doi = {10.1145/3721238.3730592},<br />
  booktitle = {SIGGRAPH Conference Papers '25},<br />
  location = {Vancouver, BC, CA},<br />
  series = {SIGGRAPH Conference Papers '25}<br />
}"
---