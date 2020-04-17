---
layout: page
title:  "The Leinard-Weichert Potential"
permalink: "/lectures/leinard"
---

### What we've been doing this week:

For the last couple of weeks we had been studying waves - waves in media, waves at boundaries, etc.  But we always just assumed the waves existed somehow.  This week we're building
the tools we need to talk about their generation.  How do you actually make a wave in the first place?  Punchline: you accelerate a charge. This week we're just putting 
together the machinery of deferred potentials so that we can do that.

### A word about the language

I'm happy to change the language for deferred potentials in my lectures, but you've probably noticed I can't change the book.  So let me try to reduce the discomfort of the term you will find in the book, which is "retarded" rather than "deferred". "Retarded" literally means delayed.  The latin parts are "re" for back and "tard" for slow. (Like tardy). Actually "tardy" would be kind of fun thing to call it.  The potential is in fact "tardy" just like you are marked "tardy" in elementary school.  It's late - it takes some time to catch up.  

The term was originally adopted as a description of 
developmentally disabled 
people as a way to speak about them objectively and clinically.  That obviously
didn't last and it became pejorative. And I acknowledge that the first definition
in every dictionary is now pejorative.  However, if it helps, it came into use
to describe electrodynamics long before it started being used as a clinical medical
term. It became so widely adopted that now it pervades multiple fields who use it.

So I understand and appreciate your discomfort, but I wanted you to know its origin 
and its meaning when you encounter in our book and others.


### Last time we practiced using deferred potentials

$$
V(\vec{r}, t) = \frac{1}{4\pi\epsilon_0}\int\frac{\rho(\vec{r}^\prime, t_d)}{\mathscr{r}}d\tau^\prime
$$

$$
\vec{A}(\vec{r}, t) = \frac{\mu_0}{4\pi}\int\frac{\vec{J}(\vec{r}^\prime, t_d)}{\mathscr{r}}d\tau^\prime
$$

What does the deferred time correspond to?  

$$
t_d = t - \frac{\mathscr{r}}{c}
$$

Here are the equations for E and B that we are talking about today (not deriving,
just talking about.)  

$$
\vec{E}(\vec{r},t) = \frac{q}{4\pi \epsilon_0}\frac{\mathscr{r}}{(\vec{\mathscr{r}}\cdot\vec{u})^3}\left[(c^2 - v^2)\vec{u} + \mathscr{r}\times(\vec{u}\times\vec{a})\right]
$$

And you already know what B is going to be:

$$
\vec{B}(\vec{r},t) = \frac{1}{c}\hat{r} \times \vec{E}(\vec{r},t)
$$

Okay so let's go backwards. 

## How are these useful?

They tell you the electric and magnetic fields of a particle of
charge $$q$$ moving at velocity $$\vec{v}$$ and acceleration $$\vec{a}$$.
The $$\vec{u}$$ that's in them is not the velocity, but it's related
to the velocity.

$$
\vec{u}\equiv c\hat{\mathscr{r}} - \vec{v}
$$

So $$\vec{u}$$ depends not on the distance $$\mathscr{r}$$ between you
and the source, but the difference between the vector pointing from the
source to you (with magnitude equal to the speed of light) and the vector
velocity of the particle.  Both $$\mathscr{r}$$ and $$v$$ are evaluated
at the deferred time.

So what is the magnitude of $$u$$ if
* The particle is traveling straight toward you at a constant velocity?  
(Ans: the speed of light
minus the velocity of the particle.  So if the particle is traveling
at the speed of light $$u$$ is zero.) 
* The particle is not moving?  Then u is equal to the distance to the 
particle times the speed of light.


## Do they reduce to things that we already know?
The first term in E falls off as the inverse square of the distance. 

Question for you:  If velocity and acceleration are both zero, what do you
get? (It should be familiar to you.)

Ans:
$$
\vec{E}(\vec{r},t) = \frac{q}{4\pi \epsilon_0}\frac{q\mathscr{r}}{\mathscr{r}^2}
$$

## Where did they come from?

Right, well let's back up a little.

They come from the Leinard-Wiechert potentials.

Here are the Leinard-Wiechert potentials for a moving point charge.

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

Let's see where that interesting denominator in $$V$$ came from, because you
can see that that translated directly into the field of a moving
point charge.  Besides that interesting denominator, the equation (10.46) 
looks like the potential of the point charge at some interesting distance.
It's not just the distance at the deferred time.  

