---
layout: page
title:  "Dipole Radiation"
permalink: "/lectures/dipole"
---

Last week was about deferred potentials.  Basically you need to
calculate the deferred potential in order to deal with time-dependent
charge distributions.

The goal of today is to see the equations for the field of a radiating dipole,
and to work some problems involving those fields.

On Monday I showed
you two not-very-rigorous derivativations
of the intensity from a radiating dipole.  
The basic idea is that you write down the deferred potential and then use

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

and then

$$
\vec{E} = - \nabla V - \frac{\partial \vec{A}}{\partial t}
$$

and

$$
\vec{B} = \nabla \times \vec{A}
$$


## Still last time:  Radiation

Punchline and main point: when charges accelerate their
fields transport energy irreversibly to infinity.  That transport
of energy to infinity is called radiation.

The power is given by integrating the intensity (given by the Poynting vector $$\vec{S}$$) 
over an area, the area over which you want to know the energy crossing per unit time.

We talked about how, for something to radiate to infinity, the energy crossing
successively larger spheres per unit time must be the same, so therefore the only
E field that can radiative is one that goes as $$1/r$$.

Looking at the equation for E-field that I'm about to write down, it's not all
the terms.  In fact it's only the time-dependent terms that have any hope of going
as $$1/r$$ because we know all the non-time dependent ones goes as $$1/r^2$$ or
faster (for a dipole for example.)  So electrodynamics really was leading up to here.

$$
P = \int \vec{S}\cdot d\vec{a} = \frac{1}{\mu_0}\int(\vec{E}\times\vec{B})\cdot d\vec{a}
$$

## Dipole radiation

We started with the formula for a dipole..

$$
V = \frac{1}{4\pi\epsilon_0} \frac{p \cos\theta}{r^2}
$$

and then we let the dipole actually oscillate in time.  

First we did it by dimensional analysis and then we did it by sort of
advanced handwaiving, and we got this:

$$
<\vec{S}> = \frac{\mu_0 p_0^2 \omega^4}{32\pi^2 c} \frac{\sin^2\theta}{r^2} \hat{r}
$$

The dependence on $$\theta$$ is really important.  You don't get
any radiation looking down on the dipole.

The dependence on $$\omega^4$$ is really important.  Power is the 4th power of frequency.
So if you make your signal generator go twice as fast you get 16 as much power.

The approximations we made (that you have to make in the rigorous derivation, too)
are (1) that the size of the dipole is much smaller than the distance you are away
from it ($$d<<r$$).  That's what let us take the $$\mathscr{r}$$ away and replace
it with $$r$$.  
(2) We have to assume that $$d<<\lambda$$.  When you're dealing with
$$\cos[\omega(t - \mathscr{r}/c)]$$ aka the cosine of the deferred time, the
geometry (shown on page 468) gets you things like 
$$\cos\left(\frac{\omega d}{2c}\cos\theta\right)$$,
and
$$\sin\left(\frac{\omega d}{2c}\cos\theta\right)$$,
which kinda stink unless you can say that $$\frac{\omega d}{2c}$$ is really small in
which case

$$\cos\left(\frac{\omega d}{2c}\cos\theta\right)\approx 1 $$

and

$$\sin\left(\frac{\omega d}{2c}\cos\theta\right)\approx \frac{\omega d}{2c}\cos\theta$$

(3) We also have to assume that we're farther away from the source
than one wavelength of light, so $$r>>\lambda$$.  That's what makes the Coulomb terms
unimportant. 

I've numbered the approximations above in the same way Griffiths numbers them on page 467-68.

That's really only 2 requirements.  $$d <<\lambda$$ and $$r>>\lambda$$.  The latter
is how you specificy the "radiation zone".  

Notice that there's a reason my thesis adviser the radio astronomer always talked about
dipole radiation with a paper clip, and that optical astronomers never talk
about paper clips. The idea was that you could make dipole
radiation by hooking a paper clip up to a signal generator - put in a sine wave
voltage like you do in 213.  For a paper clip (the dipole) to be smaller than 
a wavelength, the  wavelength has to be more than several centimeters.  
That's radio (meters) not optical (100s of nm).  So you can make radio dipole
radiation by setting your signal generator at 100's of MHz.

What will happen if you try to go faster than that?  Will you still get radiation?  What
does this approximation mean?  Yes, you will still get radiation.  Remember one of the
main takeaways of this chapter is that as long as you have a time dependent charge or current
you have radiation.  If you're making a dipole radiator but not following the rules
of $$r>>\lambda>>d$$ then the pattern just won't quite look like the one we derived
in class yesterday (the donut pattern.)

## Another comment about the radiation zone
I've always thought this was a little confusing - like somehow in the radiation zone the coulomb
term goes away .  It's not true of course.  The coulomb term drops off like $$1/r^2$$ so there
won't be a lot of force but it's there.  But as physicists it's your job to figure out what the dominant
effect is, and in the radiation zone it's the radiation.  So talking about the "radiation zone"
really is a comment on which term in the equation is dominant.

