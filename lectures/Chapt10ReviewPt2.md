---
layout: page
title:  "Chapter 10 review (part 2) Plus HW9 review"
permalink: "/lectures/Chapt10ReviewPt2"
---

Just to remind you what we're doing.  Monday was review of Chapter 10.
Chapter 10 is where we got gauge transformations and the deferred potential.
Gauge transformations lend themselves particularly well to 
relativistic notation, so I've been using it as an opportunity to
show you some of Chapter 12.

Today I want to 
* Finish showing you how you can express the Lorenz gauge in relativistic
notation.
* Review a problem on HW9 as a way of reviewing the
deferred potential.
* Review all of Chapter 11.


## Last time

We combined the vector and scalar potentials into a potential 4 vector like this:

$$
A^\mu = (V/c, A_x, A_y, A_z)
$$

which is just like a 4-vector that you're more familiar with.

$$
x^\mu = (-ct, x, y, z)
$$

The basic gist is that once Einstein added time as one of the dimensions
of space,
we need 4 numbers, not just 3, to express quantities.

We also said:

$$
J^\mu = (c\rho, J_x, J_y, J_z)
$$ 

The basic gist of these is that in difference reference frames a
current density will look like a charge density and vice versa.  That's
what these 4-vectors take care of.

There's a really nice example in the book in Chapter 12 of using
Farady's law of induction on a moving train.  Faraday's law has to
work no matter whether you're applying it from the ground outside
the train, or from inside the train itself. I recommend reading that.

In this notation then the field tensor gives you all the relationships between the
potentials and the fields.

$$
F^{\mu \nu} = \frac{\partial A^\nu}{\partial x_\mu} - \frac{\partial A^\mu}{\partial x_\nu}  
$$

And here's what the Field tensor represents:

$$
F^{\mu \nu}=
\begin{pmatrix}
0 & E_x/c & E_y/c & E_z/c \\
-E_x/c & 0 & B_z & -B_y \\
-E_y/c & B_z & 0 & B_x\\
-E_z/c & B_y & -B_x & 0 \\
\end{pmatrix}
$$

Last time we convinced ourselves that the equation above reproduces all
the relationships we're used to for E, B, V, and A.  In particular we
showed we get:

In particular $$\mu=0$$
and $$\nu=1$$ or 2 or 3 gave us....  

$$
\vec{E} = - \left(\frac{\partial \vec{A}}{\partial t} + \nabla V\right)
$$

Similarly we considered $$\mu=1$$ and $$\nu=2$$

$$
B_z = (\nabla \times \vec{A})_z 
$$

And so here it where we continue:

The two inhomogenous Maxwell's equations then look like this:

$$\frac{\partial F^{\mu\nu}}{\partial x^\nu} = \mu_0 J^\mu$$

Let's put in the relationship between the field tensor F and the 4-vector
potential A.

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

## Problem #4 on last week's homework.

Problem 10.30 A uniformly charged rod (length L, charge density λ) slides out  the x axis at constant speed v. At time t = 0 the back end passes the origin (so  its position as a function of time is x = vt, while the front end is at x = vt + L).  Find the deferred scalar potential at the origin, as a function of time, for t > 0. [First  determine the deferred time $t_1$ for the back end, the 
deferred time $$t_2$$ for the front end,  and the corresponding deferred positions $$x_1$$ and $$x_2$$.] Is your answer consistent with  the Liénard-Wiechert potential, 
in the point charge limit ($$L<< vt$$, with λL = q)?  Do not assume $$v<< c$$.  

The posted solutions (on Moodle) are one way of thinking about it.  I think aboutit a little differently, plus I know people wanted help understanding deferred potentials, and I thought this would be a good way to give you more ways of understanding it.

There are two sentences of Griffith's that I think are particularly helpful, so I'm going to quote them. "Now, electromagnetic “news” travels at the speed of light. In the nonstatic case, therefore, it’s not the status of the source right now that matters, but  rather its condition at some earlier time $$t_d$$ (called the [deferred] time) when the  “message” left." (Page 445, first full sentence.)

**Back end**

Let's talk about the back end of the rod first. 

