---
layout: page
title:  "Andrea's Crash Course in Chapter 4"
permalink: "/lectures/chapt4"
---

Predicted Release date: 2/17/20

The *atomic polarizability* is designated
by $$\alpha$$ and is the constant of proportionality between the applied
electric field $$\vec{E}$$ and the dipole moment $$\vec{p}$$.

$$
\vec{p} = \alpha \vec{E}
$$

The Torque on a dipole $$\vec{p}$$ in a uniform field $$\vec{E}$$:

$$
\vec{N} = \vec{p} \times \vec{E}
$$

The force on a dipole in a uniform field:
$$
\vec{F} = (\vec{p} \cdot \nabla) \vec{E}.
$$

And the energy of a dipole in a uniform electric field....

$$
U = - \vec{p} \cdot \vec{E}
$$

## Polarization
A material is said to be polarized if its atoms are roughly lined up. 
Polarization $$\vec{P}$$ is defined as

$$
\vec{P} = {\rm dipole~moment~per~unit~volume}
$$

You can calculate the field of a polarized object by finding the potential
of an effective surface charge and an effective volume charge.  Griffiths (and
lots of people) call them bound charges (as opposed to free charge, like in a
conductor.)

$$
\sigma_b \equiv \vec{P}\cdot\hat{n}
$$

where $$\vec{n}$$ is the normal to the surface.   

$$
\rho_b \equiv -\nabla \cdot \vec{P}
$$

so notice that $$\vec{P}$$ has to have a divergence in order for
there to be an effective (bound) charge density. 

And then we can rewrite...

$$
V = \frac{1}{4\pi\epsilon_0} \oint_\mathscr{S} \frac{\sigma_b}{\mathscr{r}}da^\prime  + \frac{1}{4\pi\epsilon_0} \int_\mathscr{V} \frac{\rho_b}{\mathscr{r}} d\tau^\prime
$$

