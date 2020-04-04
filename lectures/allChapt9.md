---
layout: page
title:  "Andrea's Crash Course in Chapter 9"
permalink: "/lectures/allChapt9"
---

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
* The most general way of writing the solutions to the wave equations for 
arbitrary propagation and polarization is (it's really important that you understand (a) why the
first equation below is a wave traveling in the $$\vec{k}$$ direction with frequency $$\omega$$ and
that you understand the relationship between E and B below.)

$$
\widetilde{E(\vec{r},t)} = \widetilde{E_0}e^{i(\vec{k}\cdot\vec{r} - \omega t) ]}\hat{n}
$$

$$
\widetilde{B(\vec{r},t)} = \frac{1}{c} \widetilde{E_0}e^{i(\vec{k}\cdot\vec{r} - \omega t) ]}(\hat{k} \times \hat{n}) = \frac{1}{c} \hat{k} \times \vec{E}
$$

where $$\vec{n}$$ is the polarization, the direction of the E-field and $$\vec{k}$$ is the direction of propagation.
* The polarization vector points where E points.  If it's linearly polarized it stays in a plane.  The combination
of two linearly polarized waves with a phase shift between them gets you a circularly polarized wave.

* In a linear medium, you end up with exactly the same wave equations you had before, but with a different
velocity $$
v = \frac{1}{\sqrt{\mu\epsilon}}
$$
* In a conductor you end up with an attenuated solution:
$$
\widetilde{E(x,t)} = \vec{\widetilde{E_0}}e^{-\kappa z}e^{i[kz - \omega t) ]}
$$
and the current acts like a damping agent.  B lags E in phase.


$$
\tilde{E}_{0,R} = \frac{1-\beta}{1+\beta}\tilde{E}_{0,I}
$$

where $$\tilde{E}_{0,R}$$ is the reflected amplitude
and $$\tilde{E}_{0,I}$$ is the incident amplitude.
The $$0$$ refers to the fact that this is a scalar amplitude.

and 
$$
\beta \equiv \frac{\mu_1 v_1}{\mu_2 v_2}
$$

There's a similar relationship between transmitted and reflected
although the 1-beta turns into a 2.

$$
\tilde{E}_{0,T} = \frac{2}{1+\beta}\tilde{E}_{0,I}
$$

In a conducting media it's the same formula for the relationship but
$$\beta$$ can be complex and is somewhat different.

$$
\tilde\beta \equiv \frac{\mu_1 v_1}{\mu_2 \omega}\tilde{k}_2
$$

You can already see that if you're in a dielectric medium, $$v_2$$ is
$$\omega/k_2$$ and you get the same thing back again.

* If $$v_2 > v_1$$ then the reflected wave remains upright.
* If $$v_1 > v_2$$ then the reflected wave is inverted.

All of these conditions come from Maxwell's equations. The relationship between E and B comes from
Ampere's or Faraday's law (you get the same answer for either.) And the equation for $$\beta$$ comes
from the boundary conditions - the same boundary conditions we dealt with in earlier chapters for
solving Poisson's equation.

**Maxwell's equations in Media:**

Gauss' Law

$$
\nabla \cdot \vec{D} = \rho_f
$$

(no name...no magnetic monopoles?)

$$
\nabla \cdot \vec{B} = 0
$$

Faraday's Law

$$
\nabla \times \vec{E} = -\frac{\partial\vec{B}}{\partial t}
$$

Ampere's Law

$$
\nabla \times \vec{H} = \vec{J}_f + \frac{\partial \vec{D}}{\partial t}
$$

If the medium is linear, then 

$$
\vec{D} = \epsilon \vec{E}
$$

and

$$
\vec{H} = \frac{1}{\mu} \vec{B}
$$

#### Each of Maxwell's equations corresponds to a particular boundary condition.

The boundary conditions we have in the order of how we usually
write Maxwell's equations are:

$$
\epsilon_1E_1^\perp = \epsilon_2E_2^\perp   
$$

$$
B_1^\perp = B_2^\perp
$$

$$
\vec{E}_1^\| = \vec{E}_2^\| 
$$

$$
\frac{1}{\mu_1}\vec{B}_1^\| =  \frac{1}{\mu_2}\vec{B}_2^\|   
$$

#### The procedure for finding out what happens as waves are incident on boundaries (i.e. the
procedure for deriving the equations for $$\beta$$ above)

