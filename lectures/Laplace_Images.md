---
layout: page
title:  "Laplace's Equation and the Method of Images"
permalink: "/lectures/laplace"
---

Question for the beginning of class:

We hold a charge $$q$$ a distance $$d$$ above an infinite grounded conducting plane.  What's the potential in the region above the plane?

Announcements

---------------------------------------

Announce office hours Sunday from ????

Announce lunch right after this with Melodie, colloquium, workshop.

Talk briefly about this problem set.

What you should expect from the environment in physics.
* mutual respect
* welcoming spaces
* honoring difference...all the differences you can think of
* integrity


---------------------------------------

We've got Coulomb's law

$$
\vec{E}(\vec{r}) = \frac{1}{4\pi\epsilon_0} \int\frac{\hat{R}}{R^2}\rho(\vec(r^\prime) d \tau^\prime
$$

where $$R = \vec{r} - \vec{r}^\prime$$

and the integral for the potential

$$
\vec{V}(\vec{r}) = \frac{1}{4\pi\epsilon_0} \int\frac{1}{R}\rho(\vec(r^\prime) d \tau^\prime
$$

but sometimes neither of those is possible and you need to "recast the problem in differential form" (as Griffiths says) using Poisson's equation

$$
\nabla^2 V = - \frac{1}{\epsilon_0}\rho
$$

If you're using Poisson's equation in a region where there's no charge
then Poisson's equation becomes Laplace's equation.

$$
\nabla^2 V = 0 
$$

By the way, there can be lots of interesting field in this region, just
not charge.

The solutions to Laplace's equation are called harmonic functions.  That's where we're going in this class...

In one dimension:

$$
\frac{d^2}{dx^2} = 0
$$

$$
V(x) = mx + b
$$

And then if you know that $$V(0)=5$$ and $$V(1)=4$$ then you can figure out
what $$m$$ and $$b$$ are.

So that's completely specified.

So that's really what we mean by solving Laplace's equation with boundary
conditions.  I don't know - I think it sounds really scarey until you point
out it's the thing you did in 7th grade where you had to figure out what
the equation of the line was.

Some interesting things to notice:
* The potential in the middle is the average of the potentials on either side.
* There can be no minimum or maximum in this region, except at the end points.

## Three dimensions

In three dimensions, what does it mean to specify the potential on the boundaries? It means to specify it on the surface.

**First uniqueness theorem: ** The solution to Laplace's equation in some volume $$\mathscr{V}$$ is uniquely determined if the $$V$$ (the potential) is specified on the boundary surface $$S$$. 

You can get it by analogy to the one dimensional case, right?

The things we noticed before are still true:

The potential at the center of a sphere is the average of the potential
around a sphere that surrounds it.

$$
V(\vec{r}) = \frac{1}{4\pi R^2} \oint_{\rm sphere} V da
$$

For this reason the potential is an "averaging" function.


There's an interesting consequence of the first uniqueness theorem.
If we can find a situation that produces the same potential on the
boundary in question, then we can find the potential every where in the volume.

**Classic Image Problem**
Your homework is dominated by image problems, by the way.


Brings us to the question I asked at the beginning of class:

We hold a charge $$q$$ a distance $$d$$ above an infinite grounded conducting plane.  What's the potential in the region above the plane?

This uses the second uniqueness theorem (but similar to the first):
**Second uniqueness theorem: ** In a volume $$\mathscr{V}$$ surrounded by
conductors and containing a specified charge density $$\rho$$, the electric
field is uniquely determined if the *total charge* on each conductor is given.

Griffiths picks the definition apart, and even proves it to you. Let's just see how to use it. The basic idea is the same as we've been talking about. We're only interested in
the field above the plane.  We know the charge, and we know the potential on the boundary (the plane) because it's a conductor and therefore an equipotential.

So instead of doing this problem we can do a different problem that has the same charge as 
in the area we're interested in, and the same potential on the boundary. 

What's the different problem?

Well, can you think of a relatively simple arrangement of charges that would have only this positive charge on this side of the plane, and V=0 at the boundary.  In other words, you can put whatever charges you want over here, as long as there's an equipotential.

Notice that this is made possible (brought to you by) Laplace's/Poisson's equation.  As long
as you know what $$\nabla^2$$ of the potential is, and you know it on the boundary, you can
know it everywhere, and it's uniquely determined by those criteria.

We need the other boundary too, but that's just the usual V goes to 0 at infinity.

We'll put the charges at $$z = +/- d$$ so the potential will look like this:

$$
V(x,y,z) = \frac{1}{4\pi\epsilon_0} \left[\frac{q}{\sqrt(x^2+y^2 + (z-d)^2)} - \frac{q}{\sqrt(x^2+y^2 + (z+d)^2)} \right]
$$

Remember thankfully in the potential you don't need vectors, and that thing in the denominator is just the difference between wherever you are and the point charge.

Does it satisfy our criteria?
* Goes to zero at infinity
* Is zero on the plan

So this is the potential everywhere that's bounded by our boundaries.

Morale: If it  satisfies Poisson’s equation in the region of interest, and assumes the correct value  at the boundaries, then it must be right.  

## What's the surface charge on the conductor?
We did that in class a couple days ago.  It's the derivative of the potential at the boundary.

$$
\sigma = \epsilon_0 \frac{\partial V}{\partial n}
$$

You can do that derivative (Griffiths shows it) and then you can integrate the surface
charge over the whole plane to get the total charge.  **What do you think the total charge is?**

## Your homework problems #5 and #6.

#5 is two parallel conducting plates with a charge in between them. Talk with your neighbor and think about what set of image charges you'd need to produce two V=0 planes.

#6 is a charge a distance $$a$$ away from the center of a neutral (not-grounded) conducting sphere of radius $$R$$. 
Griffiths does
the case where the sphere is grounded.  It's pretty interesting.  It turns out that
if you put an image charge a distance $$R^2/s$$ away from the center of the sphere 
with value $$-\frac{R}{a}q$$ then
you get potential of zero on the sphere.

**What's the total charge on the sphere?** (talk amongst yourselves)   
You can integrate Gauss' Law in the image
situation and know that
that $$\oint \vec{E}\cdot da = \frac{q^\prime}{\epsilon_0}$$.  That has to be true
in the real situation just outside the boundary.  So then there is $$q^\prime$$ on
the sphere.

So what do you do if the sphere isn't grounded, but rather neutral and isolated? 
Talk amongst yourselves.

A Gaussian surface just outside the sphere must now integrate to zero, so the total
charge has to be zero. 


Comment on Force and Energy. 
