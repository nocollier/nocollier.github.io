---
layout: post
title:  "Development of a Terrestrial Dynamical Core for E3SM at SIAM CSE"
date:   2019-02-25
categories: jekyll update
---

[slides](/assets/SIAM-CSE2019.pdf) 

Developing a predictive understanding of the terrestrial water cycle
at local to global scale is essential for accurate assessment of water
resources. Higher spatial resolution in the land component of the
Energy Exascale Earth System Model (E3SM) alone is insufficient to
meet the U.S. Department of Energy’s (DOE’s) 10-year
vision. Next-generation terrestrial models need to move beyond
one-dimensional systems by including scale appropriate
three-dimensional physics formulations. To this end, we are developing
a dynamical core which is tailored to solving thermal mass
balance. The method of choice should converge linearly in the velocity
in the presence of discontinuous coefficients and non-orthgonal
grids. We choose to implement a mixed finite element based on the
Brezzi-Douglas-Marini (BDM1) mixed finite element spaces analyzed by
Wheeler and Yotov [M. F. Wheeler and I. Yotov, A multipoint flux mixed
finite element method, SIAM J. Numer. Anal. 44:5 (2006)
2082-2106.]. In their method, the drawback of the resulting saddle
point problem is overcome by using a vertex-centered quadrature rule,
decoupling the velocity systems around the vertices of the mesh. This
allows for the velocity system to be eliminated locally, resulting in
a cell-centered stencil for pressure only. In this talk we describe
the challenges in efficiently implementing such a method as well as
present strategies for scaling the solution from the watershed to
continental scales.
