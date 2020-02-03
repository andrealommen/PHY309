---
layout: page
title:  "Boundary Conditions and Conductors"
permalink: "/lectures/conductors"
---
This is Griffiths 2.3.5 and 2.5.

As you come into class today: Be prepared to answer this question:

An uncharged spherical conductor centered at the origin has a  cavity of some weird shape carved out of it (Fig. 2.46). Somewhere within the  cavity is a charge q. Question: What is the field outside the sphere? 
(Griffiths example 2.10)


The answer is:

$$
\vec{E} = \frac{1}{4\pi\epsilon_0} \frac{q}{r^2}\hat{r}
$$

In other words, it's the same as a point charge $$q$$ at the origin.

We can use Gauss's law to get the field.

$$
\int \vec{E}\cdot d\vec{a} = \frac{1}{\epsilon_0} Q_{\rm enclosed}
$$

But if you have a question about whether we can really say that
you're right to question it.

All that really says is that the flux summed over the surface
is equal to $$\frac{q}{\epsilon_0}$$.  If we can argue that the field $$\vec{E}$$
is constant over a spherical surface centered at the origin then
we could say that 
$$
\vec{E} = \frac{1}{4\pi\epsilon_0} \frac{q}{r^2}\hat{r}
$$
but can we say that?

A conductor is defined as a substance that contains *unlimited*
free electrons.  Metals come pretty close.  If you have
unlimited free electrons it turns out you can quickly say
the following about a conductor:

* $$\vec{E}=0$$ inside a conductor.  To be clear ``inside" means
within the conducting material itself, not within a cavity
within a conductor like the one I drew above.  If we place a
conducting ball for example inside a constant external
field the charge would get moved around until the
field due to induced exactly balanced the external field.
* $$\rho=0$$.  That follows from the first bullet point and $$\nabla\cdot\vec{E} = \frac{\rho}{\epsilon_0}$$.
* All charge is surface charge. (Follows from above above.) If
there is any net charge on the conductor it has to go somewhere, and
by the 2nd rule it has to be on the surface somewhere.
* A conductor is an equipotential. Pick any two points in or
on a conductor and integrate the electric field between them: $$ \int_a^b \vec{E}\cdot d\vec{l} $$.  Because the field $$\vec{E}$$ is
zero everywhere, that integral must be zero everywhere.  That integral is the negative of the difference between the potentials $$-(V(\vec{b}) - V(\vec{a}))$$ so $$ V(\vec{a}) = V(\vec{b}) $$ and therefore the potential has to be the same everywhere in/on the conductor.
* $$\vec{E}$$ is perpendicular to the surface, just outside the conductor. If there were any component of the E-field parallel to the surface, that E-field would have moved charge until there was not
parallel component to the E-field.

Okay so let's go back to our example knowing what we know now. 
The outside surface of the conductor is spherical, and that's important. We now know that all surface on the conductor is surface charge,
so all the charge on the conductor is on the inner surface and the outer surface. 

We know the field inside the conductor (NOT INSIDE THE CAVITY!!) is zero, so the field just before we get to the exterior surface of the sphere is zero. So just inside the boundary we know the field is zero, i.e. is spherically symmetric.  We also know by $$\nabla\cdot\vec{E} = \frac{1}{\epsilon_0} Q_{enc}$$ that $$Q_{enc}$$ inside that
surface is zero. So then there must be charge $$q$$ distributed
on the outside surface. And it must be spherically symmetric. So the exterior field is just the field due to that spherically symmetric
exterior charge q.  And therefore the outside field is as we expect:

$$
\vec{E} = \frac{1}{4\pi\epsilon_0} \frac{q}{r^2}\hat{r}
$$


## The charge on the boundaries...
Let's look at the charge on the boundary of a conductor in general. 
Draw a big conductor, not necessarily spherical, and ask what the field is
on the surface.  Let's draw a ``wafer-thin" pill box, the area of
which is $A$. The distribution of charge on this surface may very
well not be uniform, but let's draw our box small enough that we
consider the field to be constant across it. The field inside is
zero, and we just said the field parallel to the surface is zero, so
Gauss' law looks like this

$$
\int \vec{E}\cdot d\vec{a} = \frac{1}{\epsilon_0} Q_{\rm enclosed}
$$

which can write as

