---
layout: page
title:  "The Electric Field"
permalink: "/lectures/electric"
---

You'll notice I didn't even put Coulomb's law in my crash course.  It's not that fun. Coulomb's law is technically an equation for Force, but I like the one
for the field better.

$$
\vec{E} = \frac{1}{4\pi \epsilon_0} \frac{q}{R^2}\hat{R}
$$

This $$\vec{R}$$ that Griffiths uses (he writes it as a script r) is kind of special. It 
takes a little getting used to:

$$
\vec{R} = \vec{r} - \vec{r^\prime}
$$
where $$\vec{r^\prime}$$ is the location of $$q$$ and $$\vec{r}$$ is the location
where you're calculating the field.
$$\vec{R}$$ points from $$q$$ to $$\vec{r}$$.

If you have a collection of charges then you sum this equation up (but just notice it's the same equation...)

$$
\vec{E} = \frac{1}{4\pi \epsilon_0}\Sigma_{i=1}^n \frac{q_i}{R_i^2}\hat{R}_i
$$

And if you have a charge distribution you do the integral... (but please...it's the same equation...)

$$
\vec{E} = \frac{1}{4\pi \epsilon_0}\int \frac{\rho(\vec{r^\prime})}{R^2}\hat{R} d\tau^\prime.
$$

Let's do an example!!
Example 2.2 page 64. 

---------For reference, we did not actually get to do the example in class-------------
