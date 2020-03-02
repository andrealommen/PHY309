---
layout: page
title:  "Lorentz Force Law and Biot-Savart"
permalink: "/lectures/lorentz"
---

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
