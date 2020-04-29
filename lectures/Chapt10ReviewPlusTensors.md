---
layout: page
title:  "Chapter 10 review Plus Relativity in Chapter 12"
permalink: "/lectures/Chapt10ReviewPlusTensors"
---

As I make these last two crash courses (chapter 10 and chapter 11) I'm going
to pay particular attention to the transitions between chapters.  For example,
what did you learn in Chapter 9 that allowed you to think about Chapter 10?  

In addition, by popular demand, I am paying particular attention to
gauge transformations, and the deferred potential.  Here goes....

Remember that in Chapter 9 we had finally achieved electromagnetic
radiation.  We spent the first 7 chapters getting all the pieces of
Maxwell's Equations (and in particular in chapter 7 we added the
tme-dependent pieces) and then we finally had the full versions
of Maxwell's equations so that we could make waves.

In Chapter 10 we had to go back to the potential formulation, because
our addition of the time-dependent pieces of Maxwell's equations changed
how we can express the potential.  

In particular we added a term to the relationship between E and V namely

$$
\vec{E} = - \nabla V - \frac{\partial\vec{A}}{\partial t} 
$$

Notice that this allows Faraday's law with the time-derivative
to be true:

$$
\nabla \times \vec{E} = -\frac{\partial\vec{B}}{\partial t}
$$

