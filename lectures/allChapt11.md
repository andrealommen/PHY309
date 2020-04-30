---
layout: page
title:  "Andrea's Crash Course in Chapter 11"
permalink: "/lectures/AllChapt11"
---

Chapter 11 is radiation.  We started talking about radiation in Chapter 10 when we noticed that the field of a point charge

$$
\vec{E}(\vec{r},t) = \frac{q}{4\pi \epsilon_0}\frac{\mathscr{r}}{(\vec{\mathscr{r}}\cdot\vec{u})^3}\left[(c^2 - v^2)\vec{u} + \mathscr{r}\times(\vec{u}\times\vec{a})\right]
$$

has a term that drops off like $$1/\mathscr{r}$$ rather than a $$1/\mathscr{r}^2$$.  That's the term that can give us radiation to infinity.  In chapter 10,
however, we were more concerned with the ramifications of the deferred
potential than we were with radiation.

In Chapter 11, by contrast, we use many of the equations from
Chapter 10, but we throw away all the terms that don't contribute
to the radiative energy.

Every E&M book starts with dipole radiation.  A dipole antenna is the
simplest to make - you attach a paper clip to a signal generator and bam, you've
got a radiating dipole.

## Dipole radiation

Starting with the voltage of a simple static dipole


$$
V = \frac{1}{4\pi\epsilon_0)} \frac{p \cos\theta}{r^2}
$$

I made you guess
what the intensity from a dipole radiator was.  You humored me and got all
the factors of $$\omega$$ (the frequency of the dipole oscillation) and $$c$$ and $$p_0$$ (the amplitude of the
dipole oscillation) and $$r$$ the distance you are from the dipole. Here's
the actual formula:

$$
<\vec{S}> = \frac{\mu_0 p_0^2 \omega^4}{32\pi^2 c} \frac{\sin^2\theta}{r^2} \hat{r}
$$

The dependence on $$\theta$$ is really important.  You don't get
any radiation looking down on the dipole along its axis.
The dependence on $$\omega^4$$ is really important.  Intensity is the 4th power of frequency.
So if you make your signal generator go twice as fast you get 16 as much intensity.

The approximations we made 
are (1) that the size of the dipole is much smaller than the distance you are away
from it ($$d<<r$$).  
(2) We have to assume that $$d<<\lambda$$.  
(3) We also have to assume that we're farther away from the source
than one wavelength of light, so $$r>>\lambda$$.  That's what makes the Coulomb terms (the non-radiative terms)
unimportant.  This last requirement is called the "radiation zone" and all it
means is that the radiation term is more important that the coulomb term. 

The fields look like this:

$$
\vec{E} = \frac{\mu_0 p_0 \omega^2}{4\pi} \frac{\sin\theta}{r} \cos[\omega(t - r/c)]\hat{\theta}
$$

$$
\vec{B} = \nabla \times \vec{A} = \frac{\mu_0 p_0 \omega^2}{4\pi c} \frac{\sin\theta}{r} \cos[\omega(t - r/c)]\hat{\phi}
$$

If you integrate intensity over the sphere you get the time-averaged total power radiated:

$$
<P> =  \frac{\mu_0 p_0^2 \omega^4}{12 \pi^2 c} 
$$

For magnetic dipoles it's remarkably similar:

$$
<P> =  \frac{\mu_0 m_0^2 \omega^4}{12 \pi^2 c^3} 
$$

where $$m_0$$ is the amplitude of the magnetic dipole moment oscillating at $$\omega$$ rather than the
amplitude of the electric dipole oscillation oscillating at $$\omega$$. 

The important thing about the polarization of the waves is that no matter
where you're looking, the polarization (the e-field) will be in line with the
projection of the axis of the dipole.  And the amplitude of the radiation
is proportional to the projection of that dipole onto a plane that's perpendicular to the propagation direction.

## Radiation from a point charge

Radiation from a point charge is less prevalent in common applications, but very common in astrophysics. Also, if you know the radiation from a point charge, you can integrate any distribution of charges to get the radiation.

Here's the total power:

$$
P = \frac{\mu_0 q^2 a^2}{6\pi c}
$$

where $$a$$ is the magnitude of the acceleration of the charge.  The angular
structure of the radiation looks again like a donut, with no radiation along
the direction of the acceleration. (See Griffiths figure on page 484, Figure 11.11)

Here's what the formula for intensity as a function of angle looks like:

$$
\vec{S}_{rad} = \frac{1}{\mu_0 c} \left(\frac{\mu_0 q}{4\pi\mathscr{r}}
\right)^2\left[a^2 -  (\hat{\mathscr{r}}\cdot\vec{a})^2\right]\hat{\mathscr{r}}
= \frac{\mu_0q^2 a^2}{16\pi^2 c}\left(\frac{\sin^2\theta}{\mathscr{r}^2}\right)\hat{\mathscr{r}}
$$

where $$\theta$$ is the angle between $$\hat{\mathscr{r}}$$ and $$\vec{a}$$ (so it's the
angle between your line of site to the particle and the acceleration of the particle). So
there's the donut (punchline #2).  If the  particle is coming toward you, you'll see nothing,
because that angle is zero.

If you don't assume velocity is zero, then you get a more interesting formula for power.

$$
P = \frac{\mu_0 q^2 \gamma^6}{6\pi c}\left(a^2 - \Bigg|\frac{\vec{v}\times\vec{a}}{c}\Bigg|^2\right)
$$

where $$\gamma = \frac{1}{\sqrt{1 - (v/c)^2}}$$

Notice that the factor of gamma means that the power increases enormously as the velocity 
approaches the speed of light.
