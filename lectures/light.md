---
layout: page
title:  "Light"
permalink: "/lectures/light"
---

#### Announcements:
* Please put your ID number of your homework.
* Please make your homework legible.  It requires a bit more effort now since 
scanning loses some information.  Thank you!!
* Solutions to exam is on Moodle.  I can't figure out a realistic way to return your
exams to you, but I'm happy to talk to you about it.  Sign up for one of my times and I can send you pictures of whatever you want.

#### To review from last time: 

To Ampere's Law we added Maxwell's correction

$$
\nabla \times \vec{B} = \mu_0 \vec{J} + \mu_0 \epsilon_0 \frac{\partial\vec{E}}{\partial t}
$$

It's really important because we can't have light without it, which is what we're
dealing with today.  It came about when we took the divergence of both
sides of Ampere's law and realized that the left side was always zero,
but the ride side was not.  (You'll recall I argued that I could make
a current density with a divergence by standing in one place and tossing
out protons in all directions.)

One thing we picked up was the continuity equation from chapter 5:

$$
\nabla \cdot \vec{J} = -\frac{\partial \rho}{\partial t} 
$$

which really just says that if I'm sitting there throwing out protons,
the charge density where I am better be decreasing. (So the minus sign
in the equation makes sense.)

#### Today:

We make light. Not of our situation.  We actually make light.

### The punchlines:
* If you take the curl of both side of each of Maxwell's curl equations, you
can decouple E and B from each other.  You get waves that travel at a velocity
$$v = \frac{1}{\sqrt{\epsilon_0 \mu_0}} = c$$.
* The wave equation is close to the Simple Harmonic Oscillator equation that we
spent most of PHY213 dealing with, but now it propogates in time.
* In media 
$$v = \frac{1}{\sqrt{\epsilon \mu}} = c$$.  So that's why (one reason at least) that
we needed to deal with E and B in media, because light not in a vacuum is
really important.  In particular the index of refraction is
$$
n = \frac{c}{v} = \frac{\sqrt{\epsilon\mu}}{\sqrt{\epsilon_0\mu_0}}
$$

Let's begin.  Your book begins by dealing with a wave on a string to show you that
this is a very general treatment of waves.  I've been looking forward to talking
about light for the whole semester so there's no way I'm going to talk about
waves on a string right now.

Let's take Faraday's Law:

$$
\nabla \times \vec{E} = -\frac{\partial\vec{B}}{\partial t}
$$

Take the curl of both sides:

$$
\nabla \times \nabla \times \vec{E} = \nabla \times \left(-\frac{\partial\vec{B}}{\partial t}\right)
$$

$$
\nabla (\nabla \cdot \vec{E}) - \nabla^2\vec{E} = -\frac{\partial}{\partial t} (\nabla \times \vec{B})
$$

$$\nabla \cdot \vec{E}$$ is zero as long as we're in free space (otherwise it's
$$\rho/\epsilon_0$$.)
And we can use Ampere's Law to replace $$\nabla \times \vec{B}$$..

$$
- \nabla^2\vec{E} = -\frac{\partial}{\partial t} \left(\mu_0\epsilon_0 \frac{\partial\vec{E}}{\partial t}\right)
$$

$$
\nabla^2\vec{E} =  \mu_0\epsilon_0 \frac{\partial^2\vec{E}}{\partial t^2}
$$

So we have a decoupled equation for E, i.e, it does not depend on B.

We can do the same thing for B and get...
$$
\nabla^2\vec{B} =  \mu_0\epsilon_0 \frac{\partial^2\vec{B}}{\partial t^2}
$$

This is the part where Griffiths notes that it's the same equation for E and 
B and they both are just waves traveling with velocity
$$v = \frac{1}{\sqrt{\epsilon_0 \mu_0}} $$.
so then he treats it very generally calling E and B "f" etc.  I encourage you
to read it, but we're going to go to dealing with E.

#### How can you tell that's a wave with velocity $$v$$?

Excellent question.  I don't think that's obvious at all.
Let's rewrite it with the $$v$$ in place and then we'll experiment with it.

$$
\nabla^2\vec{E} =  \frac{1}{v^2} \frac{\partial^2\vec{E}}{\partial t^2}
$$

First, what I would like you to do is see if you believe that the
following is a solution to this equation.  You're used to this "guess" a solution
thing from PHY213.  Try:

$$
\vec{E(x,t)} = E_0cos[k(x - vt) + \delta]\hat{y}
$$

which is also the same thing as

$$
\widetilde{E(x,t)} = \widetilde{E_0}e^{i[k(x - vt) + \delta]}\hat{y}
$$

where $$\vec{E} = Re[\widetilde{E}]$$.

You can use either one you want to prove to yourself it's a solution.

A more general solution is a superposition of any of these solutions, but
we won't really get to that until Wednesday when we talk about polarization.

I still haven't answered the question how do I know that's a wave
with velocity v. 