At time $$t=0$$ the back end of the rod is at x=0.  We are supposed to calculate
the deferred potential at x=0, so at t=0, $$t_1 = 0$$ because the back end
of the rod is right where we're calculating the potential, so there's no 'deferment', in other words, we don't have to wait at all to experience the effects
of the back end.

It gets a little more interesting when we consider some general time $$t$$. 
What is $$t_1$$ in general.  Well, as the rod moves to the right, the back
end will get farther and farther away from us at velocity $$v$$. So at time
$$t$$ the back end will be a distance $$vt$$ away from the origin. So is
the 'deferment' $$vt/c$$?  No!  Because remember Griffiths says "it's
not the status of the source right now that matters, but rather its
condition at some earlier time" which in our case is $$t_1$$.  So at $$t_1$$
the back end of the rod was at a distance $$vt_1$$ away from the origin.
And so the deferred time is

$$
t_1 = t - \frac{vt_1}{c}
$$

And if you solve that for $$t_1$$ you get:

$$
t_1 = \frac{t}{(1 + \frac{v}{c})}
$$

Does that make sense?  When $$t=0$$ we said $$t_1=0$$ and that's true!
Also, $$t_1$$ should be earlier than $$t$$ for all $$t>0$$ and that's true 
(An aside: Does this solution work for $$t<0$$?  In that case $$t_1$$ is
later than $$t$$, i.e. less negative.  I'm not sure that makes sense.)

It also makes sense that the faster the speed of light is, the less
the deferment matters (for $$c \rightarrow \infty$$ $$t_1 = t$$.)  

**Front end**

Let's tackle the front end of the rod.

Allow me to do a bad job of this at first and then correct it.  For
$$t_2$$ we want the light or "news" to be able to travel back across
the length of the rod $$L$$ and across whatever space the rod has
moved by that point $$vt$$. So the "deferment" will be roughly $$\frac{L + vt}{c}$$, but that's not quite right.  Because as griffiths says, it's not the status
of the source right now ($$t$$) that matters, but it condition
at an earlier time, $$t_2$$.  So the deferment will actually
be $$\frac{L+vt_2}{c}$$.  So you have to subtract that time from
the current time:

$$
t_2 = t - \frac{L+vt_2}{c}
$$

If you solve that for $$t_2$$ you get

$$
t_2 = \frac{t + L/c}{1 + v/c}
$$

which is very similar to what we got for $$t_1$$ except now there's
an extra term in ther numerator $$L/c$$ which makes sense, because
the front end is a distance $$L$$ away.

Notice in particular that the deferred time for the front end is
different than the deferred time for the back end.  This is an
important point - that all points in your charge distribution have
different deferred times.

The positions of the back and front ends at their
deferred times, $$x_1$$ and $$x_2$$ are

$$
x_1 = vt_1
$$

and

$$
x_2 = L + vt_2
$$

You can subsitute in our expressions above for $$t_1$$ and $$t_2$$.

Then the integral over the charge distribution over the deferred position
is just the integral over $$dx$$ from the end points of the rod.

$$
V(0,t) = \frac{1}{4\pi \epsilon} \int_{x_1}^{x_2} \frac{\lambda}{x}dx
$$

It's a subtle point why we don't have to worry about the length
contraction of the rod.  One idea is that in the integral,
the length contraction makes $$dx$$ shorter and $$\lambda$$ greater
by the same factor, so they cancel each other out.  I'm not sure
I'm totally happy with that, so I'm still thinking about this.  Stay tuned...

In any case, I think this problem does a really nice job forcing you
to think about the issues of deferred time, and what you have to
do to set up the integral over the deferred distribution of the charges.

Based on the little bit we've done on Chapter 12, it would be interesting
to repeat this problem using the 4-vector $$J^\mu$$ and solve it
relativistically using the Lorentz transformation.  In the frame that's
at rest with respect to the origin in the problem above, there should
be a current density $$\vec{J}$$, whereas in the frame moving
with the rod, there will be all $$\rho$$ and no $$\vec{J}$$.
  

## Continuing on with the rest of Chapter 10


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
