# laplacian-meshes

Please view this README rendered by GitHub at https://github.com/bmershon/laplacian-meshes

*All images, words, and code contained in this repository may be reproduced so long as the original author is given credit (Chris Tralie and Brooks Mershon).*

This assignment was completed as part of a course in 3D Digital Geometry (Math 290) taken at Duke University during Spring 2016. The course was taught by [Chris Tralie](http://www.ctralie.com/).

*LaplacianMesh.py* is the file student's are responsible for editing. The rendering engine and GUI is provided by Chris Tralie.

## Introduction

This assignment revolves around the [Laplace operator](https://en.wikipedia.org/wiki/Laplace_operator). Here, the operator is realized as a big ol' matrix which, when multiplied (on the left) by the matrix holding the mesh's vertices, gives us the curvature at each vertex. There are two flavors of the **Laplacian matrix** used here: umbrella weighting and cotangent weighting. The latter method of weighting attempts to correct for the uneven resolution of the mesh. 

The following features have been implemented in this assignment:

- Laplacian mesh editing (Umbrella and Cotangent weights
- Color interpolation
- Smoothing and sharpening
- Minimal Surfaces
- Flattening and surface parameterization
- Texturing using UV coordinates

## [Laplacian Mesh Editing](http://www.ctralie.com/Teaching/COMPSCI290/Assignments/Group3_LaplacianMesh/#lapmesh)

### Laplacian Matrix

The Laplacian operator is encoded as a sparse matrix **L**, with anchor rows appended to encode the weights of the anchor vertices (which may be manually moved, hence the name Laplacian *editing*).

### Cotangent Weights

Rather than using equal weights for each neighboring vertex in the Laplacian operator, we can attempt to correct for irregular mesh resolutions by using [Cotangent Weights](http://www.ctralie.com/Teaching/COMPSCI290/Assignments/Group3_LaplacianMesh/).

*Homer's arms are raised by placing an anchor at a vertex on a finger tip that has been displaced vertically. A small handful of anchors placed symmetrically about his body help to restrict edits to his arms. Cotangent weighting is used here.*

<img src="img/homer.png" width="49%">
<img src="img/homer-arms-raised.png" width="49%">

## [Color Interpolation](http://www.ctralie.com/Teaching/COMPSCI290/Assignments/Group3_LaplacianMesh/#function)

<img src="img/teapot-coloring.png" width="100%">

## [Laplacian Smoothing and Sharpening](http://www.ctralie.com/Teaching/COMPSCI290/Assignments/Group3_LaplacianMesh/#sharpening)

### Smoothing (Umbrella Weighting)

*We can smooth the teapot by iteratively pulling each vertex closer to the centroid of its neighbors.*

<img src="img/teapot-smooth-0.png" width="24.5%">
<img src="img/teapot-smooth-1.png" width="24.5%">
<img src="img/teapot-smooth-2.png" width="24.5%">
<img src="img/teapot-smooth-3.png" width="24.5%">

### Sharpening (Umbrella Weighting)

*We can sharpen the teapot by iteratively pulling each vertex farther away from the centroid of its neighbors.*

<img src="img/teapot-sharpen-0.png" width="49%">
<img src="img/teapot-sharpen-1.png" width="49%">

## [Minimal Surface](http://www.ctralie.com/Teaching/COMPSCI290/Assignments/Group3_LaplacianMesh/#membrane)

<img src="img/homer-minimal-before.png" width="49%">
<img src="img/homer-minimal-after.png" width="49%">

## [Mesh Parameterization (Flattening)](http://www.ctralie.com/Teaching/COMPSCI290/Assignments/Group3_LaplacianMesh/#flattening)

> I'm a little teapot
short and flat.
There is my handle;
Where is my spout?

<img src="img/teapot-parameterization.png" width="49%">
<img src="img/teapot-flattened.png" width="49%">

