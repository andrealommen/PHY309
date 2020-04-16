---
layout: page
title:  "Poynting vector, Energy, Momentum in Electromagnetic Waves"
permalink: "/lectures/transmission"
---

### Where we are
For the last two weeks we've been putting together everything we have
gathered about Maxwell's equations in vacuum and in media to understand
the propagation of electromagnetic waves in vacuum and in media. 

### Where we're going
What happens next is:
* We need to talk about energy and momentum contained in E&M fields in general (we did
that last class),and then
specifically in E&M waves (we're doing that this class).
* We need to understand dispersion - how different wavelengths will travel at different velocities in a medium (next class)
----That's all this week, while you're studying for and taking the exam------
* Then we need to go back to potentials, particularly vector potentials, so that we can understand deferred potentials, so that we can understand how radiation occurs. (We've talked about electromagnetic waves, but you'll notice we haven't talked about how we generate them at all. We
ve just assumed they're there and tried to understand their properties. In this very last section of the course, we need to generate them.

### Poynting's Theorem

$$
\frac{dW}{dt} = -\frac{d}{dt}\int_V\frac{1}{2}\left((\epsilon_0E^2 + \frac{1}{\mu_0}B^2\right)d\tau - \frac{1}{\mu_0}\oint_S(\vec{E}\times\vec{B})\cdot d\vec{a}
$$

**The first term: energy contained in the fields** 

Energy density (energy per unit volume) in an EM field in general is:

$$
u = \frac{1}{2} \left(\epsilon_0E^2 + \frac{1}{\mu_0}B^2\right)
$$

the derivative of which is the first term in Poynting's theorem. 

**The second term: the rate of energy transported out of the volume**

The second term is the rate at which energy is transported out of the volume bounded
by the surface that you're integrating over.

So Poynting's theorem says that the work done on the charges by the electromagnetic
force is equal to the decrease in energy remaining in the fields, less the energy that
flowed out through the surface.

Some more on this since we didn't quite get a handle on what this meant last time:

Poynting's theorem relates the energy stored in the electromagnetic field to the 
work done on a charge distribution (i.e. an electrically charged object), 
through energy flux.

So if an electromagnetic wave shines on your forehead (for example) it will do
work on the charges in your forehead and heat them up.  You could either measure
$$\frac{dW}{dt}$$ by measuring the change in temperature of your forehead (which would 
be the easy way out in this case), OR, you
could choose a volume of space spanning your forehead, a couple of milimeters
into it, and measure the change in energy density of the field in that volume, and the amount 
of electromagnetic flux leaving that volume.  There would be some flux leaving that
volume, right?  Some of the EM wave would make it further than the 2mm into your forehead.
And some would get reradiated out as heat.  Both of those would be included in
the second term. 

In all the cases we're going to do today, we assume there's no work being done
on any charge distribution, so the left side is 0 and so the energy density
has a simple relationship to the flux.

The integrand of the second term has a name, the Poynting Vector, which is the energy
flux density (energy per unit area, per unit time) transported by the fields:

$$
\vec{S} = \frac{1}{\mu_0}(\vec{E}\times\vec{B})
$$


Last time:
### Maxwell Stress Tensor
The force per unit area (aka stress) acting on a surface.  The diagonal elements
are pressure, and the off-diagonal elements are shear.

$$T_{ij}$$ is the force per units area in the ith direction acting on an element of surface
oriented in the jth direction.  

$$
T_{ij} = \epsilon_0\left(E_iE_j - \frac{1}{2}\delta_{ij} E^2\right) + \frac{1}{\mu_0}\left(B_i B_j - \frac{1}{2}\delta_{ij}B^2\right) 
$$


Using T you can calculate electromagnetic force per unit area:

$$
\vec{F} = \oint_S \overline{T}\cdot d\vec{a}
$$

Momentum:

$$-\overline{T}\cdot d\vec{a}$$ is the electromagnetic
momentum per unit time passing through the area $$d\vec{a}$$.

There's a continuity equation for force and momentum ($$\vec{g}$$ is momentum
density):

$$
\frac{\partial \vec{g}}{\partial t} = \nabla \cdot \overline{T}
$$

$$
\vec{g} = \mu_0\epsilon_0\vec{S} = \epsilon_0(\vec{E} \times \vec{B})
$$

So the Poynting vector is proportional to momentum density. 

(Does this even make sense unit-wise?  
* S: energy per area per time (energy flow)
* u: energy per volume
* g: momentum density

The claim is that g and S are related by $$c^2$$.  Do we buy that?
even just for units??
Momentum density units should be mass times velocity
divided by volume. So that's $$mv/d^3$$.  If we multiplied by velocity that would be energy
density. So we would believe $$u/c = g$$. 

And then S is energy/(area time) and u is energy/volume.  So if you multiply $$u$$ by $$c$$
you would get the units of $$S$$.  So $$S =cu$$ would work. 

So then $$g= S/c^2$$.  Yes, the units do work out!! 

### This time:
We take this idea of the Poynting vector and use it to calculate the energy
transferred across boundaries in an electromagnetic wave.  In other words, we'll
calculate transmission and reflection coefficients.

Let's go back to the energy density in EM fields:

$$
u = \frac{1}{2} \left(\epsilon_0E^2 + \frac{1}{\mu_0}B^2\right)
$$

In the case of an EM wave:

$$
B = \frac{1}{c}E
$$

so

$$
B^2 = \mu_0\epsilon_0E^2
$$

So what are the relative contributions from the two terms?

from E

$$
\frac{1}{2} \epsilon_0 E^2
$$

from B

$$
\frac{1}{2} \frac{1}{\mu_0} B^2 = \frac{1}{2} \frac{1}{\mu_0} \mu_0\epsilon_0 E^2 =  
\frac{1}{2} \epsilon_0 E^2
$$

So the contributions in energy from the E and B fields are equal.  That makes sense, right?
The only reason the wave is propagating is that E is begetting B and B is begetting B at
just the right amount to be infinitely sustainable.

Here's my question for you. If $$u$$ is the energy density (energy per volume) and
$$S$$ is the energy per area per time. Come up with an equation that relates the two, using
only units.

$$
S = cu
$$

if you want vectors on it:

$$
\vec{S} = cu\hat{k}
$$

(I might skip the g equation below in class because I want to concentrate on S)

And we just figured out that g and S are related by $$c^2$$ so

$$
\vec{g} = \frac{1}{c^2} \vec{S}
$$

(All I really convinced you of before is that these units make sense.  You'd believe
they're in the same direction though, right?  Energy flow and momentum going in two
different directions would be weird.  You're used to energy and momentum in mechanics
being related by the velocity of a particle (and a factor of 1/2).  And energy **flow**
makes you bring in another factor of velocity (it should flow at the same velocity
as the wave, right?)  So, yes, this is in fact correct.)

### Intensity

If you're in a lab, what you really want is intensity.  How much energy is hitting
this particular area per time?   That's the Poynting vector.  Energy per area per time.
So intensity has the same units as the Poynting vector. 

$$
I \equiv <S> 
$$

where the fancy brackets around S indicate that it's the time averaged S.

The contribution to the total energy from the E-field is
$$
\frac{1}{2} \epsilon E^2.
$$
and the contribution from the B-field is the same.  So the total energy in
the EM wave at a particular time is:
$$
\epsilon E^2.
$$

This number will oscillate with the wave, at the frequency of the wave.  But
in the lab we don't want its oscillatin amplitude, we want the average of it
over time. The average of sine-squared wave is 1/2 the amplitude squared.

So

$$
<u> = \frac{1}{2} \epsilon E_0^2
$$

And S and u are related by v so

$$
<S> = \frac{1}{2} \epsilon v E_0^2
$$

$$
I = \frac{1}{2} \epsilon v E_0^2.
$$

### The Transmission coefficient

So finally we are in a position to calculate the transmission coefficient in a
situation where we've got a wave incident on a boundary.  You've already calculated
the amplitude of the transmitted wave by matching boundary conditions.  Now we can
use that amplitude to find out the intensity of the transmitted wave relative to
the intensity of the incident wave.  Namely, they are related by the square of
the amplitudes.

For example, at the end of section 9.3.2 (or the end of the [Boundary Conditions
in Reflection and Transmission lecture](reflection) we had:

$$
\tilde{E}_{0R} = \left(\frac{n_1-n_2}{n_1 + n_2}\right)\tilde{E}_{0I}
$$

and


$$
\tilde{E}_{0T} = \left(\frac{2}{n_1 + n_2}\right)\tilde{E}_{0I}
$$

If we put those into our equation for I we will get:

$$
R \equiv \frac{I_R}{I_I} = \left(\frac{E_{0R}}{E_{0I}}\right)^2 = \left(\frac{n_1-n_2}{n_1 + n_2}\right)^2
$$

$$
T \equiv \frac{I_T}{I_I} = \frac{\epsilon_2 v_2}{\epsilon_1 v_1}\left(\frac{E_{0T}}{E_{0I}}\right)^2 = \left(\frac{4n_1 n_2}{n_1 + n_2}\right)^2
$$

(If you have time, you can look at the question you worked out for the quarter-wave
plate problem here:
[In a quarter wave plate, can we really assume the transmission coefficients are the same?](quarterwaveplate) <br>


### Summary

Intensity you measure in a lab for an EM wave (time averaged Poynting vector):

$$
I \equiv <S> = \frac{1}{2} \epsilon v E_0^2.
$$

Lots of relationships between energy density, momentum, and poynting vectors.
$$
\vec{g} =  \frac{1}{c^2} \vec{S} = \epsilon_0(\vec{E} \times \vec{B})
$$

(Momentum density in a medium is controversial so I wrote that one in a vacuum -
see Griffiths note at the bottom of page 402.)

$$
\vec{S} = cu\hat{k}
$$

(I wrote that one in a vacuum, but it's equally true in media as long as you replace
$$c$$ with $$v$$.)


And we have this general equation for energy density:

$$
u = \frac{1}{2} \left(\epsilon_0E^2 + \frac{1}{\mu_0}B^2\right)
$$

and we realized that the energy contributions from the E and B fields are equivalent.
