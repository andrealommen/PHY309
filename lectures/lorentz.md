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

The version of this with currents instead of charges (which is way more useful is)

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
\vec{B}(P) = \frac{\mu_0}{4\pi} \int \frac{\vec{I} \times \hat{\mathscr{r}}}{\mathscr{r}^2}dl = \frac{\mu_0}{4\pi}I \int \frac{\vec{dl} \times \hat{\mathscr{r}}}{\mathscr{r}^2}
$$

If you integrate this over an infinite line charge (which Griffiths does on page 209)
you get something that would be much easier to get using Ampere's Law, which
we haven't gotten to yet...

$$
B = \frac{\mu_0 I}{2\pi d}
$$


Problem 5.12, page 212:

Suppose you have two infinite straight line charges $$\lambda$$, a distance $$d$$ apart, moving along at a constant speed $$v$$ (Fig. 5.24). How fast would $$v$$ have to be in order for the magnetic attraction to balance the electrical repulsion?  Work out the actual number... is this a reasonable sort of speed?

