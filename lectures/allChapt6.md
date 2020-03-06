---
layout: page
title:  "Andrea's Crash Course in Chapter 6"
permalink: "/lectures/chapt6"
---


Torque on a dipole:

$$
\vec{N} = \vec{m}\times\vec{B}
$$

Force on a dipole:

$$
\vec{F} = \nabla(\vec{m}\cdot \vec{B})
$$

Compare to it's electrical ``twin":
$$
\vec{F} = \nabla(\vec{p}\cdot \vec{E})
$$

### The "Gilbert" model:

You can do a lot of magnetostatic problems by using electrostatic results
and replacing:
* $$\vec{p}$$ with $$\vec{m}$$
* $$1/\epsilon_0$$ with $$\mu_0$$
* $$E$$ with $$B$$

Once you get really close-up to the dipole (where it looks like a ring
of current instead of a perfect magnetic dipole) then this breaks down.
Griffiths' advice is to use the Gilbert model to get intuition, but
don't rely on it for quantitative results.

### Paramagnetism

The presence of the magnetic field can make the electron speed
up in its orbit.  The magnetic moment changes by:

$$
\Delta \vec{m} = -\frac{1}{2} e(\Delta v)R\hat{z} = -\frac{e^2R^2}{4m_e}\vec{B}
$$

Notice the change in $$\vec{m}$$ is opposite the direction of $$\vec{B}$$.

### Magnetization

$$\vec{M}$$ is the magnetic dipole moment per unit volume (just like $$\vec{P}$$
is the electric dipole moment per unit volume.)

The vector potential due to some magnetized matter is:

$$
\vec{A}(\vec{r}) = \frac{\mu_0}{4\pi} \int \frac{\vec{M}(\vec{r}^\prime) \times \hat{\mathscr{r}}}
{\mathscr{r}^2} d\tau^\prime
$$

In a manner very similar to what we did for electric dipoles, we can
define a bound volume current and a bound surface current.

$$
\vec{J}_b = \nabla \times \vec{M}
$$

$$
\vec{K}_b = \vec{M} \times \hat{n}
$$

where $$\hat{n}$$ is the normal unit vector (normal to the surface.)

With those definitions:

$$
\vec{A}(\vec{r}) 
= \frac{\mu_0}{4\pi} \int_V \frac{\vec{J}_b(\vec{r}^\prime)}{\mathscr{r}} d\tau^\prime
+ \frac{\mu_0}{4\pi} \int_S \frac{\vec{K}_b(\vec{r}^\prime)}{\mathscr{r}} da^\prime
$$

### The Auxiliary Field

$$
\vec{H} = \frac{1}{\mu_0} \vec{B} - \vec{M}
$$

Ampere's law for H:

$$
\nabla \times \vec{H} = \vec{J}_f
$$

or in integral form:

$$
\oint \vec{H}\cdot d\vec{l} = I_{free}
$$

#### Boundary Conditions

The boundary conditions on $$\vec{H}$$ are:

$$
H_{above}^\perp - H_{below}^\perp = M_{above}^\perp - M_{below}^\perp  
$$

$$
\vec{H}_{above}^\| - \vec{H}_{below}^\| = \vec{K}_f \times \hat{n}
$$

