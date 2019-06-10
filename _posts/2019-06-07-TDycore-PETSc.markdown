---
layout: post
title:  "Development of a Terrestrial Dynamical Core for E3SM at PETSc Users Meeting"
date:   2019-06-07
categories: jekyll update
---

[slides](/assets/PETScUsers2019.pdf) 

Developing a predictive understanding of the terrestrial water cycle at local to global scale is essential for accurate assessment of water resources. Higher spatial resolution in the land component of the Energy Exascale Earth System Model  alone is insufficient to meet the U.S. Department of Energy's 10-year vision. Next-generation terrestrial models need to move beyond one-dimensional systems by including scale appropriate three-dimensional physics formulations. To this end, we are developing a terrestrial dynamical core which is tailored to solving thermal mass balance equation at global scales.

The method of choice should converge quadratically in the velocity in the presence of discontinuous coefficients and non-orthgonal grids as well as lend itself to scalable solution approaches. While mixed finite element methods are a natural choice, they lead to a saddle point system which presents computational challenges.

In this talk, we compare computational advantages in using a mixed finite element based on the Brezzi-Douglas-Marini (BDM1) mixed finite element spaces analyzed by Wheeler and Yotov (2006) [M. F. Wheeler and I. Yotov, A multipoint flux mixed finite element method, SIAM J. Numer. Anal. 44:5 (2006) 2082-2106.]. In their method, the drawback of the resulting saddle point problem is overcome by using a vertex quadrature rule, decoupling the velocity systems around the vertices of the mesh. This allows for the velocity to be eliminated locally, resulting in a symmetric positive definite system in terms of pressure only.