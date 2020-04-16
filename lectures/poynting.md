---
layout: page
title:  "Poynting vector, Energy, Momentum in Electromagnestism"
permalink: "/lectures/poynting"
---

### Where we are
For the last two weeks we've been putting together everything we have
gathered about Maxwell's equations in vacuum and in media to understand
the propagation of electromagnetic waves in vacuum and in media. 

### Where we're going
What happens next is:
* We need to talk about energy and momentum contained in E&M fields in general,and then
specifically in E&M waves.
* We need to understand dispersion - how different wavelengths will travel at different velocities in a medium
----That's all this week, while you're studying for and taking the exam------
* Then we need to go back to potentials, particularly vector potentials, so that we can understand deferred potentials, so that we can understand how radiation occurs. (We've talked about electromagnetic waves, but you'll notice we haven't talked about how we generate them at all. We
ve just assumed they're there and tried to understand their properties. In this very last section of the course, we need to generate them.

### Poynting's Theorem

The big joke about Poynting's Theorem is that Poynting is a guy's name, but that his name seems to suggest something about where the energy points, i.e. travels, in an electromagnetic wave.

It's actually the relationship between Work and Energy in a field.  Poynting's theorem
is the work-energy theorem for E&M.  

Let's start by asking a question we can answer.

How much work is done by the electromagnetic
forces acting on a charge in some interval dt?

We use the Lorentz force law and the definition of work.

$$
\vec{F}\cdot d\vec{l} = q(\vec{E} + \vec{v}\times\vec{B})\cdot \vec{v} dt = q\vec{E}\cdot{v}dt
$$

If we want this in charge and current densities instead of particular particles we 
let $$q \rightarrow \rho d\tau$$ and we let $$\rho \vec{v} \rightarrow \vec{J}^2$$.

Then we get

$$
\frac{dW}{dt} = \int_v(\vec{E}\cdot\vec{J})d\tau.
$$

So that was the answer to the question "How much work is done by the electromagnetic
forces acting on a bunch of charges in some interval dt?"

So just a reminder, that's the work done by the electromagnetic forces acting on the
charges in an interval dt.  So $$\vec{E}\cdot\vec{J}$$ is the work done per unit time
per unit volume. Or the power delivered per unit volume.

Using Maxwell's equations (and only Maxwell's equations, plus the divergence theorem) (Page 358)
we get the work-energy theorem of electrodynamics, Poynting's theorem. (I skipped 
a half page of math here on page 358).

