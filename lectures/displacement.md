---
layout: page
title:  "Displacement"
permalink: "lectures/displacement"
---

[Results of the survey.](Survey.html)

One thing it would be useful to know:

Whatever we do on Monday the week a homework set is due, isn't something
you need for that problem set. We're always all done with the material
the Friday before it's due.  That will still be true.

Last time there were a couple of questions I didn't answer (I might 
save these for Monday, because we've got almost all of next week for
questions, and given recent discussions I think I want to make sure
you can do your homework this weekend.):

* How do you tell which term in a multipole is dominant?  

* How does the derivation for the potential of a dipole connect to the
multipole expansion?

Also, did you notice that the potential at the center of the cube in number 1
was V_0/6?  Why??

Doing #6 as an image charge was fun. Check out my notes.  Best part - you get
the same answer.

## Last time:
(on Monday in this case) we talked about polarization in a material and we
got:

$$
V = \frac{1}{4\pi\epsilon_0} \oint_\mathscr{S} \frac{\sigma_b}{\mathscr{r}}da^\prime  + \frac{1}{4\pi\epsilon_0} \int_\mathscr{V} \frac{\rho_b}{\mathscr{r}} d\tau^\prime
$$

where

$$
\sigma_b \equiv \vec{P}\cdot\hat{n}
$$

and

$$
\rho_b \equiv -\nabla\cdot\vec{P}
$$

## The Electric Displacement

In which we stop treating $$\epsilon_0$$ as something we can forget about, because
now we're not always in free space.

Out of this lecture we need to get:

$$
\nabla\cdot\vec{D} = \rho_f
$$

Gauss' law in the presence of a dielectric!

(Dielectric is anything that can be polarized.)

In Monday's lecture we found that the effect of polarization is to 
produce accumulations of  (bound) charge, $$\rho_b = −\nabla \cdot \vec{P}$$
within the dielectric and 
$$\sigma_b = \vec{P} \cdot \hat{n}$$
on the surface.

But there could be free charge embedded in the dielectric material.
So then we would need to combine our laws for the free and the bound charge.

$$
\rho = \rho_b + \rho_f
$$

Gauss' law:

$$
\epsilon_0\nabla \cdot \vec{E} = \rho = \rho_b + \rho_f =  −\nabla \cdot \vec{P} + \rho_f
$$

So now $$\vec{E}$$ is the total field, not just the portion generated
by polarization.

Combine the two divergence terms:

$$
\nabla \cdot (\epsilon_0 \vec{E} + \vec{P}) = \rho_f 
$$

We define $$\vec{D}$$ the electric displacement as:

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

Okay well we got our thing!  We're done!

We need a little more, and then we can do some problems:

Definitions of $$\vec{D}$$ (again)

$$
\vec{D} =  \epsilon_0 \cdot \vec{E} + \vec{P} = \epsilon_0\vec{E} + \epsilon_0\chi_e\vec{E} = \epsilon_0(1 + \chi_e)\vec{E} 
$$

where $$\chi_e$$ is called the electric susceptibility. It tells you
how susceptibility a particular material is to being polarized.  It's
defined to be unitless.

So then we can write:

$$
\vec{D} = \epsilon\vec{E}
$$

where

$$
\epsilon \equiv \epsilon_0(1 + \chi_e)
$$

$$\epsilon$$ is called the permittivity.  $$\epsilon_0$$ is the permittivity
of free space.

The dielectric constant of a material  is proportional to the permittivity, but
 without the $$\epsilon_0$$ in there:

$$
\epsilon_r \equiv 1 + \chi_e = \frac{\epsilon}{\epsilon_0}
$$

So now you've got all the equations you need.  Now we just need to
practice using them.

In class we did Example 4.5 (page 187) in groups.  It was good practice using
the new version of Gauss' law which says that $$D$$ really does JUST depend
on the free charge enclosed. (Notice it reduces to our more familiar version
of Gauss' law if $$\epsilon = $$\epsilon_0$$, (the permittivity equals the
permittivity of free space.)

$$
\oint \vec{D} \cdot d\vec{a} = Q_{f,{\rm enc}}
$$

and realizing that potential is still the integral of electric field (not electric displacement!)

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

$$\epsilon_r$$, the dielectric constant, is the one that really needs a different letter IMHO, besides
$$\epsilon$$, because it is **unitless** unlike the other two epsilons (permittivity and permittivity of free space, both of which are in units of $$C^2/Nm^2$$.)
$$\epsilon_r \equiv 1 + \chi_e = \epsilon/\epsilon_0$$.  Even though I hate
the letter they used, I find thinking about dielectric constants nice, because
if the dielectric constant is close to 1, then the material you're in
is acting pretty much like a vacuum as far as the polarization is concerned. Most gases (see Table 4.2 pg 187) have dielectric constants close
to 1.  Water has a dielectric constant of 80.  Water is very polarizable!!
What I try to remember is that the dielectric constant, times $$\epsilon_0$$
is the constant of proportionality between $$\vec{D}$$ and $$\vec{E}$$.

$$\alpha$$ is the atomic polarizability (as opposed to the capital $$P$$
bulk polarization). When I first introduced the concept of polarization we had a different constant
$$\alpha$$, the atomic polarizability, that tells you how polarizable a 
particular atom is, i.e.  $$ \vec{p} =\alpha \vec{E}$$
.  Notice that's a small $$\vec{p}$$ dipole moment, not the capital $$\vec{P}$$ polarization.