Consider a crest of the wave.  The cosine peaks when its argument is
zero.  Let's consider $$\delta =0$$ for now.  The cosine peaks when
$$k(x - vt)=0$$.  That's zero when $$x-vt = 0$$ which is when $$x=vt$$.
So the peak of this wave is at x coordinate $$vt$$.  So it's a wave traveling to
the right at velocity $$v$$.

There's another solution to the equation that looks like this:
$$
\vec{E(x,t)} = E_0cos[k(x + vt) + \delta]\hat{y}
$$

which is a wave traveling to the left at velocity $$v$$.  Both are solutions (and a more general solution will involve a superposition of both of them.)

What's this $$k$$ then???

Now let's consider a picture of the wave frozen in time.  Let's set $$t=0$$ and $$\delta=0$$.  Now we have..

$$
\vec{E(x,t=0)} = E_0cos[kx]\hat{y}
$$

That is a picture of a cosine that repeats itself when $$kx=2\pi$$.  So its
wavelength is $$x = 2\pi/k$$ or $$\lambda = 2\pi/k$$. 
or its wavenumber is $$k = 2\pi/\lambda$$.
$$k$$ has units of inverse length.

We need one more piece $$\omega$$:
Let's go back to the original wave...

$$
\vec{E(x,t)} = E_0cos[k(x - vt) + \delta]\hat{y}
$$

and rewrite it

$$
\vec{E(x,t)} = E_0cos[kx - kvt + \delta]\hat{y}
$$

Let's call $$\omega = kv$$ so now we have..

$$
\vec{E(x,t)} = E_0cos[kx - \omega t + \delta]\hat{y}
$$

$$\omega $$ has units of 1/time.  It's the angular frequency.  When $$\omega t = 2\pi$$ we've gone through a cycle of the wave.

Velocity is $$\omega/k$$ (the only thing that gets you the right units, length over time.

####The relationship between E and B

What do Maxwell's equations say about the relationship
between E and B?  For this wave to work it's got to satisfy all of Maxwell's
equations.   Let's use Faraday's law again.  First, let's write
our solution for E and B so we can stare at them:
(I got rid of the $$\delta$$'s for now.)

$$
\widetilde{E(x,t)} = \widetilde{E_0}e^{i(kx - \omega t) }\hat{y}
$$

$$
\widetilde{B(x,t)} = \widetilde{B_0}e^{i(kx - \omega t) }\hat{?}
$$

I don't know the direction of B yet, so it's a question mark.

Using Faraday's Law:

$$
\nabla \times \vec{E} = -\frac{\partial\vec{B}}{\partial t}
$$

what's the relationship between E and B?

Go!!

Answer:

The derivative of B with respect to time is a little easier so let's do
that first...

$$
\frac{\partial}{\partial t} \widetilde{B(x,t)} = -i\omega \widetilde{B_0}e^{i(kx - \omega t) }\hat{?}
$$

Now we need the curl of E.  We only have a y component to E, so

$$
\nabla \times \vec{E} = \frac{\partial E_y}{\partial x}\hat{z} -  \frac{\partial E_y}{\partial z}\hat{x}
$$

$$E_y$$ doesn't have any $$z$$ dependence so it's just the first term.

$$
\nabla \times \vec{E} = ik\widetilde{E_0}e^{i(kx - \omega t) }\hat{z}
$$

So now we equate the two:

$$
i\omega \widetilde{B_0}e^{i(kx - \omega t) }\hat{?} = ik\widetilde{E_0}e^{i(kx - \omega t) }\hat{z}
$$

So it looks like their real parts are related by...

$$
B_0 = \frac{k}{\omega} E_0 = \frac{1}{c} E_0 
$$

Their amplitudes are in the ratio of the speed of light!

and

$$
\hat{?} = \hat{z}
$$

In general that's

$$
\hat{?} = \hat{k} \times \hat{n}
$$

where $$\hat{k}$$ is the direction of propagation of the wave (x in this case)
and $$\hat{n}$$ is the polarization vector, which we define to be the direction
E is pointing, $$\hat{y}$$ in this case.


You can summarize all of the above relationship by saying

$$\widetilde{B_0}  = \frac{1}{c} (\hat{k} \times \widetilde{E_0})$$

in a vacuum.

#### Next

On Wednesday we'll deal with polarization and on Friday we'll deal with reflection
and transmission (which is basically matching boundary conditions.)

#### Review
* If you take the curl of both side of each of Maxwell's curl equations, you
can decouple E and B from each other.  You get waves that travel at a velocity
$$v = \frac{1}{\sqrt{\epsilon_0 \mu_0}} = c$$.
* The wave equation is close to the Simple Harmonic Oscillator equation that we
spent most of PHY213 dealing with, but now it propogates in time.
* $$
\vec{E(x,t)} = E_0cos[k(x - vt) + \delta]\hat{y}
$$ is a wave traveling to the right (toward positive x) with velocity $$v$$. 
* In order to satisfy the relationship between E and B in Maxwell's equations (and therefore for the wave to propagate) we need:
$$\widetilde{B_0}  = \frac{1}{c} (\hat{k} \times \widetilde{E_0})$$
