---
layout: page
title:  "Potential, Work, and Energy"
permalink: "/lectures/PotentialWorkEnergy"
---

As you come into class today: Be prepared to explain why it makes sense, from
what you know about how charges act in the presence of E-fields and electric
potentials, that there should be a minus sign in both these formulae (we 
could've defined them both without the minus sign, but then we'd have
some problems with our standard ways of thinking abou them):

$$
V(\vec{r}) \equiv -\int_\mathcal{o}^\vec{r} \vec{E}\cdot d\vec{l}
$$

$$
\vec{E} = -\nabla V
$$

So we've already established the the Electric field is curl-less, and therefore
can be expressed as the gradient of a potential.

Griffiths 2.3.2 points out that the possibly familiar fact that the line integral
of E does not depend on the path taken as long as the end points are the same.
(We didn't have time to get to that yesterday, but you can read it in my notes
or in Griffiths.)

He points out that this fact is crucial for the definition of potential

$$
V(\vec{r}) \equiv -\int_\mathcal{o}^\vec{r} \vec{E}\cdot d\vec{l}
$$

to even make sense.
If this weren't true then potential wouldn't depend on your location
relative to the point charges, but rather on the path you took to get
to your location.

But let's back up, potential is a terrible name, and Griffiths has a very
satisfying apology for it. He calls it a "hideous misnomer" because it reminds
you of potential energy, which is different. 

$$\mathcal{o}$$ is a reference point. The only thing
that's meaningful is the difference between two potential points.  That's 
equivalent to saying that the only thing you can measure is the field, which
is the derivative of the potential. 

I identified three ways I think about potential:<br>
1) The thing you take the negative derivative of to get the field. <br>
2) Positive charges fall "down" in potential. <br>
(notice that those two together are internally consistent.  The derivative
(or gradient) will point UP along the greatest slope, and the E-field will
point the other way.  The E-field times the charge is the force, so
a positive charge will be forced down. <br> 
3) To get the work done to bring in a charge from infinity to a particular
point you multiply the potential at that point by the value of the charge. 

In all three of those cases it's true that the only thing that matters is
the difference between two potentials (or the derivative.)  But notice
in the third one the second point is sort of a default point, i.e. infinity.

When we say things like "the potential at a particular point" it is really
shorthand for "the potential at a particular point assuming zero potential
at infinity."  That's the most common zero point, but it's not universal.

Griffiths derives the potential of a point charge at the origin, with the 
reference point being infinity.  He does the integral of the electric
field

$$
\vec{E}(\vec{r}) = \frac{1}{4\pi\epsilon_0}\frac{q}{r^2}\hat{r}
$$

along $$\vec{r}$$ and gets

$$
V(r) = \frac{1}{4\pi\epsilon_0}\frac{q}{r}
$$

You can see how it goes right - the integral gives you a -1, but then the potential
has a minus sign in it, so it's positive again.


So let's put some things together here.  Gauss' law aka
$$
\oint \vec{E} \cdot d\vec{a} = \frac{1}{\epsilon_0} Q_{\rm encl}
$$
and the definition of the potential 
$$
V(\vec{r}) \equiv -\int_\mathcal{o}^\vec{r} \vec{E}\cdot d\vec{l}
$$

(Example 2.7 pg 82)

Find the potential inside a spherical shell of radius $$R$$ and 
charge $$q$$. The charge is evenly distributed over the shell.

First of all, we showed on Wednesday the field inside a uniform spherical
shell is zero using Gauss' law. Is the potential also zero?

(do ABCD response)

So to get the potential, you'll integral the field from infinity down
to $$R$$, and then you'll add to that the integral of the field from $$R$$
down to $$r$$. You'll get the fields from Gauss' law. It'll look like this:

$$
V(r) = \frac{-1}{4\pi\epsilon_0} \int_\infty^R \frac{q}{{r^\prime}^2}dr^\prime - \int_R^r 0 dr^\prime 
$$

Two integrals. We know the field inside is zero by Gauss' Law.  And we know
the field outside is the field of a point charge, from Gauss' Law. We do
an in integral over each different piece.

Now vote again. Is the potential inside the radio R also zero?
