---
layout: page
title:  "The Need for Boundary Conditions and the Idea of Potentials"
permalink: "/lectures/potentials"
---

We pick up a couple things for reference, that will come in handy later.
They both relate to this vector derivatives (grad, div, curl) that we've
been talking about.

Important point: I'm going on and on about the divergence and the curl, 
because Maxwell's equations specify the divergence and the curl of the
E- and the B- fields.

### The Helmholtz Theorem

So one question you could ask is....

If we know the divergence and curl of a field, do we know the field?

No.

If we know the divergence and curl of a field, and the value of the field
at a boundary, do we know the field?

Yes.

In other words, we need **boundary conditions** in order to specify the field in many cases. We'll get to boundary conditions officially in chapter 3 when we talk about potentials more. 

### Scalar Potential

If the curl of a field (say **E**) vanishes everywhere, then **E** can be
written as the gradient of a scalar potential (V):

$$
\nabla \times \vec{E} = \vec{0}  ~~~  \rightarrow ~~~~ \vec{E} = -\nabla V.
$$

Griffiths wants to make sure you know this is true for ANY curl-less
vector field, not just for $$\vec{E}$$ although $$\vec{E}$$ is certainly
the thing upon which we're going to employ it.. 

Is $$E$$ always curl-less (i.e. is $$\nabla \times \vec{E}$$ always 0?)

No, but most of the time it is. Let's see it two ways.

1) Consider a point charge. An electron. Which way does the field point?  Towards it.  Does it have any curl?  No, there's no "swirliness" to the E-field. It's all divergence, and no curl (sounds like a hair-care ad.)

Okay, but that was for a point charge.  Is that generally true? Yes!  Any charge distribution can be made up of a sum of charges, and the E-field is the sum
of the field due to each charge.  So the E-field is a sum of curl-less fields. Is there any way to add a bunch of curl-less fields together and get a curl-ful field?

No, because the curl of a sum is the sum of the curls, so if the curl
of each of the 
individual fields that you're adding together is 0 then 
the curl of their sum is also zero.

2) Look at Maxwell's 4th equation, aka Faraday's law

$$
\nabla \times \vec{E} = -\frac{\partial B}{\partial t}
$$

So $$\nabla \times \vec{E} = 0$$ as long as $$\vec{B}$$ isn't changing in time.

(That's pretty interesting - I knew that a changing $$\vec{B}$$ would induce an
electric field, but I don't think I appreciated that a changing $$\vec{B}$$
would produce a curl-full E-field!! I'm looking forward to learning more
about that.)

### Vector Potential
AKA the potential that gives you $$\vec{B}$$.

If a vector field (say $$\vec{B}$$ for example) is divergence-less, i.e.
$$\nabla \cdot \vec{B} = 0$$ then $$B$$ can be expressed as the the
curl of some function, i.e.

$$
\vec{B} = \nabla \times \vec{A}
$$

where $$\vec{A}$$ is called the *vector potential.*

Is $$\vec{B}$$ always divergence-less? Yes, that's Maxwell's 2nd equation:

$$
\nabla \cdot \vec{B} = 0
$$

(Also called the "no magnetic monopoles" formula. If a magnetic monopole is
ever found, that formula will change. It makes sense, right?  that without
a magnetic "charge" you can't get that perfect diverging field that we
think of for an electric charge.) 

### Two things to notice about the above

In both cases, i.e. $$\vec{E} = \nabla V$$ and $$\vec{B} = \nabla \times \vec{A}$$ the field is the derivative of some other function, which means that there's
an arbitrary element that can be added to $$V$$ or $$\vec{A}$$ the will not 
affect the field.  In the case of $$V$$ it's any constant. In the case
of $\vec{A}$ it's the gradient of any scalar (because the curl of a gradient
is mathematically (and therefore without exception) zero.)  

Notice why you need that caveat that these things can only be expressed
as the gradient (curl) of a scalar (vector)... if the curl (divergence) is zero... 

### E-field case
We need $$\nabla \times \vec{E} = 0$$ (most of the time, by physics) and the curl of
a gradient is 0 (all of the time, by math).  So if $$\nabla \times \vec{E} \ne 0$$
but $$\nabla \times (\nabla V) = 0$$ then we can't express $$E$$ as $$\nabla V$$.

### B-field case
Similarly we need $$\nabla \cdot \vec{B} = 0$$ (all of the time, by Maxwell's
equations, by physics) and the
divergence $$\nabla \cdot (\nabla \times \vec{A}) = 0$$ (all of the time, by
math). So $$\nabla \cdot \vec{B}$$ isn't 0, then it's a problem if
$$\nabla \cdot (\nabla \times \vec{A})$$ is 0, and the whole idea of a vector
potential falls apart.
