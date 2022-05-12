---
layout: project
title: "DeltaConv: Anisotropic Operators for Geometric Deep Learning on Point Clouds"
sidebar_link: false
---
## SIGGRAPH 2022
# DeltaConv: Anisotropic Operators for Geometric Deep Learning on Point Clouds
[Ruben Wiersma](https://rubenwiersma.nl/)<sup>1</sup>, [Ahmad Nasikun](https://graphics.tudelft.nl/ahmad-nasikun/)<sup>1, 2</sup>, [Elmar Eisemann](http://graphics.tudelft.nl/~eisemann/)<sup>1</sup>, and [Klaus Hildebrandt](http://graphics.tudelft.nl/~klaus/)<sup>1</sup><br />
<sup>1</sup>Delft University of Technology, <sup>2</sup>Universitas Gadjah Mada

<img src="assets/img/publications/deltaconv/deltaconv.png" class="featured" width="80%">

<a id="github-link"
      class="icon" title="DeltaConv Github Repo" aria-label="Github Project"
      href="https://github.com/rubenwiersma/deltaconv" target="_blank">
    <i class="fa fa-2x fa-github"></i> Code</a>&nbsp;&nbsp;
<a id="pdf-link"
      class="icon" title="HSN PDF" aria-label="PDF link"
      href="https://arxiv.org/abs/2111.08799" target="_blank">
    <i class="fa fa-2x fa-file-pdf-o"></i> Paper PDF</a>&nbsp;&nbsp;
<a id="pdf-link"
      class="icon" title="Cite" aria-label="Cite"
      href="#cite">
    <i class="fa fa-2x fa-quote-right"></i> Cite</a>

## Abstract
Learning from 3D point-cloud data has rapidly gained momentum, motivated by the success of deep learning on images and the increased availability of 3D data. In this paper, we aim to construct anisotropic convolution layers that work directly on the surface derived from a point cloud. This is challenging because of the lack of a global coordinate system for tangential directions on surfaces. We introduce DeltaConv, a convolution layer that combines geometric operators from vector calculus to enable the construction of anisotropic filters on point clouds. Because these operators are defined on scalar- and vector-fields, we separate the network into a scalar- and a vector-stream, which are connected by the operators. The vector stream enables the network to explicitly represent, evaluate, and process directional information. Our convolutions are robust and simple to implement and match or improve on state-of-the-art approaches on several benchmarks, while also speeding up training and inference.

## Summary
Our focus is on constructing intrinsic convolutions which are anisotropic or direction-dependent. This is difficult because of the fundamental challenge that surfaces typically lack a global intrinsic coordinate system.

As an illustration of the problem, consider a CNN on images. Because an image has a globally consistent up-direction, the network can build anisotropic filters that activate the same way across the image.
For example, one filter can test for vertical edges and the other for horizontal edges. No matter where the edges are in the image, the filter response is consistent. In subsequent layers, the output of these filters can be combined, e.g., to find a corner.

<img src="assets/img/publications/deltaconv/intro.png" class="featured" width="50%">

Because we do not have a global coordinate system on surfaces, one cannot build and use anisotropic filters in the same way as on images. This limits current intrinsic convolutions on point clouds.

### DeltaConv

DeltaConv is described in terms of geometric operators instead of kernels. A well known operator that has been used widely in geometric deep learning is the Laplacian. While the Laplacian is a natural fit for intrinsic learning on surfaces, it is isotropic.

A classical way of creating anisotropic operators is to write the Laplacian as the divergence of the gradient and apply a linear or non-linear operation on the intermediate vector field. DeltaConv builds on this idea by constructing learnable anisotropic operators from elemental geometric operators: the gradient, co-gradient, divergence, curl, Laplacian, and Hodge-Laplacian. Because the operators output scalars and vectors, DeltaConv splits into a scalar- and vector stream.

<img src="assets/img/publications/deltaconv/deltaconv_schematic.png" class="featured" width="70%">

DeltaConv is easy to implement: you only need two sparse matrices that represent gradient and divergence. Everything else can be implemented with matrix multiplication and standard MLPs.

## Results

The result is an intrinsic and anisotropic convolution layer that can be used in typical neural architectures for learning on point clouds that produces state-of-the-art results: 93.8% accuracy on ModelNet40, 86.9mIoU on ShapeNet, and 84.7% accuracy on the most difficult variant of ScanObjectNN. Meanwhile, it's faster than previous edge-based convolutions, because it represents directional features at points instead of edges.

A simple example on images illustrates the difference with other convolution layers for point clouds. We apply a classical anisotropic diffusion operator (Perona-Malik) on images and overfit a ResNet with different convolution layers on the result. DeltaConv is able to approximate the anisotropic diffusion process and is also able to mimic different diffusion times, where other convolutions struggle.

<img src="assets/img/publications/deltaconv/astronaut-20.png" class="featured" width="80%">

## Learn more

Find out more about DeltaConv in our paper, or come see our (virtual) presentation at SIGGRAPH 2022.

<a id="github-link"
      class="icon" title="DeltaConv Github Repo" aria-label="Github Project"
      href="https://github.com/rubenwiersma/deltaconv" target="_blank">
    <i class="fa fa-2x fa-github"></i> Code</a>&nbsp;&nbsp;
<a id="pdf-link"
      class="icon" title="HSN PDF" aria-label="PDF link"
      href="https://arxiv.org/abs/2111.08799" target="_blank">
    <i class="fa fa-2x fa-file-pdf-o"></i> Paper PDF</a>&nbsp;&nbsp;
<a id="pdf-link"
      class="icon" title="Cite" aria-label="Cite"
      href="#cite">
    <i class="fa fa-2x fa-quote-right"></i> Cite</a>

## Contact
r.t.wiersma [at] tudelft.nl, k.a.hildebrandt [at] tudelft.nl

<a href="http://graphics.tudelft.nl" target="_blank">Computer Graphics and Visualization group TU Delft</a>

## Cite
```
@Article{Wiersma2022DeltaConv,
  author    = {Ruben Wiersma, Ahmad Nasikun, Elmar Eisemann, Klaus Hildebrandt},
  journal   = {Transactions on Graphics},
  title     = {DeltaConv: Anisotropic Operators for Geometric Deep Learning on Point Clouds},
  year      = {2022},
  month     = jul,
  number    = {4},
  volume    = {41},
  doi       = {10.1145/3528223.3530166},
  publisher = {ACM},
}
```