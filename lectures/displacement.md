---
layout: page
title:  "Displacement"
permalink: "lectures/displacement"
---

Results of the survey:

One thing it would be useful to know:

Whatever we do on Monday the week a homework set is due, isn't something
you need for that problem set. We're always all done with the material
the Friday before it's due.  That will still be true.

Last time there were a couple of questions I didn't answer (I might 
save these for Monday, because we've got almost all of next week for
questions, and given recent discussions I think I want to make sure
you can do your homework this weekend.):

* How do you tell which term in a multipole is dominant?  

This is a great question.  There are a bunch of answers. 
* If the total charge is zero then the monopole term vanishes. 

* How does the derivation for the potential of a dipole connect to the
multipole expansion?

Also, did you notice that the potential at the center of the cube in number 1
was V_0/6?  Why??

Doing #6 as an image charge was fun. Check out my notes.  Best part - you get
the same answer.

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
