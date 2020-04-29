---
layout: page
title:  "Radiation from a Point Charge"
permalink: "/lectures/point"
---

The goal of today is that you understand what the radiation from a point charge
looks like.  We need to derive the Larmor Formula for radiation from a point charge.
Here's the punch line.  The power radiated from a point charge is this:

$$
P = \frac{\mu_0 q^2 a^2}{6\pi c}
$$

where $$a$$ is the magnitude of the acceleration of the charge.  The angular
structure of the radiation looks again like a donut, with no radiation along
the direction of the acceleration. (See Griffiths figure on page 484, Figure 11.11)

Along the way I want to show you that you get no radiation from constant velocity.
You do get field from constant velocity, and it looks like a pancake because of the 
deferred potential, but you don't get radiation.

Last time:
We started with the formula for a dipole..

$$
V = \frac{1}{4\pi\epsilon_0} \frac{p \cos\theta}{r^2}
$$

and then we let the dipole actually oscillate in time.  

We talked about the requirements for the dipole approximation to be a good
approximation to the radiation you would measure from a dipole.  They are
that $$d <<\lambda$$ and $$r>>\lambda$$, where $$d$$ is the size of the dipole
and $$\lambda$$ is the wavelength of the radiation.  The latter
is how you specificy the "radiation zone".  

Similar criteria are true for magnetic dipoles but you replace the restrictions
on $$d$$ above with restrictions on $$b$$ the radius of the current loop that
makes up the magnetic dipole, $$m_0$$.

We thought about these restrictions by thinking of attaching a paper clip to
a signal generator to create a dipole antenna.   If we want the dipole
approximation to be valid we need the wavelength of the radiation to be
larger than the dipole, which means we need radio wavelengths near meters.  
The pattern of the radiation would be in a donut, with no radiation along
the axis of the dipole.

We looked at this problem of the radio tower, which I would like to take five minutes
to look at since you worked on this. 


### Problem 11.23 
A radio tower rises to height h above flat horizontal ground. At  the top is a magnetic dipole antenna, of radius b, with its axis vertical. FM station  KRUD broadcasts from this antenna at (angular) frequency ω, with a total radiated  power P (that’s averaged, of course, over a full cycle). Neighbors have complained  about problems they attribute to excessive radiation from the tower—interference  with their stereo systems, mechanical garage doors opening and closing mysteriously, and a variety of suspicious medical problems. But the city engineer who  measured the radiation level at the base of the tower found it to be well below the  accepted standard. You have been hired by the Neighborhood Association to assess  the engineer’s report.  

(a) In terms of the variables given (not all of which may be relevant), find the  formula for the intensity of the radiation at ground level, a distance R from the  base of the tower. You may assume that b<< c/ω << h. [Note: We are interested  only in the magnitude of the radiation, not in its direction—when measurements  are taken, the detector will be aimed directly at the antenna.]  

(b) How far from the base of the tower should the engineer have made the measurement? What is the formula for the intensity at this location?  

(c) KRUD’s actual power output is 35 kilowatts, its frequency is 90 MHz, the  antenna’s radius is 6 cm, and the height of the tower is 200 m. The city’s radioemission limit is 200 microwatts/cm2. Is KRUD in compliance? 

Answers:

(a) Use our equation for intensity from an oscillating magnetic dipole. You
can equally well use the equations from an electric dipole and you'd get the same thing. The
important thing is that the radiation intensity is proportional to $$\sin\theta/r^2$$.
The magnitude of the time-averaged intensity is related to the power
(for either a magnetic or electric dipole) by:

$$
|<S>| = \left(\frac{3P}{8\pi}\right) \frac{\sin^2\theta}{r^2}
$$

And then figuring out what $$\theta$$ is trigonometry problem.  When the engineer is
$$R$$ away from the base, they're a distance $$r = \sqrt{R^2 + h^2}$$ away from the dipole.

$$
\sin\theta = \frac{R}{\sqrt{R^2 + h^2}}
$$

So then

$$
I(R) = |<S>|  = \left(\frac{3P}{8\pi}\right) \frac{R^2}{\left(R^2 + h^2\right)^2}
$$

(b) The intensity directly below the antenna (R=0) would be zero.  The engineer could've measured
it in a number of places as long as they knew how the intensity would go as a function of
$$\theta$$.  The official answer is that you find the location of maximum intensity,
where $$\frac{dI}{dR}$$ is zero, which is where $$R=h$$. (That assumes the engineer measured
it from the ground.  I say, get them up on a ladder at a height equal to the tower height
and measure it there.)

(c) Assuming the city's radioemission limit is based on ground measurements, you would actually
need the 'official' answer from above, and know that the maximum radiation on the ground
happens where $$R=h$$. Then you can put in:

$$
I_{max} = \left(\frac{3P}{8\pi}\right) \frac{R^2}{\left(R^2 + h^2\right)^2}
= \left(\frac{3P}{8\pi}\right) \frac{h^2}{\left(h^2 + h^2\right)^2}=
\frac{3(35\times10^3 {\rm Watts})}{32\pi(200 m)^2} = 0.026 W/m^2 = 2.6 \mu W/cm^2$$. 

So KRUD
is in compliance.

## A good emitter is a good receiver

Something I didn't say last time is that an antenna that emits a particular kind of
radiation is also good at receiving that same radiation.  So a paper clip is a good
radio receiver, but it would only detect polarization along itself.  So to detect
any radiation you need a second paper clip oriented perpendicularly.


## Today - radiation from a point charge

