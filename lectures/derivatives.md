---
layout: page
title:  "All the Fundamental Theorems Together"
permalink: "/lectures/derivatives"
---

Fundamental theorem of **calculus**:

$$
\int_a^b \left(\frac{df}{dx}\right)dx= f(b) - f(a)
$$

Fundamental theorem for **gradients**:

$$
\int_a^b (\nabla T)\cdot d\vec{l} = T(\vec{b}) - T(\vec{a})
$$

Fundamental theorem for **divergences**:

$$
\int_V (\nabla \cdot \vec{v})d\tau = \oint_S \vec{v}\cdot d\vec{a}
$$

Fundamental theorem for **curls**:

$$
\int_S (\nabla \times \vec{v})\cdot d\vec{a} = \oint_P \vec{v} \cdot d\vec{l}
$$

On the left side is an integral over a derivative, which you can see from the
first theorem, gives you back the original function evaluated at the endpoints.
For the other derivatives it's a little more complex, but in every case
on the left-hand side there is an integral over a derivatives, and on the right-hand side there's the function evaluated at boundaries.

In the case of divergence the integral is over a volume, and the right side
is evaluated over the surface that bounds that volume.

In the case of the curl the integral is over a surface, and the right side
is evaluated over the perimeter that bounds that surface.

The curl theorem (usually called Stokes' theorem) is the most funky (IMHO) 
because there are many different surfaces you can choose whose perimeter
will be the same. Stokes' theorem is true for all of those surfaces.

I think the hardest part about applying these theorems is getting
the direction of $$d\vec{l}$$ and $$d\vec{a}$$.  In the divergence
theorem $$d\vec{a}$$ always points _out_ of the volume. In the curl theorem
the relationship between $$d\vec{l}$$ and $$d\vec{a}$$ is given by the
right-hand-rule. Your fingers curl around in the direction of $$d\vec{l}$$
and your thumb points in the direction of $$d\vec{a}$$. In both cases
$$d\vec{a}$$ points perpendicular to the surface at each point.