(Before we added $$-\frac{\partial\vec{A}}{\partial t}$$ to
the formula for E we could only get $$\nabla \times \vec{E}=0$$
so that's what we had to fix.)

Using our new relationship, and replacing E and B in Maxwell's
equations with A and V, we got something that starts to look
 like a wave equation (two derivatives wrt space minus two derivatives
with respect to time equals zero.) Mathematically the wave equation is

$$
\left(\nabla^2\vec{A} - \mu_0 \epsilon_0 \frac{\partial^2 \vec{A}}{\partial t^2 }\right)
- \nabla\left(\nabla\cdot\vec{A} + \mu_0\epsilon_0\frac{\partial V}{\partial t}\right) = -\mu_0\vec{J}
$$

$$
\nabla^2 f - \frac{1}{v^2}\frac{\partial^2 f}{\partial t^2} = 0
$$
That's not specific to E&M.  That's any physical quantity f where that equation is
true permits oscillating waves of whatever f is that travel at velocity $$v$$.


We were excited about this because it bears resemblance to a wave
equation and it's got some sources in it, so we're honing in on something
that could actually generate electromagnetic waves, rather than just allow them.
(You can say that up until now, all we knew is that Maxwell's equations allow
EM waves, but we didn't know how to generate them.)

But it still doesn't look exactly like a wave equation, because it's got all this extra
stuff in it.  Can we make that go away somehow?    Yes, in fact a gauge
transformation is exactly the thing that will just kind of make that go away.

### Gauge Transformations (10.1.2)

Just as before, our two new equations do not uniquely determine the potentials.  We
can add things to V and $$\vec{A}$$ as long as they don't change E and B.  That's
called "gauge freedom".

The bottom line is that to A we can the gradient of any scalar $$\lambda$$ as 
long as we subtract the time-derivative of that same scalar from $$V$$.

$$
\vec{A}^\prime = \vec{A} +\nabla \lambda
$$

$$
V^\prime = V - \frac{\partial \lambda}{\partial t}
$$

And what I mean by "can" is that these two new potentials give us the same
E and B that we had before.

I really do think about this the same way as I think about adding a scalar
to a potential when doing electrostatics.  You were okay when we called the
"ground" the zero of potential, and any height above that gave you a significant
gravitational potential or significant voltage (i.e. electric potential). And you
knew that I could move my "ground" to whatever height or whatever voltage I wanted
to make the problem easier for me.  If I have a ball rolling down an inclined plane,
it'd be silly to put the zero of potential below 10 meters below the bottom of 
the plane given te problem I'm trying to do.  Same here - there are choices you
can make that lend themselves to the problem at hand.

We talked about two gauges - the Coulomb gauge and the Lorenz gauge.  I'm going
to concentrate on the Lorenz gauge because that's what we need to get the wave
equation.

### The Lorenz gauge

Here we pick

$$
\nabla \cdot \vec{A} = \mu_0\epsilon_0\frac{\partial V}{\partial t}
$$

If you do that you get rid of the middle term in the equation I had you rearrange
above

$$
\left(\nabla^2\vec{A} - \mu_0 \epsilon_0 \frac{\partial^2 \vec{A}}{\partial t^2 }\right)
- \nabla\left(\nabla\cdot\vec{A} + \mu_0\epsilon_0\frac{\partial V}{\partial t}\right) = -\mu_0\vec{J}
$$

So now it's:

$$
\left(\nabla^2\vec{A} - \mu_0 \epsilon_0 \frac{\partial^2 \vec{A}}{\partial t^2 }\right)
= -\mu_0\vec{J}
$$

That operator on the left has a name:

$$
\nabla^2 - \mu_0 \epsilon_0 \frac{\partial^2 }{\partial t^2 } = \square^2
$$

It's called the d'Alembertian.

The equation for V becomes similarly simpler and you get.
In the Lorenz gauge you can write our final two equation as:

$$
\square^2V = -\frac{1}{\epsilon_0}\rho
$$

$$
\square^2\vec{A} = -\mu_0\vec{J}
$$

The d'Alembertian is a natural generalization of the Laplacian.  
Both V and A satisfy the wave equation.
The wave equation

$$
\square^2f = 0
$$

So the
equations above can be regarded as 4-D versions of Poisson's equations. 

And what does this have to do with relativity?

## Relativity

I think I hinted that you could combine V and A into a 4-vector like this:

(12.132)

$$
A^\mu = (V/c, A_x, A_y, A_z)
$$

What's a 4-vector?  A 4-vector is a 4-dimensional vector.  3 of the components
look just like space components that you're used to. So the last 3 components
are just the vector potential you're used to, i.e. you could write the vector
potential as

$$
\vec{A} = (A_x, A_y, A_z)
$$

but now we're adding a 4th component.  It's called the 'time-like' component.  
It's not obvious in the case of potentials that it's like time, but notice
that in all cases (e.g. in the one I'm about to show you with charge density
and current density) in order to get the first component into the 4-vector, you
always have to manipulate some familiar quantity a factor of the speed of light in order for
it to have units that match the other quantities in the 4-vector.  The units of
all 4 things have to be the same. (Just like the units in the 3-vectors you're
used to all have to be the same.)

For example the coordinates of an object in space in relativity are:

$$
x^\mu = (-ct, x, y, z)
$$

So that's what I mean - you have to multiply time by $$c$$ in order to get
it into the same units as the others.

You'll also need the general form of charge and current density:

Based on this, how do you think you make them into a 4 vector?  

(12.124)

$$
J^\mu = (c\rho, J_x, J_y, J_z)
$$ 

Makes sense, right?  Because current density is charge per time per area.  And
charge density is charge per volume, so to translate from one to the other
you need to exchange a space unit for a time unit.  And to do that you mulitply
the charge density by $$c$$.

We'll get to more of this later, but why would you want to do this?  I thought
physics was working perfectly well with the 3 vectors. We spent almost the whole
semester thinking of charge and current density as different things, and it all
works out.  Why do this?  

The thing is that there's sloshing between these things depending on what reference
frame you're in.  That's the whole point of making things into 4 vectors.  Depending
on what reference frame you're in a charge density in one frame is going to look
like a current density in another.    I actually think it's a little easier to
understand how a reference frame can turn $$\rho$$ into $$\vec{J}$$ (or V into $$\vec{A}$$) than it is
to understand how a reference frame can turn time into space.  But that's the
essence of relativity.

The bottom line is that if you're going a reasonable fraction of the speed of
light, these effects become important and you need to account for them in Maxwell's
equations.

(I think you can skip the general Maxwell equations in tensor form (pg 567),
because that's before we have general form of potential)

and the field tensor F can be written like this:

12.133 (The field tensor gives you all the relationships between the
potentials and the fields.)

$$
F^{\mu \nu} = \frac{\partial A^\nu}{\partial x_\mu} - \frac{\partial A^\mu}{\partial x_\nu}  
$$

That's pretty cute, no?

Okay, but if you're thinking that's so cute it's useless, because I don't know what
it means, I totally sympathize.


Let's figure out what it means, because I know that I haven't told you how to
deal with these $$\mu$$'s and $$\nu$$'s.  $$F^{\mu \nu}$$ is a tensor.  You can 
think of $$\mu$$ as the row-number and $$\mu$$ as the column-number.  

And here's what the Field tensor represents:
(12.119)

$$
F^{\mu \nu}=
\begin{pmatrix}
0 & E_x/c & E_y/c & E_z/c \\
-E_x/c & 0 & B_z & -B_y \\
-E_y/c & B_z & 0 & B_x\\
-E_z/c & B_y & -B_x & 0 \\
\end{pmatrix}
$$

If we have timr on Wednesday when I convince you that
one person's E-field is another person's B-field (if the two people
are not at rest w.r.t. each other), but for now just notice that
this matrix has off-diagonal elements.  What quality does a matrix
need to have in order to mix components of a vector when you
multiply the vector by the matrix?  Yes, off-diagonal elements.  
So this matrix is setting us up to mix E and B components.  In other
words, one person's E is another person's B. 

Let's see if we can get the equation for E out of it.  Let's look at $$\mu=0$$
and $$\nu=1$$.  So the zeroth row and 1st column is supposed to be $$E_x$$.

$$
F^{0 1} = \frac{\partial A^1}{\partial x_0} - \frac{\partial A^0}{\partial x_1}
$$

Oh wait!!!  So $$x_0$$ is time (ct actually), so that first thing is the derivative
of the vector potential with respect to time.  And $$A_0$$ is the scalar potential
V, so that second thing is the spatial derivative of $$A$$.

So this is

$$
E_x/c = -\frac{1}{c} \left(\frac{\partial A_x}{\partial t} + \frac{\partial V}{\partial x}\right)
$$

$$
E_x/c = -\frac{1}{c} \left(\frac{\partial \vec{A}}{\partial t} + \nabla V\right)_x
$$

And actually once we did that for $$\nu=2$$ and $$\nu=3$$ we'd have:
$$
\vec{E} = - \left(\frac{\partial \vec{A}}{\partial t} + \nabla V\right)
$$

Can we boldly get $$\vec{B}$$ as well?  This one is actually more straightforward.

Try $$\mu=1$$ and $$\nu=2$$

$$
F^{1 2} = \frac{\partial A^2}{\partial x_1} - \frac{\partial A^1}{\partial x_2}
$$

$$
B_z = (\nabla \times \vec{A})_z 
$$

And Maxwell's equations then look like this:

$$\frac{\partial F^{\mu\nu}}{\partial x^\nu} = \mu_0 J^\mu$$

$$\frac{\partial G^{\mu\nu}}{\partial x^\nu} = 0$$

## This is how far we got on the first day of this lecture.

I think that I was never convinced that this was an easier/more elegant way to
write out Maxwell's equations until I texed up this lecture.  That was so much
easier to write Maxwell's equations that writing out Gauss's Law, Faraday's law, etc...
all those vectors....sheesh.

And I thought electrodynamics was pretty elegant before we did this.  The fact that
you can say everything that happens to E&M fields with just those 4 equations is
stunning.

But this is craziness.
And how do we get the inhomogenous equations - the ones that are related to
current density and charge density?  

Let's tackle this in terms of the potentials, and figure out what it means.  
And we're going to get back to the Lorenz
gauge condition as well.


$$\frac{\partial }{\partial x_\mu}\left( \frac{\partial A^\nu }{\partial x^\nu}\right)
-\frac{\partial }{\partial x_\nu}\left( \frac{\partial A^\mu }{\partial x^\nu}\right)
 = \mu_0 J^\mu$$


Whenever there is an index
repeated in a term, like the $$\mu$$ in the first term of the first equation, it
means you sum over it.

So now, finally, let's look at the Lorenz gauge condition.

$$
\nabla\cdot\vec{A} = -\frac{1}{c^2}\frac{\partial V}{\partial t}
$$

In relativistic notation the gauge condition becomes:
$$\frac{\partial A^\mu}{\partial x^\mu} = 0$$

Do you see it!??  That's cute right?  Because the 0th component of A is V/c.  It works!

Then our inhomogenous equation becomes (because the first term goes away):

$$
-\frac{\partial }{\partial x_\nu}\left( \frac{\partial A^\mu }{\partial x^\nu}\right)
 = \mu_0 J^\mu
$$

Which is :

$$
\square^2 A^\mu = -\mu_0 J^\mu
$$

where

$$\square^2 \equiv 
\frac{\partial }{\partial x_\nu}\frac{\partial }{\partial x^\nu} = \nabla^2 - \frac{1}{c^2}\frac{\partial^2}{\partial t^2}
$$

So we got our wave equation back!!

If you want more information on this.

Sections 12.1 and 12.2 just review relativity and have nothing to do with
electrodynamics. 

Sections 12.3 shows you how magnetism is a relativistic phenomenon.
(The current loop on the train)

Page 559 (equation 12.109) shows you how E and B depend on your reference
frame.

And 12.110 and 12.111 are very nice demonstrations of how one person's
E-field is another person's B-field.

So E and B are "stirred together" when you go from one inertial system
to another.

If I have time on Wednesday I would like to show how a Lorentz
transformation mixes together E and B, using the formalism I just
showed you.

## The Deferred Potential:

Where did it come from?   We kinda got it out of thin air. We said that it
satisfies the inhomegenous wave equation. (Griffiths proves that it does
on page 446.)

$$
V(\vec{r}, t) = \frac{1}{4\pi\epsilon_0}\int\frac{\rho(\vec{r}^\prime, t_d)}{\mathscr{r}}d\tau^\prime
$$

$$
\vec{A}(\vec{r}, t) = \frac{\mu_0}{4\pi}\int\frac{\vec{J}(\vec{r}^\prime, t_d)}{\mathscr{r}}d\tau^\prime
$$

where

$$
t_d = t - \frac{\mathscr{r}}{c}
$$


The Leinard-Wiechert potentials for a moving point charge.

$$
V(\vec{r},t) = \frac{1}{4\pi \epsilon_0}\frac{qc}{(\mathscr{r}c - \vec{\mathscr{r}}\cdot\vec{v})}
$$

where $$\vec{v}$$ is the velocity of the charge at the deferred time, and $$\vec{r}$$
is the vector from the deferred position to the place you're calculating the
field $$\vec{r}$$.

The vector potential is nice and simple:

$$
\vec{A}(\vec{r},t) = \frac{\vec{v}}{c^2}V(\vec{r},t)
$$

And from these we got the fields of a moving point
charge:

$$
\vec{E}(\vec{r},t) = \frac{q}{4\pi \epsilon_0}\frac{\mathscr{r}}{(\vec{\mathscr{r}}\cdot\vec{u})^3}\left[(c^2 - v^2)\vec{u} + \mathscr{r}\times(\vec{u}\times\vec{a})\right]
$$

And B:

$$
\vec{B}(\vec{r},t) = \frac{1}{c}\hat{r} \times \vec{E}(\vec{r},t)
$$

Question for you:  If velocity and acceleration are both zero, what do you
get? (It should be familiar to you.)

Ans:
$$
\vec{E}(\vec{r},t) = \frac{q}{4\pi \epsilon_0}\frac{q\mathscr{r}}{\mathscr{r}^2}
$$


Wait, how are these different from E and B fields we had back in chapter 1-6?

Well, that last one isn't, because that's the field of a non-moving point charge.But in order to calculate the field from a charge distribution that has a time
dependence, we needed to know how Maxwell's equations depend on time.  So we
needed chapter 7.  We could have actually gone from chapter 7 to chapter 10
without talking about electromagnetic radiation.  We could have figured
out that the wave equation came from the Lorenz gauge on Maxwell's conditions
and that of the time dependent solutions to Maxwell's equations, there must
be one where there's a wave that propagates to infinity.


## Covariant and contravariant vectors
You may have noticed that some of the indices are superscripts and some are
subscripts. They differ from each other by the sign of the zeroth component.

Much more information on this is on page 525-527 of your text 12.1.4 where they
introduce four vectors. To do relativity right, you have to scrupulously keep 
track of whether something is covariant or contravariant. The rules of
dealing with the notation do that for you.  And as in that equation we
have for Maxwell's inhomogenous equations above, if you have $$\mu$$'s on the
left and no$$\mu's$$ on the right, then you better have both an upper
and a lower $$mu$$ on the left.  It means you're summing over them.
