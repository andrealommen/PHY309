---
layout: page
title:  "Radiation"
permalink: "/lectures/radiation"
---

Last week was about deferred potentials.  Basically you need to
calculate the deferred potential in order to deal with time-dependent
charge distributions.

The goal of today is to show you two not-very-rigorous derivativations
of the intensity from a radiating dipole.  Griffiths does the
rigorous derivativation, but I want to show you the forest for
the trees.  After we talk about the forest today, hopefully
you'll have more appreciation for the trees when you read
section 11.1.


### Here's what the deferred potentials look like

$$
V(\vec{r}, t) = \frac{1}{4\pi\epsilon_0}\int\frac{\rho(\vec{r}^\prime, t_d)}{\mathscr{r}}d\tau^\prime
$$

$$
\vec{A}(\vec{r}, t) = \frac{\mu_0}{4\pi}\int\frac{\vec{J}(\vec{r}^\prime, t_d)}{\mathscr{r}}d\tau^\prime
$$

The deferred time corresponds to:

$$
t_d = t - \frac{\mathscr{r}}{c}
$$


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

Last class I spent awhile motivating that difference, i.e. motivating
why the different between c and v comes up in the equations.

We considered a moving train and I convinced you that the length
of the train in the moving frame was:

$$
L^\prime = \frac{L}{1 -  \frac{v}{c}}
$$

So the train appears longer by a factor of $$\frac{1}{1 -  \frac{v}{c}}$$
Once you allow for the train not to be coming straight toward you, that
v/c turns into a $$\hat{\mathscr{r}}\cdot\vec{v}/c$$ 

This translates into a decreased charge density (because of increased
volume) for charges moving relative to you.  And that's where
that difference in the denominator of V comes from.

## Radiation

Punchline and main point: when charges accelerate their
fields transport energy irreversibly to infinity.  That transport
of energy to infinity is called radiation.

We have studied power in a field.  The Poynting vector
is power per area.  So power is the Poynting vector
$$S$$ integrated over an area.  

$$
P = \int \vec{S}\cdot d\vec{a} = \frac{1}{\mu_0}\int(\vec{E}\times\vec{B})\cdot d\vec{a}
$$

If this radiation is going to be transported to infinity then we
need it to actually leave.  Let's think about it leaving some
area that we designate.  How much power exits some volume
bounded by a closed surface?
(I just made the previous integrals closed surface integrals.)

$$
P = \int \vec{S}\cdot d\vec{a} = \frac{1}{\mu_0}\int(\vec{E}\times\vec{B})\cdot d\vec{a}
$$

Well if we want this power to actually leave the sphere, and also to
go to infinity, then no matter what size sphere we choose, the power
leaving it should be the same. (Imagine a light bulb emitting 60 watts of
power.  There should be 60 watts of power measured at any distance as longas you integrate over the sphere. Otherwise energy is bunching up someplace.)

So then the part of this pointing vector that correponds to radiation
is the part where $$E\times B$$ decreases at $$1/r^2$$.   Otherwise
we'll measure different amounts of power at different radii.

That means that we only want the part of the field that drops
off as $$1/r$$.  That's not the coulomb field.  The coulomb field
of a point charge drops off as $$1/r^2$$.  So that's not transporting
energy.  

Let's look at two equations we didn't talk about last time. They
are called Jefimenko's equations and they result directly from
the deferred potential above.  Let's just write down E.

$$
E(\vec{r}, t) = \frac{1}{4\pi\epsilon_0}\int\left[\frac{\rho(\vec{r}^\prime, t_d)}{\mathscr{r}^2}\hat{\mathscr{r}} +\frac{\dot\rho(\vec{r}^\prime, t_d)}{c\mathscr{r}}\hat{\mathscr{r}} - \frac{\dot{\vec{J}}(\vec{r}^\prime, t_d)}{c^2\mathscr{r}}\right]d\tau^\prime
$$

That first term is the Coulumb term (and the whole thing reduces to the
columb field if nothing has any time dependence.) And the second two
terms are the ones that decrease with r.  The first and second terms
came from using the chain rule in differentiation $$\rho/\mathscr{r}$$.
The third term came from the new thing we added to the field - we
don't just need $$\nabla V$$ anymore.  Now we also need $$\frac{\partial \vec{A}}{\partial t}$$.

## Dipole radiation

