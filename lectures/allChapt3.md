---
layout: page
title:  "Andrea's Crash Course in Chapter 3"
permalink: "/lectures/chapt3"
---

There are multiple ways to compute the potential, and each is suited to a different set of circumstances:

### Compute directly
I would consider this a last resort unless you've got a point charge.

$$
V(r) = \frac{1}{4\pi\epsilon_0}\int \frac{1}{R}\rho(\vec{r}^\prime d\tau^\prime.
$$

### Integrating Poisson's (or Laplace's) equation's twice to get the potential
This works great in one dimension when you have boundary conditions, 
because you can integrate it twice to get rid of the derivatives.  You'll
have two constants of integration, which you can figure out by using the 
boundary conditions. 

$$
\nabla^2 V = \frac{d^2V}{dx^2} = -\frac{\rho}{\epsilon_0}
$$

### Method of Images
Create a set of charges outside the region of interest that produce 
a potential in the region of interest that matches the boundary conditions.
It's useful for point charges near conducting planes and conducting spheres. 
Note that if what you really want is the field rather than the potential, you
can compute it directly from the image charges (rather than computing $$V$$
and taking the gradient).

### Separation of variables
You assume your solution is the product of two functions, each of which
is a function of only one variable, and then you use boundary conditions
to find the potential.
This works great if you have cartesian boundaries, in which case you 
get solutions that are products of exponentials and/or sinusoids.

In spherical coordinates this works, too, as long as you have azimuthal
symmetry (i.e. nothing in the problem involves $$\phi$$) You end up with Legendre Polynomials in the function of $$\theta$$. 

### Multipole Expansion
If you're interested in the potential outside of the charge distribution,
the multipole expansion is useful because it'll tell you what the 
dominant term in the potential is...the next leading term...etc.
The general solution to Coulomb's law (at the top of this page) actually
naturally gets you Legendre Polynomials.  Note that you don't need boundary
conditions to use a multipole expansion, because the multipole expansion
is actually a formula for the potential given a particular charge distribution.
