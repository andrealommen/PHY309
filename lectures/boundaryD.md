---
layout: page
title:  "Boundary Value Problems Using Displacement"
permalink: "lectures/boundaryD"
---

## Last time:

We defined $$\vec{D}$$ the electric displacement as:

$$
\vec{D} =  \epsilon_0 \vec{E} + \vec{P} 
$$

because it was very convenient.

So now Gauss's law is just

$$
\nabla \cdot \vec{D} = \rho_f 
$$

and the integral version is

$$
\oint \vec{D} \cdot d\vec{a} = Q_{f,{\rm enc}}
$$

Also

$$
\vec{D} = \epsilon\vec{E}
$$

($$\epsilon$$ is permittivity.)

We did a problem that made us realize that this still has to be true:

$$
V_b - V_a = - \int_a^b \vec{E} \cdot d\vec{l}
$$

i.e. potential is still the integral of the E field, not the displacement vector.  (Notice that among other
things it would have the
wrong units if it were the integral of the diplacement vector.)

**The dielectric constant, $$\epsilon_r$$**
A slightly different formulation of the proprotionality between E and D.

$$\vec{D} = \epsilon_0\epsilon_r\vec{E}$$.

## Boundary value problems in the presence of a dielectric
This also will have the side effect of reviewing a lot of stuff for the exam. (It reviews boundary
value problems and dielectrics and surface charge all at the same time.)

I want to give you a problem and you think about what you know, and what you need to know.

A long cylindrical dielectric rod of radius R is placed perpendicular to an externally applied, constant electric 
field, $$\vec{E}\hat{x}$$. Solve for the potential, both inside and outside the rod. 
Choose the potential at the center of the cylinder to be 0.  

This is really similar to #5 on the last homework set, a conducting rod in an externally applied, constant electric
field.

Before we do anything, talk with your group about what you think the solution is going to look like, just kind of
from waiving your hands. 

Ans: I'm hoping you figure out that
* the material will be polarized, and divergence-free, so the bound charge is all on the surface
* the potential inside the sphere will not be zero, but it will be lower than outside the sphere in general,
because the polarization serves to counter-act the field some.
* out at infinity, you should have $$\vec{E}$$ plus the field of a rod that has a whole bunch of charge
on one side, and the opposite charge on the other side, 
because that's what the charge on the cylinder looks like.  So just like before, at s=$$\infty$$ you should
get $$V = -Es\cos\phi$$. 
* I would expect that the smaller that $$R$$ is, the smaller the potential outside that we see in
addition to the $$V = -Es\cos\phi$$.