$$
EA = \frac{1}{\epsilon_0} \sigma A
$$

where $\sigma$ is the surface charge density at that location. The $$A$$'s cancel and we have:

$$
\vec{E} = \frac{\sigma}{\epsilon_0} \hat{n}
$$

So just outside a conductor, the field is proportional to the 
surface charge.

Let's back up a smidge and pick up the idea of boundary
conditions.

## Boundary Conditions
The field will change by $$\frac{\sigma}{\epsilon_)}$$ when it
crosses any boundary with surface charge $$\sigma$$.

In the example above let's say we weren't on conductor, so we
couldn't say $$\vec{E}_{inside}=0$$.  Then we would have

$$
\vec{E}_{outside} - \vec{E}_{inside} = \frac{\sigma}{\epsilon_0} \hat{n}
$$

(Page 89 of Griffiths)

or more generally

$$
\vec{E}_{above} - \vec{E}_{below} = \frac{\sigma}{\epsilon_0} \hat{n}
$$

(The minus sign appears because $$d\vec{a}$$ points in the opposite
direction on the bottom of the pill box.)

We know $$\vec{E} = -\nabla V$$ so

$$
\nabla V_{above} - \nabla V_{below} = - \frac{\sigma}{\epsilon_0} \hat{n}
$$

Because the right side points completely in $$\hat{n}$$ any parallel
components of $$\nabla V$$ must be the same above and below.  So
then we can write this equation just for the $$\hat{n}$$ component.

$$
\nabla V_{above} \cdot \hat{n} - \nabla V_{below} \cdot \hat{n} = - \frac{\sigma}{\epsilon_0}
$$

aka

$$
\frac{\partial V_{above}}{\partial{n}} - 
\frac{\partial V_{below}}{\partial{n}} 
= - \frac{\sigma}{\epsilon_0} 
$$

So that's your first boundary condition.  That the fields and 
potentials change by a particular amount crossing a boundary,
and that amount is given by the equations above.

## Back to conductors

So if the field inside a conductor is zero, then the field
outside a conductor (by the equation above) is

$$
\vec{E} = \frac{\sigma}{\epsilon_0} \hat{n}
$$

where $$\hat{n}$$ is the vector perpendicular to the surface
pointing exactly outwards.

If you know the potential or the field, you can calculate the
surface charge...

$$
\sigma = \epsilon_0 \frac{\partial V}{\partial n}
$$

## Capacitance

Oh wow let's actually talk about something kind of tangible - 
capacitance.  (I actually consider capacitance to be pretty
abstract, but at least we can go to a store and purchase a 
capacitor of a particular value, so it must be something real.)

$$
C \equiv \frac{Q}{V}
$$

We're in a position to easily calculate the capacitance of two
parallel plates.  Let's put $$Q$$ on the top plate and $$-Q$$
on the bottom plate.  The area of each plate is $$A$$.  

By Gauss's law the field of each is

$$
E = \frac{1}{\epsilon_0} \frac{Q}{A} 
$$

or

$$
E = \frac{\sigma}{\epsilon_0} 
$$

where $$\sigma = \frac{Q}{A}$$ 

To get the potential difference of the plates we integrate
the field between them according to:

$$
\Delta V = \int_{bottom}^{top} \vec{E}\cdot d\vec{l}
$$

The field between them is twice what it is for one plate:
 $$E = 2\frac{\sigma}{\epsilon_0}$$ and the
integral of the field between them is $$d$$, the distance between
them, times $$E$$.

$$
\Delta V = \frac{dQ}{\epsilon_0 A}
$$

and the capacitance is

$$
C = \frac{Q}{V} = \frac{\epsilon_0 A}{d}
$$

And that's what capacitance is a measure of - a configurations ability to hold charge when a given voltage is placed across it. The
larger the capacitance the more charge it can hold for a given
voltage.  So that makes sense that the large the area of the plates
the more charge they can hold.  The shorter the distance...I don't know if I can argue that one based on my intuition.  I get it from
the equation, that voltage difference between the plates
drops as the distance between them dropes, and thus the capacitance
increases....but I'm not sure I could honestly say that that part
makes sense to me - the smaller the distance the larger the
capacitance.

Griffiths figure 2.35 on page 88 is amazing. It gets you between $$\rho$$, $$\vec{E}$$, and $$V$$ in both directions.