Using the relation between E and B at the top of this page, you can write down an expression
for the incident, reflected, and transmitted waves.  You'll have 3 unknown complex amplitudes: 
$$\tilde{E}_{0,I}$$,
$$\tilde{E}_{0,T}$$, and 
$$\tilde{E}_{0,R}$$.  In a real problem you would probably know the incident amplitude, so you can
count that as two unknowns complex amplitudes.
A complex number is a real amplitude and a phase, so each of those complex amplitudes is two numbers.
So you really have 4 unknowns. You also have 4 boundary conditions.  So you have 4 equations and 4
unknowns. And you can solve for both the transmitted and reflected amplitudes: 
$$\tilde{E}_{0,T}$$, and 
$$\tilde{E}_{0,R}$$.  

Again, that solution is:


$$
\tilde{E}_{0,R} = \frac{1-\beta}{1+\beta}\tilde{E}_{0,I}
$$

$$
\tilde{E}_{0,T} = \frac{2}{1+\beta}\tilde{E}_{0,I}
$$

$$
\beta \equiv \frac{\mu_1 v_1}{\mu_2 \omega}\tilde{k}_2 
$$

The following formula for k is the most general one that includes a conductor
(with conductivity $$\sigma$$.)
If you don't have a conductor then the second term is just 0.

$$
\tilde{k}^2 = \mu\epsilon\omega^2 + i\mu\sigma\omega
$$


Some things to notice about the solution:

If $$v_2 = v_1$$ (which means you don't really have an interface),
then there's no reflection. If you get really high emissivity $$\epsilon$$
then $$v_2$$ is really small and you get total reflection (like a mirror). 
Really high emissivity is like conductivity, so conductors are usually
good mirrors (like a spoon for example.)

There are a great many things you can figure out about the waves without really
matching the boundary conditions, but just by noticing what the form
of the boundary conditions looks like in all cases, i.e.

$$
(....)e^{i(\vec{k}_I\cdot\vec{r}-\omega t)}
+
(....)e^{i(\vec{k}_R\cdot\vec{r}-\omega t)}
=
(....)e^{i(\vec{k}_T\cdot\vec{r}-\omega t)}
$$

From these we figured out Snell's law:

$$
k_{I}\sin\theta_I 
=
k_{R} \sin\theta_R
=
k_{T} \sin\theta_T
$$

and the first law of geometrical optics, which I like saying as "You can
draw all the k-vectors and the boundary in one 2-dimensional sheet of paper."

So the form of the boundary conditions gets you the relationships betwen the k's.

To get the amplitudes of the reflected and transmitted waves you need to put in the specific
boundary conditions.  To do this you need to do two separate problems: the polarization in the plane
of incidence, and the polarization perpendicular to the plane of incidence.

#### For polarization in the plane of incidence
From

$$
\tilde{E}_{0R} = \left(\frac{\alpha-\beta}{\alpha + \beta}\right)\tilde{E}_{0I}
$$

$$
\tilde{E}_{0T} = \left(\frac{2}{\alpha + \beta}\right)\tilde{E}_{0I}
$$

where
$$\alpha =\frac{\sqrt{1 - \sin^2\theta_T}}{\cos\theta_I} = \frac{\sqrt{1 - [(n_1/n_2)\sin\theta_I]^2}}{\cos\theta_I}$$
and as before
$$\beta = \frac{\mu_1n_2}{\mu_2n_1}$$

Those are known as Fresnel's equations for the case of polarization in
the plane of incidence.  They have interesting consequences.  One interesting consequence
is that there's an incident angle (Brewster's angle) at which 
there is no reflected wave (where $$\alpha = \beta$$).
This phenomenon makes polarized sunglasses reduce reflections off the road.  The transmitted
polarization has to be vertical, so that it permits reflections that are in the plane
of incidence, but reduced by Brewster's angle.   

There is no Brewster's angle for incident light polarized perpendicular to the plane
of incidence.  You'll be solving that case for your homework.  Here are the answers:
(I have assumed $$\mu_1 = \mu_2 = \mu_0$$)


$$
\tilde{E}_{0R} = \frac{\cos\theta - \sqrt{n^2 - sin^2\theta}}{\cos\theta + \sqrt{n^2 - sin^2\theta}}\tilde{E}_{0I}
$$

$$
\frac{\tilde{E}_{0T}}{\tilde{E}_{0I}} = 1 + \frac{\tilde{E}_{0R}}{\tilde{E}_{0I}}
$$

You'll see when you sketch them that you can't get the reflected amplitude to go to zero, as
advertised.

