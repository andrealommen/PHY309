---
layout: page
title:  "Andrea's Crash Course in Chapter 5"
permalink: "/lectures/chapt5"
---

### The Lorentz Force Law

For moving point charge...

$$
F_{mag} = Q(\vec{v} \times \vec{B})
$$

For current....

$$
F_{mag} = I \int d\vec{l} \times \vec{B}
$$

### The Biot-Savart Law:

$$
\vec{B}(\vec{r}) = \frac{\mu_0}{4\pi} \int \frac{\vec{I} \times \hat{\mathscr{r}}}{\mathscr{r}^2}dl^\prime 
$$

$$\mu_0$$ is the permeability of free space. $$\mathscr{r}$$ is the vector
from the source point to the point $$\vec{r}$$.

For a steady current...

$$
\vec{B}(\vec{r}) = \frac{\mu_0}{4\pi}I \int \frac{\vec{dl^\prime} \times \hat{\mathscr{r}}}{\mathscr{r}^2}
$$

For a straight long current...

$$
B = \frac{\mu_0 I}{2\pi d}
$$

You can find the direction of $$\vec{B}$$ using the right hand rule. 

### Ampere's Law (the curl of $$\vec{B}$$)

Differential form:

$$
\nabla \times \vec{B} = \mu_0 \vec{J}
$$

Integral form:

$$
\oint \vec{B}\cdot d\vec{l} = \mu_0 I_{enc}
$$

or for a current density $$\vec{J}$$:

$$
\oint \vec{B}\cdot d\vec{l} =  \int\vec{J}\cdot d\vec{a}
$$

### The Divergence of B 

Unlike E the divergence of B is zero:

$$
\nabla \cdot \vec{B} = 0
$$

### The Vector Potential:

$$
\vec{B} = \nabla \times \vec{A} 
$$

(We can assume $$\vec{A}$$ exists because the divergence of B is zero. The
curl of a divergence is zero.)

### Poisson's equation for $$\vec{A}$$:  

$$
\nabla^2 \vec{A} = -\mu_0 \vec{J} 
$$

Note this is really three equations, one for each component of $$\vec{A}$$.

### Boundary conditions:
For the magnetic field and its associated vector potential:
* A is continuous
* B perp is continuous!! 
* B parallel is discontinuous

$$
B_{above}^\perp = B_{below}^\perp
$$

$$
B_{above}^\| - B_{below}^\| = \mu_0 K 
$$

where $$\vec{K}$$ is the surface current.  (Current per area, so surface charge
density times velocity).

### Magnetic Dipole:

$$
\vec{m} = I\vec{a}
$$

where $$\vec{a}$$ is the vector area of the loop.  Figure out which
was it points using the right-hand rule.

$$
A_{dip}(\vec{r}) = \frac{\mu_0}{4\pi} \frac{\vec{m}\times\hat{r}}{r^2}
$$