$$
\frac{dW}{dt} = -\frac{d}{dt}\int_V\frac{1}{2}\left((\epsilon_0E^2 + \frac{1}{\mu_0}B^2\right)d\tau - \frac{1}{\mu_0}\oint_S(\vec{E}\times\vec{B})\cdot d\vec{a}
$$

**The first term: energy contained in the fields** 

In Chapter 2 we found the work necessary to assemble a static charge distribution

$$
W = \frac{\epsilon_0}{2}\int E^2d\tau
$$

(you may remember agonizing over that factor of 2.)

In Chapter 7, I don't think we talked about this in class but we got
that the work required to get currents going (recall that emf's always try to
resist changes in currents):

$$
W = \frac{1}{2\mu_0}\int B^2d\tau
$$

If you put those together and ask how much energy is carried by a combined
electromagnetic field you get.

$$
u = \frac{1}{2} \left(\epsilon_0E^2 + \frac{1}{\mu_0}B^2\right)
$$

the derivative of which is the first term in Poynting's theorem. 

**The second term: the rate of energy transported out of the volume**

The second term is the rate at which energy is transported out of the volume bounded
by the surface that you're integrating over.

So Poynting's theorem says that the work done on the charges by the electromagnetic
force is equal to the decrease in energy remaining in the fields, less the energy that
flowed out through the surface.

The integrand of the second term has a name, the Poynting Vector:

$$
\vec{S} = \frac{1}{\mu_0}(\vec{E}\times\vec{B})
$$

$$\vec{S}\cdot d\vec{a}$$ is the energy per unit time crossing the 
surface $$d\vec{a}$$, so S is the energy flux density.

### Major punchline
**S is the energy flux density.**

(We did a brief review here before we moved on to the Maxwell Stress Tensor)


### Maxwell Stress Tensor

There's a thing called a Stress Tensor, and it helps you do problems involving
momentum, but it looks
totally intimidating at first. 

Can I show it to you backwards?

Here's how you find the ij element of the stress tensor, $$\overline{T}$$.

$$
T_{ij} = \epsilon_0\left(E_iE_j - \frac{1}{2}\delta_{ij} E^2\right) + \frac{1}{\mu_0}\left(B_i B_j - \frac{1}{2}\delta_{ij}B^2\right) 
$$

Griffiths writes it with two arrows, but I'm overlining it in my notes.

Before you have time to get intimidated let's do an example:

**Problem 8.7**

Consider an infinite parallel-plate capacitor, with the lower plate (at  z = −d/2) carrying surface charge density −σ, and the upper plate (at z = +d/2)  carrying charge density +σ.  

(a) Determine all nine elements of the stress tensor, in the region between the  plates. Display your answer as a 3 × 3 matrix: 

So we have our matrix:

$$
\begin{matrix}
T_{xx} & T_{xy} & T_{xz}\\
T_{yx} & T_{yy} & T_{yz}\\
T_{zx} & T_{zy} & T_{zz}
\end{matrix}
$$

What's $$T_{xx}$$?

To calculate that it looks like we need the field in the x-direction. There's no
magnetic field in this problem at all, so the B's are all zero.  The E field is all
in the z-direction.  So $$E_x$$ and $$E_y$$ are zero. So any term involving
$$E_x$$ or $$E_y$$ has to be zero.  The field in z is

$$
E_z = -\frac{\sigma}{\epsilon_0}
$$

(You can get that using Gauss' law if that's not a thing you just happen to remember off
the top of your head. You might also remember that the field from a sheet is independent
of distance, proportional to surface charge density, and that the units of field
are charge per area divided by $$\epsilon_0$$ so really what else could it be?)

So the only non-zero thing in $$T_{xx}$$? is the 
$$- \frac{1}{2}\delta_{ij} E^2  $$
where that E is the total field, and $$\delta_{ij}$$ is 1 when $$i=j$$.
So

$$
T_{xx} = \epsilon_0 \frac{1}{2} \left(-\frac{\sigma}{\epsilon_0}\right)^2 = -\frac{\sigma^2}{2\epsilon_0}
$$

$$T_{zz}$$ is only slightly more complicated because it's got a non-zero $$E_z^2$$ term.


$$
T_{zz} = \epsilon_0\left(E_z^2 - \frac{1}{2} E^2 \right) = \epsilon_0 \left[\left( -\frac{\sigma}{\epsilon_0}\right)^2 - \frac{1}{2} \left(-\frac{\sigma}{\epsilon_0}\right)^2\right] = \frac{\sigma^2}{2\epsilon_0} 
$$

So now actually we have all the elements of our matrix:
$$
\overline{T} =\left(\begin{matrix}
-\frac{\sigma^2}{2\epsilon_0} & 0 & 0\\
0 & -\frac{\sigma^2}{2\epsilon_0} & 0 \\
0 & 0 & \frac{\sigma^2}{2\epsilon_0}
\end{matrix}
\right)
$$

Which we can also write as:

$$
\overline{T} =\frac{\sigma^2}{2\epsilon_0} 
\left(
\begin{matrix}
-1 & 0 & 0 \\
0 & -1 & 0 \\
0 & 0 & 1
\end{matrix}
\right)
$$

Okay but I claimed that somehow made our life easier.  Next part of the problem!!

(b) Use Eq. 8.21 to determine the electromagnetic force per unit area on the top  plate. Compare Eq. 2.51. 


What's 8.21?  I didn't give you that one yet.  Here it is:

$$
\vec{F} = \oint_S \overline{T}\cdot d\vec{a}
$$

This equation (which is derivedin Griffiths section 8.2.2) tells you what $$\overline{T}$$
is physically.  It's the force per unit area (aka stress) acting on the surface. 
$$T_{ij}$$ is the force per units area in the ith direction acting on an element of surface
oriented in the jth direction.  

So let's think about that for a second.  If the force and the surface are in the same
direction, then force per area is just pressure.  So the diagonal elements are pressures.

What about the off-diagonal elements?  If the force and the surface area are in orthogonal
directions that's a shear (the force is along the surface.)  So the off-diagonal elements
are shears.  In this problem we're doing we don't have any forces along the surface of
the capacitor plates, so the off-diagonal elements are zero.

But let's go back to our problem at hand.  We're supposed to use that equation to
calculate the force per unit area on the top plate.

We have to use this equation with a closed surface. So let's draw a box around the
top plate.  The area of the box on the top and bottom is A.  We didn't talk about the
stress tensor outside the capacitor, but there's no field there, so T=0 there.  No contribution.  We'll make the sides of the box so skinny that there's no contribution there (but actually
if you did make them the opposite sides would cancel out because their $$d\vec{a}$$'s are
in opposite directions. So we're left with the bottom plate.  $$\vec{a} = -A\hat{z}$$  
So when we do the integral we get:

$$
F_z = -\frac{\sigma^2}{2 \epsilon_0} A
$$

and the force per unit area is $$\vec{f} = \frac{F}{A} = -\frac{\sigma^2}{2\epsilon_0}\hat{z}.$$

(And yes, that's the same thing we got in chapter 2.)

(c) What is the electromagnetic momentum per unit area, per unit time, crossing  the x y plane (or any other plane parallel to that one, between the plates)? 

Oh I can calculate mometum using the stress tensor, too?  Yes!  Isn't that awesome??

Wait, what kind of momentum are we talking about...because there's nothing moving here.
It's electromagnetic momentum.  It's the momentum stored in the fields. According
to Newton's second law, the force on an object is equal to the rate of change of
its momentum, and we just calculated that there's a force on each of these plates, so
therefore there's an electromagnetic momentum stored in them.

$$
\vec{F} = {d\vec{p}}{dt}
$$

It turns out that $$-\overline{T}\cdot d\vec{a}$$ is the electromagnetic
momentum per unit time passing through the area $$d\vec{a}$$.
Any area vector in the xy plane is pointing in the z direction. The z vector is (0,0,1)
so we can dot the tensor into the vector and we get the zz component.  So the
electromagnetic momentum per unit area, per unit time, crossing the xy plane
or any plane parallel to that one is $$-{\sigma^2}{2\epsilon_0}$$

(d) Of course, there must be mechanical forces holding the plates apart—perhaps  the capacitor is filled with insulating material under pressure. Suppose we suddenly remove the insulator; the momentum flux (c) is now absorbed by the  plates, and they begin to move. Find the momentum per unit time delivered to  the top plate (which is to say, the force acting on it) and compare your answer  to (b). [Note: This is not an additional force, but rather an alternative way of  calculating the same force—in (b) we got it from the force law, and in (d) we  do it by conservation of momentum.] 

It's the momentum delivered per unit time, so it's  $$-{\sigma^2}{2\epsilon_0}$$ which
is what we got in (b).  So we calculated the force using the force per area and using
the time derivative of momentum.

That was not super earth-shattering but it:
* Shows you how to use the stress tensor.
* Shows you that there's consistency between force and momentum as their should be.  In
fact there's a continuity equation for force and momentum:

$$
\frac{\partial \vec{g}}{\partial t} = \nabla \cdot \overline{T}
$$

Griffiths calls it the continuity equation for electromagnetic momentum, but you can also 
just call it the conservation of momentum.

Okay but wait, what's g?  (I told you I was doing this backwards.)

$$
\vec{g} = \mu_0\epsilon_0\vec{S} = \epsilon_0(\vec{E} \times \vec{B})
$$

So the Poynting vector is proportional to momentum density ( and remember momentum
density and energy have the same units.)

### Next time:
We'll take this idea of the Poynting vector and use it to calculate the energy
transferred across boundaries in an electromagnetic wave.  In other words, we'll
calculate transmission and reflection coefficients.
