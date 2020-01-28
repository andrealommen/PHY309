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
lines cross the surface, yu are doing that integral on the left-hand side.  And the right hand side tells you that that's proportional to the charge enclosed by the sphere.  