So it turns out that calculating the radiation from an oscillating
dipole is pretty easy.   I want you to guess what the formula is.
Just using dimensional analysis (not using Jefimenko's formulae).

You know the potential of a dipole:
(We're really starting to pull a lot of things together now.)

$$
V = \frac{1}{4\pi\epsilon_0)} \frac{p \cos\theta}{r^2}
$$

That's for a dipole in the z direction, with $$\theta$$ being the 
polar coordinate.

Come up with a formula for intensity (power per area), that includes
$$p, \omega, \epsilon_0, \mu_0, c$$ and $$r$$ where $$\omega$$
is the frequency at which the dipole is oscillating.  You know these things:

* The poential of a dipole (above).
* E is the spatial derivative of V.
* B is E/c
* Intensity is S given by $$\frac{1}{\mu_0}E\times B$$.
* Intensity must decrease by $$1/r^2$$.

Ans: 
I got that the units of $$<S>$$ which I will designate $$[S]$$
must be

$$
[S] = \left[\frac{1}{\mu_0}\right][E][B] = \left[\frac{1}{\mu_0\epsilon_0^2 c}\frac{p^2}{r^6}\right]
$$

And then we were told it has to go like $$1/r^2$$ so I need to
convert $$r^4$$ into c's and $$\omega's$$.  So then I get

$$
<S> \propto  \frac{\mu_0}{c}\frac{p_0^2\omega^4}{r^2}
$$

That actually is the formula down to a factor of $$32\pi^2$$ which
admittedly is pretty big.  But that's all the dependencies.
I wrote the dipole moment $$p$$ as $$p_0$$ to indicate that $$p_0$$
is the amplitude of the oscillating dipole.

## More of a derivation, but still pretty cavalier

Imagine that we have two small spheres connected by a wire,
and q(t) is the charge on the top sphere. Here's how we
write down the charge.

$$
q(t) = q_0 \cos{\omega t}
$$

We know that the radiation depends on dA/dt (among other things)
 from staring at Jefimenko's
equation, so let's rely on A to estimate this.  

A involves J, so let's calculate I.

$$
I(t) = \frac{dq}{dt}=  -q_0 \omega \sin{\omega t}
$$

To get A we normally integrate J over a volume, but I is all happening
in one dimension, so integrating J over a volume is the same thing
as integrating I over a length. (Remember J is I per area.)

The integral would look something like this:
$$
\vec{A} = \frac{\mu_0}{4\pi} \int\frac{\vec{J}(\vec{\mathscr{r}})}{\mathscr{r}}d\tau^\prime
$$

$$
\vec{A} = \frac{\mu_0}{4\pi} \int\frac{\vec{I}}{r}dz^\prime
$$

We'll say our dipole is small enough that $$\mathscr{r}$$ is
basically just $$r$$.  Therefore the integral doesn't depend upon
it.  Formally we're saying the linear extent of the dipole
is small compared to the distance we are away.  So then..

$$
\vec{A} = \frac{\mu_0}{4\pi} \frac{I d}{r}
$$

where I integrated dz over the length of the dipole, d (the separation
of the charges).

So now
$$
A = -\frac{\mu_0}{4\pi} \frac{q_0d\omega \sin{\omega t}}{r}
$$

$$
\frac{\partial {A}}{\partial t} = -\frac{\mu_0}{4\pi} \frac{q_0d\omega^2 \sin{\omega t}}{r}
$$

Oh yay!  We've still got 1/r! That's what we wanted.
And now we've got everything we need to calculate $$S$$.

$$
S = |\frac{1}{\mu_0}(\vec{E}\times \vec{B})| = \frac{1}{\mu_0 c} E^2
$$

$$
S = \frac{\mu_0 p_0^2 \omega^4}{16\pi^2 c r^2} \sin^2\omega t
$$

where I let $$p_0 = qd$$.

The only other piece we need is that time-averaged amplitude of
a sine-wave squared is 1/2  the amplitude of it.  So the 
formula for the time-averaged intensity of dipole radiation is

$$
<\vec{S}> = \frac{\mu_0 p_0^2 \omega^4}{32\pi^2 c} \frac{\sin^2\theta}{r^2} \hat{r}
$$

The dependence on $$\theta$$ is really important.  You don't get
any radiation looking down on the dipole.

The $$\sin \theta$$ comes from  decomposing $$\hat{z}$$ the
direction of the dipole, into $$\hat{theta}$$ and $$\hat{r}$$.  The $$\cos\theta \hat{r}$$
term goes away because it ends up cancelling with the $$\theta$$
term in the scalar potential.


