---
layout: page
title:  "Electromotive Force and Induction"
permalink: "/lectures/induction"
---

### Last time:

### The Auxiliary Field

We said that the total current density was the sum of the free and bound current, where
the so-called "bound" current is created by the alignment of atoms in the material. 

$$
\vec{J} = \vec{J}_b + \vec{J}_f
$$

$$\vec{H}$$ the auxiliary field, is the field (divided by $$\mu_0$$) that would be
there if only the free current existed.  The piece due to the magnetism is subtracted off.

$$
\vec{H} = \frac{1}{\mu_0} \vec{B} - \vec{M}
$$

and Ampere's law now reads:

$$
\nabla \times \vec{H} = \vec{J}_f
$$

or in integral form:

$$
\oint \vec{H}\cdot d\vec{l} = I_{free}
$$

## TODAY: Electromotive Force and Induction

We've already had charges moving in currents, but all of our
currents have been steady.  Today we'll get to electrodynamics,
i.e. electromagnetic changes.

Where we're going....

We need Ohm's law (and we'll talk about how it's not a law)

$$
\vec{J} = \sigma \vec{E}
$$

And we want to see why conductivity ($$\sigma$$) is proportional
to charge density and why it increases with decreasing temperature.

We are getting to Faraday's law:

$$
\nabla \times \vec{E} = - \frac{\partial \vec{B}}{\partial t}
$$

via the flux rule:
$$
\epsilon = -\frac{d\Phi}{dt}
$$

But to get there we need to talk about Ohm's law and how it's not a law.

#### Why is Ohm's law not a law?
Well, it's not always true.    It's more of a generalization of
the way a lot of materials behave.  For many materials, the current
density $$\vec{J}$$ is proportional to the force on the charges, i.e.

$$
\vec{J} = \sigma \vec{f}
$$

where $$\vec{f}$$ is the force per unit charge.

In most cases the electric field is providing the dominant force
on the charges and the force is proportional to the electric
field so

$$
\vec{J} = \sigma \vec{E}
$$

and that is known as "Ohm's law."

A more familiar version of the law is:

$$
V = IR
$$

where $$R$$ is the resistance, and $$V$$ is the voltage between two points,
and $$I$$ is the current flowing between those points.

Why would you even expect Ohm's law to be true?  A steady force on a charge
should accelerate it, right?  But the "law" seems to say that the
charges will achieve a constant velocity (or current.)  Why?

#### How current works
We need to understand how current works in order to talk about electromotive force.
We need electromotive force to talk about Faraday's law, which is where we're going!

Griffiths has a nice analogy on page 300 about driving in a car and having to
stop at lights and stop signs.  You accelerate in between, but ultimately
your average speed is quite constant and predictable.

Electrons are quite similar, except instead of stop signs they have
collisions.