Griffiths here makes a nice argument about the volume of a train changing
if it's coming toward you as opposed to being at rest - because you'll 
observe the front of the train to be closer, because the light won't
have to travel as far.

We're using the train to look for justification of this formula, which
I will rewrite somewhat:

$$
V(\vec{r},t) = \frac{1}{4\pi \epsilon_0}\frac{q}{\mathscr{r}}
\frac{1}{1 - \frac{\hat{\mathscr{r}}\cdot\vec{v}}{c}}
$$

You may recognize that last factor from studies of special relativity.
It's geometry.  Again, General Relativity is all geometry and you are
accidentally doing GR now, because it's imbedded in Maxwell's equations.

Let's remind ourselves where it comes from. Consider a train coming toward 
you.  Light from the front will take a shorter time to get to you than light
from the back. So light from the back left sooner (a deferred time) when the
train was further away.  So the train will appear a bit longer than when it's
not moving.

How much longer?
If at rest, the train is a length $$L$$.  And when moving the train appears
a length $$L^\prime$$. The difference between those lengths, is the time
it took light to travel from the back to the front of the train ($$L^\prime/c$$), multiplied
by the speed of the train.


$$
(L^\prime - L)= L^\prime  \frac{v}{c}
$$

$$
L^\prime = \frac{L}{1 -  \frac{v}{c}}
$$

So the train appears longer by a factor of $$\frac{1}{1 -  \frac{v}{c}}$$
Once you allow for the train not to be coming straight toward you, that
v/c turns into a $$\hat{\mathscr{r}}\cdot\vec{v}/c$$ 

What does that have to do with our potential?  Well, you'll remember that
electromagnetism is formulated as current and charge density.  And the
fact that space gets dilated when something is moving relative to you
changes the density of the charge by that same amount.  So when calculating
the potential the density gets decreased by an amount

$$
\frac{1}{1 - \frac{\hat{\mathscr{r}}\cdot\vec{v}}{c}}
$$

That's the same as

$$
\frac{\mathscr{r}c}{\mathscr{r}c - \vec{\mathscr{r}}\cdot\vec{v}}
$$

This times $$\frac{q}{4\pi\epsilon_0\mathscr{r}}$$
is the Leinard-Wiechert potential. (Remember you have to evaluate
all the r's and v's at the deferred time.)


###  Calculating the deferred time for the particle. 
I'm not sure we need this piece, but I'm leaving it in here for reference.

Let's consider that the trajectory of out point charge is given by $$\vec{w(t)}$$.
In other words, the position of the charge at time $$t$$ is $$\vec{w}(t)$$.
We can use that to calculate the deferred time. The deferred time is a time that's
different from $$t$$ by how far the charge is away from us. (I'm assuming
we want to calculate the potential where I'm standing.) 
If I'm standing at $$\vec{r}$$ then that distance (a function of time) is:

$$
d(t) =? |\vec{r} - \vec{w}(t)|
$$

Not quite.  

I don't actually want the distance *now*, I want the distance between where
the charge was when the light that I'm now observing left it, and where I am now.
So I want the position at the deferred time.

$$
d(t) = |\vec{r} - \vec{w}(t_d)|
$$

And the deferred time is the current time $$t$$ minus the time it takes
light to travel that far.

$$
t_d = t -  \frac{1}{c}|\vec{r} - \vec{w}(t_d)|
$$

(Equivalent to Griffiths 10.44)
The second term on the right side is the time it takes for news to travel from the source to you.  Said another way, if you're receiving light at time $$t$$ from the source,
then it left the source a time $$\frac{1}{c}|\vec{r} - \vec{w}(t_d)|$$ ago. 


## What fancy things do they let us do?

They let us calculate the field from any arbitrary combination of charges.  What we'll do first is tackle dipole radiation, because that turns out to allow nice simplifications, and also turns out to be a good approximation to much of the radiation we observe.

That is what chapter 11 is about and then we're done!!

Two things to notice about E.  The first term (as you found) reduces to the field
of a point charge if v=0.  It's called the generalized Coulomb field and it falls
off like $$r^2$$.  The second term falls off slower, and is therefore more
important at large distances.  It's this term that is responsible for radiation,
as we will see in chapter 11.

