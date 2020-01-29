---
layout: page
title:  "Divergence and Curl of Electric fields, Gauss's Law)"
permalink: "/lectures/divcurlE"
---

#### Griffiths 2.2

Divergence theorem:

$$
\int_V (\nabla \cdot \vec{v})d\tau = \oint_S \vec{v}\cdot d\vec{a}
$$

Curl Theorem:

$$
\oint \vec{E}\cdot d\vec{a} = \frac{1}{\epsilon_0}Q_{enc}
$$

Maxwell's Equation for divergence of E:<br>
(Remember we expect the divergence of E to be significant because we know
what the field lines look like, and they diverge!)

$$
\nabla \cdot \vec{E} = \frac{1}{\epsilon_0}\rho 
$$

Deriving the more familiar form of Gauss's law...

Integrate both sides over the volume
$$
\int_V\nabla \cdot \vec{E} d\tau = \int_V\frac{1}{\epsilon_0}\rho d\tau 
$$

We can use the divergence theorem on the left side and rearrange the right
side a little:

$$
\oint_S \vec{E}\cdot d\vec{a} = \frac{1}{\epsilon_0}\int_V\rho d\tau
$$

Oh that integral on the right side is just the integral of the current density
over the volume, so that's the charge enclosed in that volume, aka $$Q_{enc}$$.


$$
\oint_S \vec{E}\cdot d\vec{a} = \frac{1}{\epsilon_0}Q_{enc}
$$

On Monday we were talking about how one of the trickiest things is figuring
out what $$\vec{a}$$ and which $$\vec{E}$$ these are.  I think seeing this 
derivation and keeping it in mind really helps. 

Gauss' Law, though usually in kind of unhelpful form, is simpler than the 
integral form above...there's no integral and no dot product.  It just says that everywhere in space the divergence of E is proportional the charge density at that point in space (with the constant of proportionality being $$1/\epsilon_0$$.)

Then when we use the Divergence Theorem to get the more familiar form we know that the integral over The Volume (whatever volume you pick) and the integral over the surface area must be related. The surface has to bound the volume.

Griffiths has a really nice couple of pages 66-68 that do a really nice job of arguing pictographically that you would actually kind of expect the $$
\oint_S \vec{E}\cdot d\vec{a} = \frac{1}{\epsilon_0}Q_{enc}
$$ version of Gauss' law to be true by staring at pictures of field lines. 

![Figure 2.12 from Griffiths](/PHY309/figures/Figure2.12)

Look at the figure and imagine that you enclose it with a sphere.  And you count the field lines that are crossing the sphere.  No matter how big or small you
make the sphere you get the same number of field lines crossing your sphere.  So the number of field lines crossing that sphere seems to be an indication of the charge enclosed.   And look even further - the direction that they cross seems to tell you the sign of the charge.  That's the 
$$
\oint_S \vec{E}\cdot d\vec{a} = \frac{1}{\epsilon_0}Q_{enc}
$$
version of Gauss's law. When you're answering the question about how many field
lines cross the surface, yu are doing that integral on the left-hand side.  
And the right hand side tells you that that's proportional to the charge 
enclosed by the sphere.  

Apparently, the Electric flux through any closed surface is a measure of the charge inside. 

![Figure 2.13 from Griffiths](/PHY309/figures/Figure2.12)

Here's the field from two oppositely charged particles. Is it still true?

Let's draw a sphere around these charges as well.  The situation doesn't
really have spherical symmetry but let's still draw a sphere. According
the
$$
\oint_S \vec{E}\cdot d\vec{a} = \frac{1}{\epsilon_0}Q_{enc}
$$
version of Gauss' Law, the integral on the left hand side, over the surface,
should be zero, because the total charge enclosed is zero.  Can you 
imagine that that's true?  Yes, check it out.  On every point on the sphere
on the left-hand side of the equation you take the $$\vec{E}$$ vector at
that point, and dot it into the $$d\vec{a}$$ vector that is pointing radially
outward.  Then you integrate that dot product all over the surface of the
sphere.  It looks like it would kind of be a mess, because the E-vector
isn't pointing radially at all points.  But look at this, for every time
the E-vector is pointing in, there's a point opposite it where it's pointing
out.  The sum over those two points will be zero, so the integral over
the whole thing will be zero.