This has some similarities to radiation from a dipole.  I'd say you'll use dipole
radiation more often in your life (because for example, it's how radio stations work) but
in some of the more exciting physics applications, like all of the universe's great
accelerators (black holes for example) you'll need to take into account the radiation
from a point charge that's being accelerated in some field.

The scheme is really the same - start with the deferred potentials and take the derivative
to get the field, drop anything that drops off faster than $$1/r$$.

The first difference is that we've already done some of the work for a point charge, by way
of the Leinard-Wiechert potentials, so we don't have to start with the most generalized
form of the deferred potentials.  

In Chapter 10 [in the lecture on Leinard-Wiechert Potentials](PHY309/lectures/leinard) we talked
about the formula for the electric field of a point charge:

$$
\vec{E}(\vec{r},t) = \frac{q}{4\pi \epsilon_0}\frac{\mathscr{r}}{(\vec{\mathscr{r}}\cdot\vec{u})^3}\left[(c^2 - v^2)\vec{u} + \vec{\mathscr{r}}\times(\vec{u}\times\vec{a})\right]
$$

(Reminder: $$\vec{u}\equiv c\hat{\mathscr{r}} - \vec{v}$$)
(I'm not going to write B, because we're not going to need it.)

Again, this came from the Leinard-Wiechert potentials which are the general potentials of
a point charge, and used $$\vec{E} = -\nabla V - \frac{\partial E}{\partial t}$$ to get E.


So where is the radiation going to come from?  

So that first term is going as 1/r^2.  And the second term is going as 1/r.  

So, yes, the radiation will come from the second term.  So if there's no acceleration
there's no radiation.  That's punchline number one. Now we need the pancake punchline.

We need to tackle the vectors here to get that.  So let's just keep the radiation
term from that equation above:

$$
\vec{E}_{rad} = \frac{q}{4\pi \epsilon_0}\frac{\mathscr{r}}{(\vec{\mathscr{r}}\cdot\vec{u})^3}\left[\vec{\mathscr{r}}\times(\vec{u}\times\vec{a})\right]
$$

and

$$
\vec{B}_{rad}(\vec{r},t) = \frac{1}{c}\hat{\mathscr{r}}\times \vec{E}_{rad}
$$

and 

$$
vec{S}_{rad} = \frac{1}{\mu_0}(\vec{E} \times \vec{B}) = \frac{1}{\mu_0 c} (E^2\hat{r})
$$

We need an easier version of E to put into that equation.  Let's work on E.

Let's get rid of our $$\vec{u}$$ by saying that we're instanteously at zero velocity.
So now $$\vec{u}$$ can be relaced by $$c\hat{r}$$ and we have

$$
\vec{E}_{rad} = \frac{q}{4\pi \epsilon_0c^2\mathscr{r}}\left[\hat{\mathscr{r}}\times(\hat{\mathscr{r}}\times\vec{a})\right]
$$

(Use the triple product rule on page 8:  $$\vec{A} \times \vec{B} \times \vec{C} = \vec{B}(\vec{A}\cdot\vec{C}) - \vec{C}(\vec{A}\cdot\vec{B})$$)  You can see our donut already!!  It's encoded
in the $$\hat{r}\cdot\vec{a}$$.  That makes it look like it's going to be proportional
to cosine $$\theta$$ which it's not....so keep watching...

$$
\vec{E}_{rad} = \frac{\mu_0 q}{4\pi\mathscr{r}}\left[(\hat{\mathscr{r}}\cdot \vec{a}) \hat{\mathscr{r}}-\vec{a})\right]
$$

That is the expression we put into $$S_{rad}$$

$$
\vec{S}_{rad} = \frac{1}{\mu_0 c} \left(\frac{\mu_0 q}{4\pi\mathscr{r}}
\right)^2\left[a^2 -  (\hat{\mathscr{r}}\cdot\vec{a})^2\right]\hat{\mathscr{r}}
= \frac{\mu_0q^2 a^2}{16\pi^2 c}\left(\frac{\sin^2\theta}{\mathscr{r}^2}\right)\hat{\mathscr{r}}
$$

where $$\theta$$ is the angle between $$\hat{\mathscr{r}}$$ and $$\vec{a}$$ (so it's the
angle between your line of site to the particle and the acceleration of the particle). So
there's the donut (punchline #2).  If the  particle is coming toward you, you'll see nothing,
because that angle is zero.

That $$\left[a^2 -  (\hat{\mathscr{r}}\cdot\vec{a})^2\right]$$ isn't totally obvious.  If you
square the expression in brackets above it, (using FOIL for example), the F and the OI terms
end up combining to give you that last term $$-(\hat{\mathscr{r}}\cdot\vec{a})^2$$.  And that's
there the $$\sin^2\theta$$ comes from, i.e.$$(1 - \cos^2\theta)$$.  

We just need one more punchline, which is the Larmor formula.  To get the total
power radiated over a sphere, we integrate $$\vec{S}$$ over a sphere to get:

$$
P = \frac{\mu_0 q^2 a^2}{6\pi c}
$$

So this finally, is the total power radiated from a particle of charge q with an acceleration
of a and zero velocity.

As long v << c this is good approximation to the total power even with some velocity.

The velocity dependence looks like this:


$$
P = \frac{\mu_0 q^2 \gamma^6}{6\pi c}\left(a^2 - \Bigg|\frac{\vec{v}\times\vec{a}}{c}\Bigg|^2\right)
$$

where $$\gamma = \frac{1}{\sqrt{1 - (v/c)^2}}$$

Notice that the factor of gamma means that the power increases enormously as the velocity 
approaches the speed of light.

Once again you'll notice that relativity is encoded in electrodynamics.