I would like you to arrange the following variables into a formula for
current density based on your (and your neighbor's) intuition.

* $$\vec{J}$$: current density
* n: the number of molecules per volume
* q: the charge on one electron
* f: the number of free electrons per molecule
* $$\lambda$$: the distance between collisions (would you got faster or slower in your car if there were more space between stoplights?)
* m: the mass of an electron
* $$\vec{E}$$: the electric field
* $$v_{thermal}$$: the thermal velocity of the electrons (the random velocity of the electrons, NOT the velocity due to the electric field)


When you've got a formula for $$\vec{J}$$ see if you can
make if have the right units.

The thing they will get wrong most likely is thermal velocity... so
at some point (after they've wrestled with it a little) give them this hint...

What should happen with the thermal velocity? You've probably decided
that the shorter the distance is between collisions the slower you
will go.  That's correct.    

But what effects how short the distance is between collisions?  

Let's think instead of the time between collisions.  How much time is
in between collisions?  

$$
t_{between~collisions} = \frac{\lambda}{v_{thermal}}
$$  

where $$\lambda$$ is the distance between them.  So the shorter
the time between collisions the lower the

What's the relationship between the average velocity of the current, i.e.
the $$\vec{v_{ave}}$$ in

$$
\vec{J} = \rho \vec{v_{ave}}
$$

and the thermal velocity?  Ans:   The thermal velocity just tells
you the time in between colisisions, and the velocity of the charges
is determined by the acceleration due to the electric field and
the time in between collisions, like this:

$$
v_{ave} = \frac{1}{2} at
$$

where $$a$$ is the acceleration due to the field and $$t$$ 
is $$\frac{\lambda}{v_{thermal}}$$.


$$
v_{ave} = \frac{1}{2} \frac{qE}{m_e}\left(\frac{\lambda}{v_{thermal}}\right)
$$

where $$a$$ is the acceleration due to the field and $$t$$ 
is $$\frac{\lambda}{v_{thermal}}$$.

And $$\rho$$ is $$nfq$$ (the number of electrons per volume times the
charge per electron).  So now we can put it all together...


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

#### What does this formula have to do with emf?    Griffiths (pg 303)  has a really nice explanation
of why you get current moving in a loop at all.    You've only got the battery connected
in one place, but somehow the current is constant all the way around?  Seems very unlikely,
but in fact it's quite a magnificent approximation to the truth.  It's because if the
current is not constant, then you get charges piling up somewhere, and then you get a
larger E-field and then the current goes faster and corrects itself.   This is only
possible because of the way current actually works (via collisions as above).  That's the
connections. 

A couple important reminders...and if they're not reminders then please read about them...

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
(We need this to get Faraday's law, in which an electric field is generated by a changing
flux. We're going to get there by way of showing than an emf (electromotive force) is
generated by a changing flux.)

I remind you that magnetic flux is the integral of $$\vec{B}\cdot d\vec{a}$$

$$
\Phi = \int\vec{B}\cdot d\vec{a}
$$

So if I have a constant magnetic field B coming out of the board in the shaded
region, then the magnetic flux through the loop is the magnetic field
times 
the height $$h$$ and width $$x$$ of the region the magnetic flux is in

![Griffiths Figure 7.10](Figures/Figure7.10.png){:class="img-responsive"}

$$
\Phi = Bhx
$$

(On page 306 Griffiths does a really nice motivation of the following using the
notion of force per charge $$\vec{f}$$ as described above.)

If this loop is moving out of the magnetic field, at velocity $$v$$, then the emf
generated is $$-Bhv$$. In general

$$
\epsilon = -\frac{d\Phi}{dt}
$$

That's called the "flux rule" for motional emf.


#### Faraday's law of induction

Faraday did a whole bunch of experiments with this.  All of which you will notice produce
an emf by the rules above.

* Experiment 1: He pulled a loop of wire to the right through the magnetic field.  A current flowed through the loop.
* Experiment 2: He moved the magnetic field to the left, holding the loop still. Again, a current flowed in the loop.
* Experiment 3: With both the loop and the magnet at rest he changed the strength of the field. Once again, current flowed through the loop.

Given than emf is the integral of electric field around the loop (as shown above), then
a changing magnetic field must produce an electric field.  


$$
\epsilon = \int\vec{E}\cdot d\vec{l} = -\frac{d\Phi}{dt}
$$

and

$$
\Phi = \int\vec{B}\cdot d\vec{a}
$$

So then

$$
\int\vec{E}\cdot d\vec{l} = -\frac{d \int\vec{B}\cdot d\vec{a}}{dt}
$$

$$
\int\vec{E}\cdot d\vec{l} = - \int\frac{\partial \vec{B}}{\partial t}\cdot d\vec{a}
$$

That is Faraday's law in integral form.  We can apply Stokes' theorem (the curl theorem)
to get

$$
\nabla \times \vec{E} = - \frac{\partial \vec{B}}{\partial t}
$$

Next time we'll talk about how Faraday's law fits together with all of Maxwell's equations.

#### To review: 

We talked about Ohm's law not really being a law, but rather something that a lot of
materials seem to follow.  In it's general form it looks like this:

$$
\vec{J} = \sigma \vec{E}
$$


We talked about an average speed of charges as they undergo collisions in a constant
electric field, and we came up with:

$$
\vec{J} = nfq\vec{v}_{ave} = \left(\frac{nf\lambda q^2}{2m_e v_{thermal}}\right)^2 \vec{E}
$$

which shows
why conductivity ($$\sigma$$) is proportional
to charge density and why it increases with decreasing temperature.

Armed with this notion of Ohm's law, we could talk about what creates a constant
current in circuit.  An emf $$\epsilon$$ is the integral of force per charge
around a current. We used the notion of magnetic flux, and emf to find the flux rule:

via the flux rule:
$$
\epsilon = -\frac{d\Phi}{dt}
$$

and then Faraday's law.

$$
\nabla \times \vec{E} = - \frac{\partial \vec{B}}{\partial t}
$$