So once again, the flux through any closed surface is a measure of the charge inside. 

Griffiths conducts this same discussion in a somewhat different order.  He starts with Coulomb's law, convinces you that the flux through a surface should be
a measure of the charge inside, and arrives at Gauss's law.  Then he uses
the Divergence Theorem to get you Gauss' Law in integral form:
$$
\nabla \cdot \vec{E} = \frac{1}{\epsilon_0}\rho 
$$
As always, it's worth reading.

Also please note that if you know \vec{E} everywhere you can find the
charge density $\rho$ by taking the divergence of $\vec{E}$.  This is very useful in problem _____ on your homework..

### Applications of Gauss' Law

Basically, if you can use Gauss' Law to do a problem you should.  Problem \#4 on your problem set will convince you of that (that is in fact the main point of the problem.)

The industry standard at this moment is to do three Gauss' Law problems:
* One with spherical symmetry
* One with cylindrical symmetry
* One with planar symmetry

That's what we'll do!!

**Spherical Symmetry**

Let's take charge $$q$$ and spread it evenly over the surface of a sphere of radius $$a$$.

Gauss' Law is true for any surface we choose.  But the only surfaces that make
it useful are ones where the symmetry helps us. In other words, ones where the
symmetry is such that the field is constant over the surface.

So we get to draw our Gaussian sphere wherever we want. 

There's no charge inside of radius a. 

All the Gaussian surfaces (which, to be clear, are completely imaginary) I'm about to draw are going to be spheres with a radius, r.  With this spherical charge distribution, the E-field on any sphere is going to be constant all over the sphere.  That's what is going to make our life easy.

*Region inside of a, r<a*
With $$r<a$$ the surface encloses no charge, so the right side of  
$$
\oint_S \vec{E}\cdot d\vec{a} = \frac{1}{\epsilon_0}Q_{enc}
$$
is zero.  We could do the integral explicitly (Griffiths does this if you'd
like to see that) but I'd rather say that if we know the magnitude of
$$E$$ is constant
across the sphere, and always points parallel to the area 
element $$d\vec{a}$$ then the integral is just $$E$$ times the 
area of the sphere. So we can get rid of the dot product because the two
vectors are always parallel, and replace them with their magnitudes. 

$$
E4\pi r^2 = 0
$$

And now we're left with a very boring equation for $$E$$, i.e. $$E=0$$.  So we conclude that inside the radius $$a$$ the field is zero.

This is a rather famous result, that the field due to a spherical shell of charge is zero inside the sphere.

--------For reference this is how far we actually got in this class---------

*Cylindrical Symmetry*
Here Griffiths has an interesting example that I will use exactly (page 73).
It's a cylinder where the charge density is proportional to the distance from
the central axis, $$s$$. In particular $$\rho = ks$$.  I like this example
because though there is cylindrical symmetry, Gauss's law still leaves us
an integral to do (for its right side) because of the curious charge distribution. And it also
gives us practice forming integrals as we were talking about on Monday.

$$
Q_{enc} = \int_v \rho d\tau
$$

Again, Griffiths actually writes down $$d\tau$$ in cylindrical coordinates 
$$d\tau = sdsd\phi dz.  If you think about it that way, that's great.  I don't. If I had to take apart my thought process it's something like this:
* I have a volume integral.
* But the only thing I need to integrate over is $$s$$, because that's the
only thing $\rho$ depends upon. 
* So what's the volume element at a particular $$s$$? The thing I want is whatever you have to multiply by $$ds$$ to get a volume. (Griffiths might say: After I've integrated over $$\theta$$ and $$\phi$$ what would I have?)
* The circumference is $$2\pi s$$, and the circumference times the length
is $$2\pi sl$$.  That's an area.  If I multiply that by $$ds$$ that's a volume.
* Therefore my volume element is $$2\pi slds$$. 
* I check that the volume element is really a volume - yup it has units of length cubed.
* $$Q_{enc}= \int_0^s \rho(s^\prime) 2\pi s^\prime l ds^\prime = 2\pi kl \int_0^s {s^\prime}^2ds^\prime=2\pi kl s^3/3$$ 
* Does that have the right units?  $$kl$$ is a charge density, so 
if we multiply that by a volume that should have units of charge.  So yes!

