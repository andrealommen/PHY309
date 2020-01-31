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

So let's put some things together here.  Gauss' law, aka
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
V(r) = \frac{-1}{4\pi\epsilon_0} \int_\infty^R \frac{q}{r^\prime}^2dr^\prime - \int_R^r (0) dr^\prime 
$$

Two integrals. We know the field inside is zero by Gauss' Law.  And we know
the field outside is the field of a point charge, from Gauss' Law. We do
an in integral over each different piece.

Now vote again. Is the potential inside the radio R also zero?

#### Work

Let's skip ahead a little so that we can confront *work* and answer this question about the
1/2 in the definition for work.

So I think everyone at least vaguely remembers from 106 or a 106-like class that if
you multiply the potential at a particular point by a charge, that is the amount of work
required to place that charge at that point. (And by the above discussion, we are assuming
that the potential was calculated using infinity as a reference point, and that we are
bringing the charge in from infinity.)

$$
W = q V
$$

or if you have a collection of charges then...

$$
W = \frac{1}{2}\int \rho V d\tau
$$

(Those two formula are in the "Andrea's crash course for Chapter 2" document which I 
encourage you to use.)

So let's tackle this 1/2. (Page 92-93 of Griffiths)

The potential due to a point charge $$q_1$$ is

$$
V_1(r) = \frac{1}{4\pi\epsilon_0}\left(\frac{q_1}{R}\right)
$$

where $$R$$ is the same as Griffith's script r, and is the difference between the position
of the point charge at the point where you're calculating the potential.  Notice in the 
case of potential it's just the distance between those.

So then the work required to put a point charge $$q_2$$ at that location is

$$
W_2=q_2V_1(r) = \frac{1}{4\pi\epsilon_0}q_2\left(\frac{q_1}{R}\right)
$$

$$R$$ was the distance between the point charge $$q_1$$ and the place we're calculating the
potential, so actually that distance $$R$$ is the distance between charge $$q_1$$ and $$q_2$$
so let's call that $$R_{12}$$ now. 

$$
W_2=q_2V_1(r) = \frac{1}{4\pi\epsilon_0}q_2\left(\frac{q_1}{R_{12}}\right)
$$

Now let's add charge $$q_3$$.  This requires an amount of energy 

$$
W_3 = q_3V_{12}
$$

where $$V_{12}$$ is the potential due to the presence of charges 1 and 2. (Griffiths makes 
the point that you need to nail down the charges as you place them so that they don't move
around.)

$$
W_3 = q_3\left[\frac{1}{4\pi\epsilon_0}\left(\frac{q_1}{R_{13}}\right)
+ \frac{1}{4\pi\epsilon_0}\left(\frac{q_2}{R_{23}}\right)\right]
$$

which we can write a little bit more succinctly..

$$
W_3 = \frac{1}{4\pi\epsilon_0}q_3\left[\left(\frac{q_1}{R_{13}}\right)
+ \left(\frac{q_2}{R_{23}}\right)\right]
$$

we can add a fourth charge the same way...

$$
W_4 = \frac{1}{4\pi\epsilon_0}q_4\left[
\left(\frac{q_1}{R_{14}}\right)
+ \left(\frac{q_2}{R_{24}}\right)
+ \left(\frac{q_3}{R_{34}}\right)
\right]
$$

So then the TOTAL work to assemble the 4 charges is the sum of

$$
W = W_2 + W_3 + W_4 = 
\frac{1}{4\pi\epsilon_0}\left[
\left(\frac{q_1q_2}{R_{12}}\right)
+ \left(\frac{q_1q_3}{R_{13}}\right)
+ \left(\frac{q_2q_3}{R_{23}}\right)
+ \left(\frac{q_1q_4}{R_{14}}\right)
+ \left(\frac{q_2q_4}{R_{24}}\right)
+ \left(\frac{q_3q_4}{R_{34}}\right)
\right]
$$

So can you see the rule emerging?

$$
W = 
\frac{1}{4\pi\epsilon_0}
\sum_{i=1}^{i=n}
\sum_{j>i}^{j=n}
\frac{q_iq_j}{R_{ij}}
$$

The $$j>i$$ rule makes it so you don't count any pair twice.  So actually we could just
let it count every pair twice and then divide by 2.

$$
W = 
\frac{1}{2}
\frac{1}{4\pi\epsilon_0}
\sum_{i=1}^{i=n}
\sum_{j \neq i}^{j=n}
\left(\frac{q_iq_j}{R_{ij}}\right)
$$

We can pull the $$q_i$$ out of the second sum, because that sum is over j.

$$
W = 
\frac{1}{2}
\frac{1}{4\pi\epsilon_0}
\sum_{i=1}^{i=n} q_i
\sum_{j \neq i}^{j=n}
\left(\frac{q_j}{R_{ij}}\right)
$$

And put the $${4\pi\epsilon_0}$$ in a differen place so you can see what I'm about to do..

$$
W = 
\left(\sum_{i=1}^{i=n} q_i\right)
\left(\sum_{j \neq i}^{j=n}
\frac{1}{4\pi\epsilon_0}
\frac{q_j}{R_{ij}}\right)
$$

Aha!!  The term in parenthesis is the potential $$V(\vec{r})$$ due to all the OTHER charges
besides $$i$$.   That's what we get because of the $$1/2$$.  In the original expression we
had to make sure that we were assembling them and only counting the work for the new pairs
we added, but now because of the $$1/2$$, we can ask, for each particle, what's the sum of
the potentials of **all** the other particles.  And then divide by $$2$$.

This is easier to write:

$$
W = \frac{1}{2}\sum_{i=1}^{i=n}q_iV(\vec{r_i})
$$

where $$V(\vec{r}_i)$$ is the potential at the point $$\vec{r}_i$$ where you're putting the $$i$$th
particle.

So that's where the $$\frac{1}{2}$$ comes from.

When you have a charge distribution instead of a collection of point charges it looks like this:

$$
W= \frac{1}{2}\int\rhoVd\tau
$$
