---
layout: page
title:  "Summary of Course So Far"
permalink: "lectures/CumulativeSummary1"
---

* Talk today by candidate for next year, 4pm. Veranga Perera.

What have we accomplished so far?

### Vector calculus

* We reviewed vector calculus, in particular the divergence, gradient, and curl theorems. We have applied them in various scenarios including:

     (-) To $$\nabla \times \vec{E} = \frac{\rho}{\epsilon_0} $$ to get the integral form of Gauss's law. $$
\oint \vec{E} \cdot d\vec{a} = \frac{1}{\epsilon_0} Q_{\rm encl}
$$

     (-) To our equation for the potential of polarized material to get the notion of "bound" surface charge and "bound" volume charge.

$$
V = \frac{1}{4\pi\epsilon_0} \left[\int_\mathscr{V} \nabla^\prime\cdot\left(\frac{\vec{P}}{\mathscr{r}}\right) d\tau^\prime - \int_\mathscr{V} \frac{1}{\mathscr{r}}(\nabla^\prime \cdot\vec{P}) d\tau^\prime\right]
$$

$$
V = \frac{1}{4\pi\epsilon_0} \oint_\mathscr{S} \frac{\sigma_b}{\mathscr{r}}da^\prime  + \frac{1}{4\pi\epsilon_0} \int_\mathscr{V} \frac{\rho_b}{\mathscr{r}} d\tau^\prime
$$

### Minus signs
There is a collection of minus signs we've had to keep track of:

$$
V_b - V_a = - \int_a^b \vec{E} \cdot d\vec{l}
$$

where $$d\vec{l}$$ points along the path you're taking from $$a$$ to $$b$$.

At the surface of a conductor:

$$
\vec{E} =  \frac{\sigma}{\epsilon_0} \hat{n}  
$$

Notice the surface charge density $$\sigma$$ is positive if the E-field points 
out of the surface.  That
makes sense, right?  because E-field lines should start on positive charges.

and

$$
\sigma = -\epsilon_0 \frac{dV}{d\hat{n}} 
$$

where $$\vec{n}$$ is the vector perpendicular to the surface. Note that you have
to get that vector in the correct direction in order to get the correct
sign of the charge.  

$$
\nabla^2 V =  -\frac{\rho}{\epsilon_0}
$$

### Interesting factors of 1/2

Even though this is the formula for work to bring in a point charge, $$q$$, to a location where
the potential is $$V$$:

$$
W = q V
$$


This is the formula for the work required to assemble a charge distribution $$\rho$$

$$
W = \frac{1}{2}\int \rho V d\tau
$$

The same factor of $$1/2$$ is in the equation for energy stored in a E-field.

$$
W = \frac{\epsilon_0}{2} \int E^2 d\tau
$$

### Laplace's equation

$$
\nabla^2 V = 0
$$

This is true at every point in space where there is no charge.  An interesting consequence
of this formula is that if you can find a solution for $$V$$ for which Laplace's equation
is true, and which matches the boundary conditions of you're problem, you are guaranteed
that that is the solution to the potential everywhere.  So we investigated a number of
techniques that use this somewhat uncomfortable result:

* Separation of variables.  We assume the potential can be expressed as a product of two or three functions.  By clever use of arbitrary separation constants, we ensure that Laplace's
equation is true everywhere.  The general solutions usually end up as infinite series. We use the
boundary conditions of our problems to hone in on the specific solution to the problem at hand.

* Method of images. We actually solve a different problem than the one we're given, but as
long as it has the same value at the boundaries of the problem we're given, the set of
image charges gives us the correct potential. 

* Multipole expansion. We found that Coulomb's law (the potential version of it) can be
expressed as an infinite sum of successively smaller and smaller terms whose angular
form is that of the Legendre Polynomials (at least in the case of azimuthal symmetry). This
can be very useful for solving problems where the charge distribution has a finite extent (i.e. doesn't go to infinity) because only the first several terms will matter.

In particular, the 2nd term of the multipole expansion is the potential of a dipole.  Dipoles
turn out to be very important in nature, because atoms, despite their complicated electronic structure, often can be approximated as dipoles.
