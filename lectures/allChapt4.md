---
layout: page
title:  "Andrea's Crash Course in Chapter 4"
permalink: "/lectures/chapt4"
---

The *atomic polarizability* is designated
by $$\alpha$$ and refers to the ability of a single atom to polarize: 

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

You can calculate the field everywhere by our regular laws for $$\vec{E}$$ if
you know the bound surface charge and bound volume charge.    The electric field
is the sum of the field from all the bound and free charges.

$$
\rho = \rho_b + \rho_f
$$

Using that equation for $$\rho$$ the potential is the usual integral over all the charge.

## The Electric Displacement
We invented the displacement vector to try to make our lives easier, so we didn't
have to know the bound charge in order to calculate the field. 

Reminder, a dielectric is anything that can be polarized.

$$
\vec{D} =  \epsilon_0 \vec{E} + \vec{P} 
$$

So now Gauss's law is just

$$
\nabla \cdot \vec{D} = \rho_f 
$$

and the integral version is

$$
\oint \vec{D} \cdot d\vec{a} = Q_{f,{\rm enc}}
$$

So often in problems involving dielectrics, you calculate $$\vec{D}$$, a non-physical
vector in weird units (see my [rant](final_words_displacement)), because it's easiest.  And then from $$\vec{D}$$ you
calculate $$\vec{E}$$ using the equation below.

$$
\vec{D} = \epsilon\vec{E}
$$

The potential is still the integral of electric field (not electric displacement!)

$$
V_b - V_a = - \int_a^b \vec{E} \cdot d\vec{l}
$$

## The $$\epsilon$$ confusion. 

I have to say that the abundance of versions of $$\epsilon$$ is really confusing.  Let me try to straighten them out.

$$\epsilon$$ is the permittivity of any medium. It is the constant of proportionality between $$\vec{E}$$ and $$\vec{D}$$. 
It's defined as:
$$
\epsilon \equiv \epsilon_0(1 + \chi_e)
$$

$$\chi_e$$ is the electric susceptibility.  It's the constant (defined to be unitless) that tells you how **susceptible** a material is to being
polarized.  So if $$\chi_e=0$$ the material is exactly as susceptible as 
free space, i.e. not at all. 
$$
\vec{P} = \epsilon_0\chi_e\vec{E}
$$
.  It's convenient, but a little confusing, that $$\epsilon_0$$ is included
in the definition of $$\chi_e$$, because whenever you're talking about 
electric susceptibility you are specifically NOT talking about free space.
$$\epsilon_0$$ is included in $$
\vec{P} = \epsilon_0\chi_e\vec{E}
$$ so that the units of $$\chi_e$$ are dimensionless.

$$\epsilon_r$$, the dielectric constant, 
is **unitless** unlike the other two epsilons (permittivity and permittivity of free space, both of which are in units of $$C^2/Nm^2$$.)
$$\epsilon_r \equiv 1 + \chi_e = \epsilon/\epsilon_0$$.  

I find thinking about dielectric constants nice, because
if the dielectric constant is close to 1, then the material you're in
is acting pretty much like a vacuum as far as the polarization is concerned. 