So now we put that into Gauss's law:

$$
\oint_S \vec{E}\cdot d\vec{a} = \frac{1}{\epsilon_0}Q_{enc}
$$

$$
\oint_S \vec{E}\cdot d\vec{a} = \frac{1}{\epsilon_0}\frac{2}{3} \pi kl s^3
$$

What's the left side? It's the integral over the area $$4\pi s^2$$. The electric
field is constant over the curvey part of the area $$ 2\pi sl E$$ (the circumference
of the curvey part times it's length) and zero over the ends of the cylinder.

Why is it zero over the ends of the cylinder?  In this case it's because
of the dot product $$\vec{E}\cdot d\vec{a}$$. Those two vectors are perpendicular to each other at the flat ends of the cylinder.

$$
2\pi sl E  = \frac{1}{\epsilon_0}\frac{2}{3} \pi kl s^3
$$

And now we can solve for E

$$
E  = \frac{1}{\epsilon_0}\frac{1}{3} k s^2
$$

What direction will it be?  $$\hat{s}$$

Let me give you practice coming up with the right integral to do and
figuring out what to put on both sides of the equation.
Let's do a spherical charge distribution, but this time it depends upon
$$r$$. For $$r<a$$ $$\rho(r) = kr$$. 

$$
\oint_S \vec{E}\cdot d\vec{a} = \frac{1}{\epsilon_0}Q_{enc}
$$

for r<a
$$
E4\pi r^2 = \frac{1}{\epsilon_0} \int_0^r(\rho(r) 4\pi {r^\prime}^2 dr^\prime
$$

While you're doing that I'll create a poll for the answer.

**The curl of E**

We talked on Monday about the curl of E being zero everywhere that the
B-field isn't changing. In the last part of 2.2 Griffiths proves this
using Coulomb's law.  Here's the brief version:

Coulomb's law 

Coulomb's law for a point charge at the origin

If we want to prove that the curl is zero, we could use the curl theorem
to transform the curl into something else that's easier to integrate.

Fundamental theorem for **curls**:

$$
\int_S (\nabla \times \vec{v})\cdot d\vec{a} = \oint_P \vec{v} \cdot d\vec{l}
$$

(That was to remind you that's generally true of any vector!!)  Now let's apply it to E-fields.

$$
\int_S (\nabla \times \vec{E})\cdot d\vec{a} = \oint_P \vec{E} \cdot d\vec{l}
$$

So we will do a line integral of E from a to b.

Coulomb's law is.

$$
\vec{E} = \frac{1}{4\pi \epsilon_0} \frac{q}{R^2}\hat{R}
$$ 

For a point charge at the origin $$R$$ becomes $$r$$.

$$
\vec{E} = \frac{1}{4\pi \epsilon_0} \frac{q}{r^2}\hat{r}
$$ 

And in spherical coordinates the line element is
$$
dl = dr \hat{r} + rd\theta \hat{\theta} + r\sin{\phi}d\phi \hat{\phi}
$$

So we dot those two together and we get:

And the integral of that will be 

$$
 = - \frac{1}{4\pi \epsilon_0} \frac{q}{r} |_a^b
$$

That will be zero if points $$a$$ and $$b$$ are the same, i.e. if it's a
close-loop integral.

The integral of the curl over any surface by any close-line perimeter will be 
zero, no matter how small or large that surface is.  So therefore the the curl 
of $\vec{E}$ must be zero in general.


