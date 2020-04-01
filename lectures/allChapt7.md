---
layout: page
title:  "Andrea's Crash Course in Chapter 7"
permalink: "/lectures/allChapt7"
---

Chapter 7 is where we started to add dynamics - things changing in time.

## Electromotive Force and Induction

Ohm's 'law' 

$$
\vec{J} = \sigma \vec{E}
$$

A more familiar version of the law is:

$$
V = IR
$$

Faraday's law once you add the term with B changing in time:

$$
\nabla \times \vec{E} = - \frac{\partial \vec{B}}{\partial t}
$$

We argued that if these are the quantities at hand...

* $$\vec{J}$$: current density
* n: the number of molecules per volume
* q: the charge on one electron
* f: the number of free electrons per molecule
* $$\lambda$$: the distance between collisions (would you got faster or slower in your car if there were more space between stoplights?)
* m: the mass of an electron
* $$\vec{E}$$: the electric field
* $$v_{thermal}$$: the thermal velocity of the electrons (the random velocity of the electrons, NOT the velocity due to the electric field)

then the expression for the current density should look something like this:

$$
\vec{J} = nfq\vec{v}_{ave} = \left(\frac{nf\lambda q^2}{2m_e v_{thermal}}\right) \vec{E}
$$

Neither I nor Griffiths claim this is the accurate formula for
conductivity but it shows you two important things:
* The current density is proportional to the electric field, so it
shows you how an "Ohmic" situation can arise.
* It correctly predicts that conductivity is proportional to
the charge density.
* It correctly predicts that conductivity increases with decreasing
temperature.

#### Electromotive force
(We needed this to get the time-derivative term in Faraday's law)

emf is the integral of the force per unit charge, $$\vec{f}$$, all the way around the circuit
loop:

$$
\epsilon \equiv \oint \vec{f}\cdot d\vec{l}
$$

With an ideal source of emf (which is usually what we pretend to have) the voltage difference
between the two terminals of the battery is equal to the emf.

$$
V = -\int\vec{E}\cdot d\vec{l} = \epsilon \equiv \oint \vec{f}\cdot d\vec{l} = \epsilon
$$

#### Magnetic Flux
Magnetic flux is the integral of $$\vec{B}\cdot d\vec{a}$$

$$
\Phi = \int\vec{B}\cdot d\vec{a}
$$

$$
\epsilon = -\frac{d\Phi}{dt}
$$

That's called the "flux rule" for motional emf.


#### Faraday's law of induction

Given than emf is the integral of electric field around the loop (as shown above), then
a changing magnetic field must produce an electric field.  

$$
\int\vec{E}\cdot d\vec{l} = - \int\frac{\partial \vec{B}}{\partial t}\cdot d\vec{a}
$$

We can apply Stokes' theorem (the curl theorem) to get

$$
\nabla \times \vec{E} = - \frac{\partial \vec{B}}{\partial t}
$$

#### Maxwell's correction
Now that we have the magnetic field derivative term on the curl-E equation, we need
the electric field derivative term on the curl-B equation.  That's called Maxwell's
correction.

$$
\nabla \times \vec{B} = \mu_0 \vec{J} + \mu_0 \epsilon_0 \frac{\partial\vec{E}}{\partial t}
$$

We figured out that we needed this term to make the divergence of both sides of Ampere's law
zero. (Recall the divergence of a curl is always zero, so the right side has to be zero as well.)

#### So finally we have Maxwell's equations for dynamical situations
(We will need these to get light)

Gauss' Law

$$
\nabla \cdot \vec{E} = \frac{1}{\epsilon_0} \rho
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
\nabla \times \vec{B} = \mu_0 \vec{J} + \mu_0\epsilon_0\frac{\partial\vec{E}}{\partial t}
$$

#### Polarization Current
In order to get M's equations properly in media, we needed the concept of the
polarization current.

The electric polarization
$$\vec{P}$$ produces a bound charge density

$$
\rho_b = -\nabla \cdot \vec{P}
$$

and likewise we get bound current from a derivative of magnetization.

$$
\vec{J_b} = \nabla \times \vec{M}
$$

#### Maxwell's equations in matter end up looking like this:
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
