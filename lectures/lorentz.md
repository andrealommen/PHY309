---
layout: page
title:  "Lorentz Force Law and Biot-Savart"
permalink: "/lectures/lorentz"
---

We start magnetic fields today!  So far, all our charges have been stationary.  Now they can move.

So then whether something is an electric or magnetic field depends upon what reference frame you're
in?? (absolutely!!!)  So the two better be intimately related.  We'll get there...but not today.  Our
goals for today are a little more sedate:

### Goals:
* Remember the formula for Lorentz force.  (Given a magnetic field, you should be able to calculated the force)
* Remember the Biot-Savart Law. (Given a current, calculate the magnetic field)  We actually aren't going to
confont the specific integral in the Biot-Savart law. I'm letting Griffiths do that.  He does a nice
integral of a line charge. 

## The Lorentz Force Law

$$
F_{mag} = Q(\vec{v} \times \vec{B})
$$

When you combine it with the electric force you get:

$$
F = Q[ \vec{E} + (\vec{v} \times \vec{B})]
$$

The most interest result of the Lorentz force or the magnetic force is that
it causes things to go in circles, and the magnetic force can do no work.

(Show magnetic field pointing into the board, and velocity pointing to the right).

If you don't have just one charge, but a line of charge (for example) then
you can integrate over it. (We're getting toward current - that's what we
almost always mean by a line of charge moving at some velocity along
the line.)

$$
F_{mag} = \int (\lambda dl) (\vec{v} \times \vec{B})
$$

You can tell that's the same formula as above right?  You just have to do the
integral over all the pieces of charge?

But presumably the current is traveling along the direction $$\vec{dl}$$
or really the whole thing doesn't make much sense.  And $$\vec{I}$$ is 
charge per time...

Casually speaking...

$$
I = \frac{charge}{time} = \frac{charge}{length} \frac{length}{time} 
$$

$$
\vec{I} = \lambda \vec{v}
$$

So then...

$$
F_{mag} = I \int d\vec{l} \times \vec{B}
$$


## But we need a way to calculate the magnetic field in the first place for this
to be useful:

### The Biot-Savart Law:
(the magnetic field of a steady current)

$$
\vec{B}(\vec{r}) = \frac{\mu_0}{4\pi} \int \frac{\vec{I} \times \hat{\mathscr{r}}}{\mathscr{r}^2}dl^\prime = \frac{\mu_0}{4\pi}I \int \frac{\vec{dl^\prime} \times \hat{\mathscr{r}}}{\mathscr{r}^2}
$$

$$\mu_0$$ is the permeability of free space. $$\mathscr{r}$$ is the vector
from the source point to the point $$\vec{r}$$.

If you integrate this over an infinite line charge (which Griffiths does on page 225)
you get something that would be much easier to get using Ampere's Law, which
we haven't gotten to yet...

$$
B = \frac{\mu_0 I}{2\pi d}
$$

You can find the direction of $$\vec{B}$$ using the right hand rule. 


In groups:

Problem 5.12, page 212:

Suppose you have two infinite straight line charges $$\lambda$$, a distance $$d$$ apart, moving along at a constant speed $$v$$ (Fig. 5.24). How fast would $$v$$ have to be in order for the magnetic attraction to balance the electrical repulsion?  Work out the actual number... is this a reasonable sort of speed?

This problem was super cool, because the answer is the speed of light.  We 
talked about how this equalling of magnitudes of forces is the same equalling
of magnitudes that allows an electromagnetic wave to travel.  It can
only travel at $$c$$ because that's where the magnitudes are equal.

## Jumping 5 chapters ahead (roughly)

This is jumping about 5 chapters ahead, but I think it's instructive to see how we're going
to derive the wave equation:

Maxwell's equations in a vacuum (no charges or currents...which is, admittedly a really different
situation than we are dealing with in this chapter.)

Gauss' Law

$$
\nabla \cdot \vec{E} = 0
$$


(no name...no magnetic monopoles?)

$$
\nabla \cdot \vec{B} = 0
$$

Faraday's Law

$$
\nabla \times \vec{E} = -\frac{\partial\vec{B}}{\partial t}
$$

Ampere's Law 

$$
\nabla \times \vec{B} =  \mu_0 \epsilon_0 \frac{\partial\vec{E}}{\partial t}
$$

Take the curl of both sides of Faraday's Law:

$$
\nabla \times \nabla \times \vec{E} = -\nabla \times \frac{\partial\vec{B}}{\partial t}
$$

Use the vector identity (math, not physics!)

$$
\nabla \times \nabla \times \vec{G} = \nabla(\nabla\cdot\vec{G}) - \nabla^2 \vec{G}
$$

where $$\vec{G}$$ is any vector.

So now we have
$$
\nabla(\nabla\cdot\vec{E}) - \nabla^2 \vec{E} = -\frac{\partial}{\partial t}(\nabla \times \vec{B})
$$

Then use Ampere's law and Gauss's law to get:

$$
\nabla^2 \vec{E} = \frac{1}{c^2} \frac{\partial^2\vec{E}}{\partial t^2}
$$

Don't let the fancey $$\nabla$$ fool you. That's just two spatial derivatives on the left,and two
time derivatives on the right.

And that's how you get ..

$$
c = \frac{1}{\sqrt{\mu_0 \epsilon_0}}
$$

because the solutions of it look like:

$$
E = E_0 \sin{kx - \omega t}
$$

and $$\omega/k$$ = c

So what does our parallel wire example have to do with the speed of light?  

Light only travels because by Faraday's law an E-field is getting induced by a B-field that's
changing in time, and that E-field changing in time, by Ampere's law is inducing a B-field that's
changing in time.  It's cool enough that they induce each other, but in order for the wave
to propagate they have to induce each other exactly enough that the amplitude of the wave
stays constant.  If it doesn't, it either peters out very quickly, in which case it's not
a propagating wave, or its amplitude expands as it travels, which is unphysical (although
very much like a tidal wave, so it's not unphysical in water!)

However, the amazing thing is that there's a particular speed it travels that makes it
so the E-field replicates the B-field at exactly the same amplitude it started at, and the B-field
replicates the E-field at exactly the same amplitude it started at, and the wave can propagate forever.

Woah.

This actually helps us think a big about $$\mu_0$$ and $$\epsilon_0$$ and what they represent.
Let's back up a bit. Do you remember in 213 (or in your waves class) where we usually got

$$
v_{string} = \sqrt{\frac{T}{\mu}}
$$

Where $$T$$ is the tension and is related to the restoring force, and $$\mu$$ is the mass per unit
length of the string and therefore related to the inertia?  You need
both to make something oscillate.  The restoring force keeps returning it to zero, and the inertia
makes it over-shoot the zero-point. 

We've got the same thing here.  The permittivity $$\epsilon_0$$ is the thing that is trying
to undo the electric field (see our discussion of polarization). And the permissivity $$\mu_0$$, or
rather $$1/\mu_0$$ in Faraday's law is the thing that tells us how good the magnetic field
is at reproducing itself. (We haven't really gotten to Faraday's law yet, but you remember the
basic idea.  You always figure out the direction of current caused by induction by asking which
way the current has to go to counteract the change in magnetic field.  That's inertia - the 
magnetic field doesn't like to change. 

If we put this together, the square root of the restoring force $$1/\epsilon_0$$ divided by the 
inertial property $$\mu_0$$ then we get

$$
v = \frac{1}{\sqrt{\mu_0 \epsilon_0}}
$$