Questions I might ask you to tease this out:
* What does the bound charge distribution look like on the surface of the cylinder?  (You can just draw pictures
to figure this out.
* How will the potential inside the cylinder relate to the potential outside the cylinder?
* What should the potential very far away look like?


So to get a little more mathematical but not precise...
* Outside the sphere I expect $$V = -Es\cos\theta + A\cos \theta/r^2$$
where $$A$$ is something we have to figure out. (it turns out not to be the potential of a dipole, which
I still don't understand - so that $$r^2$$ isn't right.)
* Inside the sphere I expect $$V = (-{\rm small~~fraction}) Es\cos\theta$$.
* The $$A$$ and the small fraction must depend upon the dielectric constant of the material. If
the dielectric constant is 1 then I should get that the potential is $$-Es\cos\theta$$ everywhere, so
if the dielectric constant is 1 then $$A=0$$ and the small fraction should be 1.

Questions I might ask you to tease this out:
* If the dielectric constant is 1, what would the potential be everywhere?


Okay now let's get quantitative. I'll remind you that in the case of the the conducting rod in the external field,
you got a solution that looked like the $$n=1$$ term of the multipole expansion.  The answer was:

$$
V(s,\phi) = -E_0(s-R^2/s)\cos\phi
$$

That was the potential outside the cylinder.  Inside the sphere the potential was zero because it was a conducting
cylinder.  In this case, you actually need to calculate the potential both inside and outside the cylinder.

Here's the most general solution to Laplace's equation in cylindrical coordinates (with no $$z$$ dependence):

$$
V(s,\phi) = A_0\ln s + B_0 + \sum_{n=1}^\infty \left(A_ns^n + \frac{B_n}{s^n}\right)(C_n\cos n\phi + D_n\sin n\phi)
$$

You can see that the solution for outside the conducting cylinder looks just like the $$n=1$$ term of this. 

To solve the boundary value problem you need to know two more things that we haven't talked about:
* $$V$$ must be continuous everywhere. That's a general rule.
* $$D_{\perp, in} - D_{\perp, out} = \sigma_f$$  This is really similar to the rule we had for electric fields from
chapter 2 (equation 2.3.1) and the [Boundary Conditions lecture](/PHY309/lectures/conductors) namely
$$
\vec{E}_{above} - \vec{E}_{below} = \frac{\sigma}{\epsilon_0} \hat{n}
$$

Notice now the $$\epsilon_0$$ is gone because we're using $$\vec{D}$$. So again, the new equation reduces
to the more familiar one in the case of $$\epsilon = \epsilon_0$$.

Talk with your groups about how you're going to solve the boundary value problem for this scenario.

The salient points:
* You must allow the constants inside and outside to be different.   Across the boundary they can be different. You
haven't had to deal with this yet because you haven't had two sides to a boundary.  Remember what's true:  Laplace's
equation is true everywhere there's NOT charge.  So it has to work outside, and it has to work inside, but
at the border, you just know the potentials have to be the same.
* Where does the permittivity or dielectric constant come in?  In the last boundary conditions, the
one involving $$\vec{D}$$ at the border.  $$\vec{D}$$ is the negative derivative of the potential times
the permittivity.  So you can figure out $$\vec{D}$$ inside and outside and set them equal to each other (because
there's no free charge in this case.)  That will give you an equation that has $$\epsilon$$ on one
side the $$\epsilon_0$$ on the other side. The ratio will be the dielectric constant $$\epsilon_r$$.
* When you're considering matching the two potentials on either side of the boundary conditions, the two things
on either side will be infinite sums of cosines and sines of $$\phi$$. For that equation to be true for
all $$\phi$$ those coefficients must match each other - the thing multiplying $$\cos n\phi$$ on the left
must be equal to the the thing multiplying $$\cos n\phi$$ on the right.
* The argument that makes all the $$\sin n\phi$$ terms go to zero is pretty interesting. You could kind of
guess it right off the bat that it doesn't make any sense to have something depend upon $$\sin\phi$$ when
the only input function is $$\cos\phi$$.  But you have to be careful because you're starting to use
a boundary condition that depends upon derivatives.  However, that derivative is of both sides of the
equation, and it's a derivative in $$s$$ so really it'd be fine to set the coefficients of $$\sin\phi$$
equal to zero.   Another strategy is to notice that you can still satisfy all the boundary conditions without
them, therefore you must not need them.

What you would end up with if we finished is:

$$
V(r<R) = - \frac{2E_0s}{\epsilon_r +1} \cos\phi
$$

and

$$
V(r>R) = -E_0 \cos\phi\left[s - \frac{R^2}{s}\frac{\epsilon_r -1}{\epsilon_r + 1}\right]
$$

## Checking our solution afterward...
* Does it meet the criteria that if $$\epsilon_r =1$$ then we get $$-E_0s\cos\phi$$ back everywhere?
Indeed it does.
* We can tell that it satisfied Laplace's equation because it does actually look like our original
general solution for cylindrical coordinates, with only the $$n=1$$ and only the $$\cos\phi$$ term. 
* It's true that the smaller $$R$$ the smaller that additional term of the potential is.
* The potential inside the cylinder is indeed a somewhat reduced version of the potential
 from the external field alone, $$-Es\cos\phi$$, and it's more reduced the higher the dielectric
constant $$\epsilon_r$$ is.
* In fact, if we let $$\epsilon_r -> \infty$$ do we get back our solution for a conducting cylinder? Yes!!
Oh that's super cool.

## Parallel fields in dielectrics!

There's a big difference between dielectrics and conductors in that you **can** have fields
parallel to the surface in a dielectric.

$$
D_{\parallel, above} - D_{\parallel, below} = 
P_{\parallel, above} - P_{\parallel, below} = 
$$  

Makes sense right?  If you've got your little polarized atoms lined up + - + - + - along the surface, you
won't have zero field along the surface.


