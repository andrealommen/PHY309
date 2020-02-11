---
layout: page
author: Andrea Lommen
title: Common Mistakes 
permalink: /common/
---

# Assignment #1

## Tip for dealing with integrals over the volume, i.e.:

$$
Q_{encl} = \int_0^a \rho(r) d\tau
$$

### Short version of my tip:

If the the function you're integrating over (e.g. charge density $$\rho(r)$$) only depends
on $$r$$ then don't integrate over both $$\phi$$ and $$\theta$$, just
say

$$
Q_{encl} = \int_0^a \rho(r) 4\pi r^2 dr
$$

### Long version of my tip:

Lots of you said (on #6 on the HW):

$$
Q_{encl} = \int_0^a\int_0^\pi \int_0^{2\pi} \rho(r) r^2 \sin\theta d\theta d\phi dr
$$

which is absolutely correct, but you totally don't need to go through that trouble.

For spherically symmetry functions

$$
d\tau = 4\pi r^2 dr ~~~~~{\rm For~spherically~symmetric~functions.} 
$$

$$4\pi r^2 dr$$ is a perfect, differentially small volume element, as long as whatever you're integrating over only depends upon $$r$$ and not on $$\theta$$ and $$\phi$$.  In other words, as long as your problem has spherical symmetry.

Another version I saw was

$$
Q_{encl} = \int_0^a \rho(r) dr ~~~~~{\rm this~is~wrong}
$$

That version is actually incorrect. $$\rho(r)$$ is a charge per volume, so in order to get charge you need to integrate over the volume.  You can get a clue
about whether you're integrating over something reasonable by looking at its
units. $$dr$$ only has units of length, so it can't be a volume.  $$4 \pi r^2 dr$$ has units of length cubed, so it's a volume.  

Whenever I'm "setting up integrals" which I think is physics speak for "making stuff up that looks like an integral and will hopefully give me the answer I want" I look carefully at the units of the thing. The units have to work out in the integral for the units to work out in the problem. $$dr$$ has units of length.
