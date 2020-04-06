---
layout: page
title:  "Can we really assume the transmission coeffients for the two polarizations are the same?"
permalink: "/lectures/quarterwaveplate"
---

#### Short answer.  yes.

#### Funner answer follows. (Thanks to Nathan Merrill for this question.)

On your last homework you found that the thickness of the quarter wave plate was

$$
t = \frac{\pi c}{2 \omega (n_x - n_y)}
$$

Let's turn that around and get the difference between $$n_x$$ and $$n_y$$ for a particular
thickness $$t$$.  In other words, if you want to make a quarter-wave plate out of a
material of thickness $$t$$ then the difference between $$n_x$$ and $$n_y$$ must be

$$
n_x - n_y = \frac{\pi c}{2 \omega t}
$$

I think this equation would make more sense in terms of the wavelength $$\lambda$$:

$$
\omega = \frac{2\pi c}{\lambda}
$$

then

$$
n_x - n_y = \frac{\pi c}{2 \left(\frac{2\pi c}{\lambda}\right) t}
$$

$$
n_x - n_y = \frac{\lambda}{4 t}
$$

Oh, look at that!!  It's a **quarter** wave plate and the index of refraction has to
be different by the ratio between a quarter wavelength and the thickness of the material.

For typical numbers what is that difference $$n_x - n_y$$?  I'm not sure I've ever seen a quarter-wave plate, but let's go for a quarter of a cm.  And the middle of the optical band has a wavelength of 600 nm.  So then

$$
n_x - n_y = \frac{600 nm}{4 \times .25 cm} = 6 \times 10^{-6}
$$

That's pretty small!!  Okay, but does it justify our idea that the transmission 
coefficients are identical?  

The transmission coefficient for normal incidence between two materials $$n_1$$ and
$$n_2$$ is:

$$
T = \frac{4n_1 n_2}{(n_1 + n_2)^2}
$$

Let's assume we're going from air $$n_1=1$$ to either $$n_x$$ or $$n_y$$. Let's assume
$$n_x = n$$ and $$n_y = n + \delta$$.

The ratio of the two transmission coefficients (to $$n_x$$ or to $$n_y$$) is then

$$
\frac{T_y}{T_x} = 
\frac{
 \frac{4n(n+\delta)}{(1 + n + \delta)^2}
}{
 \frac{4n(n)}{(1 + n)^2}
}
$$

$$
\frac{T_y}{T_x} = \left(\frac{n+\delta}{n}\right)\left(\frac{1 + n}{1 + n + \delta}\right) 
$$


$$
\frac{T_y}{T_x} = \left(1+\frac{\delta}{n}\right)\left(\frac{1}{1 + \frac{\delta}{1 + n}}\right) 
$$

Use a Taylor series on the second term.

$$
\frac{T_y}{T_x} = \left(1+\frac{\delta}{n}\right)\left({1 - \frac{\delta}{1 + n}}\right) 
$$

$$
\frac{T_y}{T_x} = 1+\frac{\delta}{n} - \frac{\delta}{1 + n} + h.o.t.
$$

$$
\frac{T_y}{T_x} = 1+\frac{\delta}{n^2+1}  + h.o.t.
$$

By our previous calculation $$\delta$$ is going to have a value like $$10^{-5}$$
and the denominator really isn't that much different than unity.  So the difference
in transmission coefficients is going to be a factor of $$\approx 1.00001$$.
The light goes through two interfaces with the same transmission coefficient so
the number we're interested is $$T^2$$, but
1.00001 squared is still something like 1 part in $$10^5$$.
So the difference in the intensity of light between the two polarizations will
be something like one part in 
$$10^5$$.

### Summary

The difference between $$n_x$$ and $$n_y$$ in a quarter wave plate is really small.   Roughly
it's one part in however many wavelengths can fit in the width of the quarter wave plate. 
That same number (one part in the number of wavelengths across the width of the plate) is
how different the two transmission coefficients are.