## What do the fields look like?  
We 'derived' the equation for power radiated, but what do the fields actually look like?

Once you make those approximations that I just talked about you get the following
for the scalar and vector potentials of a dipole:

$$
V(r, \theta, t) = \frac{p_0\omega}{4\pi\epsilon_0c} \frac{\cos\theta}{r}\sin[\omega(t - r/c)]
$$

$$
\vec{A}(r, \theta, t) = -\frac{\mu_0p_0\omega}{4\pi r} \sin[\omega(t - r/c)]
$$

It looks like the vector potential is missing its $$\theta$$ dependence, but remember it's
all in the $$\hat{z}$$.  $$\hat{z} = \cos\theta \hat{r} - \sin\theta\hat{\theta}$$.

Then we use

$$
\vec{E} = -\nabla V - \frac{\partial \vec{A}}{\partial t}
$$

and after we drop the terms proportional to $$1/r^2$$ by the third approximation we get

$$
\vec{E} = \frac{\mu_0 p_0 \omega^2}{4\pi} \frac{\sin\theta}{r} \cos[\omega(t - r/c)]\hat{\theta}
$$

And you can take $$\nabla \times \vec{A}$$ to get $$\vec{B}$$ and drop the terms
proportional to $$1/r^2$$ but you also know what it is
off the top of your head because this is EM radiation and you know the relationship of
B to E.

$$
\vec{B} = \nabla \times \vec{A} = \frac{\mu_0 p_0 \omega^2}{4\pi c} \frac{\sin\theta}{r} \cos[\omega(t - r/c)]\hat{\phi}
$$

And you can see from those two formula that it's easy to get the formula for
time-averaged intensity that we got last time:

$$
<\vec{S}> = \left< \frac{1}{\mu_0} (\vec{E} \times \vec{B})\right> =  \frac{\mu_0 p_0^2 \omega^4}{32 \pi^2 c} \frac{\sin^2\theta}{r^2} \hat{r} 
$$

Remember the 16 turned into a 32 by doing the time averaging over the $$\cos^2$$.

If you integrate this over the sphere you get the time-averaged total power radiated:

$$
<P> =  \frac{\mu_0 p_0^2 \omega^4}{12 \pi^2 c} 
$$

I'm not actually going to go through the derivative for magnetic dipole radiation
but it's remarkably similar.   You end up with:

$$
<P> =  \frac{\mu_0 m_0^2 \omega^4}{12 \pi^2 c^3} 
$$

where $$m_0$$ is the amplitude of the magnetic dipole moment oscillating at $$\omega$$ rather than the
amplitude of the electric dipole oscillation oscillating at $$\omega$$. 
Notice the big difference is the $$c^3$$ in the denominator rather than $$c$$ which accounts
for the difference in definition of electric dipole $$p_0 = qd$$ and magnetic dipole $$m_0 = IA$$
where $$A$$ is the area of the loop and $$I$$ is the current.  So magnetic dipole
moment has an extra factor of meters/sec in its units, so the equation for power
deals with that by putting an extra two factors of $$c$$ in its denominator.  The
equations for field from a dipole also have an extra factor of $$c$$ in the denominator.

Okay yay we know everything!  

## Wait, what do these waves actually look like?

They are monochromatic waves traveling in directions $$\vec{r}$$ and the electric field and magnetic
fields are perpendicular to each and in phase with each other.  What direction is it polarized?  In the $$\theta$$
direction... that's the polar angle.  So wherever you are, the E-field will be lined up with the direction of
the dipole. And in fact its amplitude will be proportional to the projection of the dipole onto a plane that's
perpendicular to the propagation direction.  So the amplitude will be proportional to how big the dipole looks to you.  Same with the the amplitude of the magnetic field, but it's direction will be orthogonal. Which direction?  B is
always in the direction of $$\hat{k} \times \hat{n}$$ so it's always in the $$\hat{\phi}$$ direction, which
is consistent with the equation above.

The amplitude is decreaseing like $$1/r$$ which is not actually a wave we've had before.  We've had plane waves whose
amplitude doesn't decrease with distance. This one does. It's a spherical wave rather than a plane wave. 


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

### Why is the sky blue?
The strong frequency dependence of the formula makes the sky blue. 

Let's back up.
This dipole radiation is a good model for absorption and emission of radiation from oscillating charges in atoms..
Just like an oscillating dipole will cause
radiation, radiation will cause a dipole to oscillate.    

So sunlight hitting atoms in the atmosphere makes atoms
oscillate and then they re-emit the radiation in the donut pattern.  That's the way scattering works.  The
blue light is higher frequency and therefore is more effective at this scattering.  That's why the sky
away from the sun looks blue.

### Sunlight is polarized.  Sunlight is also polarized because of this phenomenon. The oscillation of the electron
from the incident light is perpendicular to the direction of propagation of the incident light (because the E-field
is perpendicular to the direction of propagation.) But that means when you look at a particular part of the sky,
the electrons will all be oscillating in a particular plane.  So when that atom re-radiates its polarization
direction will be in that plane.     
