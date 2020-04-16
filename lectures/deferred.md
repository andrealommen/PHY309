---
layout: page
title:  "The Deferred Potential"
permalink: "/lectures/deferred"
---

(Note to reader: your textbook calls this the "retarded potential." We
opted to call it the "deferred potential" instead.)

### The scheme for the week 
* Then we need to go back to potentials, particularly vector potentials, so that we can understand deferred potentials, so that we can understand how radiation occurs. (We've talked about electromagnetic waves, but you'll notice we haven't talked about how we generate them at all. We
ve just assumed they're there and tried to understand their properties. In this very last section of the course, we need to generate them.

### What we did last time. 


### Started with Maxwell's equations

Gauss' Law

$$
\nabla \cdot \vec{E} = -\frac{1}{\epsilon_0} \rho
$$

(no name...no magnetic monopoles?)

$$
\nabla \cdot \vec{B} = 0
$$

Faraday's Law

$$
\nabla \times \vec{E} = -\frac{\partial\vec{B}}{\partial t}
$$

Ampere's Law with Maxwell's correction

$$
\nabla \times \vec{B} = \mu_0 \vec{J} + \mu_0 \epsilon_0 \frac{\partial\vec{E}}{\partial t}
$$

We had to rewrite our equation for the relationship between E and V.

$$
\vec{E} = - \nabla V - \frac{\partial\vec{A}}{\partial t} 
$$

Which made us revise Poisson's equation:

$$
\nabla^2 V  +\frac{\partial}{\partial t}(\nabla \cdot \vec{A}) = -\frac{1}{\epsilon_0} \rho
$$

That gave us the relationship between V,A, and $$\rho$$.
Then we need a relationship between V, A, and the current density $$\vec{J}$$.

$$
\left(\nabla^2\vec{A} - \mu_0 \epsilon_0 \frac{\partial^2 \vec{A}}{\partial t^2 }\right)
- \nabla\left(\nabla\cdot\vec{A} + \mu_0\epsilon_0\frac{\partial V}{\partial t}\right) = -\mu_0\vec{J}
$$

That two equations contain all the information
in Maxwell's equations.

Just as before, our two new equations do not uniquely determine the potentials.  We
can add things to V and $$\vec{A}$$ as long as they don't change E and B.  That's
called "gauge freedom".

We looked at two gauge conditions/restrictions/transformations (depending on who
you ask).

### The Coulomb Gauge

$$
\nabla \cdot \vec{A} = 0
$$

which gives us back:

$$
\nabla^2 V = -\frac{1}{\epsilon}\rho
$$

That's a nice equation for V.  The equation for A isn't great.

### The Lorenz gauge

This is the one we'll use for the rest of the semester. We choose this
relationship between A and V.

$$
\nabla \cdot \vec{A} = -\mu_0\epsilon_0\frac{\partial V}{\partial t}
$$

If you do that you get 


$$
\square^2V = -\frac{1}{\epsilon_0}\rho
$$

$$
\square^2\vec{A} = -\mu_0\vec{J}
$$

where

$$
\nabla^2 - \mu_0 \epsilon_0 \frac{\partial^2 }{\partial t^2 } = \square^2
$$

It's called the d'Alembertian.

### What's important to take away from here?

* Expressing E and B in terms of V and A is helpful for doing problems, but
we had to adjust our equation for E to depend on both V and A in order for the
situation to work.
* To those V and A you can add things that don't change the field.  That's called a 
gauge transformation.
* We will be in the Lorenz gauge for the rest of the semester, which means that
we have the two wave equations above involving the d'Alembertian $$\square^2$$
which is actually pretty familiar set of operations that we know gives us waves.

### How do we know this gauge is valid? (a post-lecture note)
As with the Coulomb gauge I'm trying to figure out how we know the 
Lorenz gauge meets our criteria:
``To A we can the gradient of any scalar $$\lambda$$ as long as we subtract the
time-derivative of that same scalar from $$V$$.''  

I found an interesting answer on [StackExchange.](https://physics.stackexchange.com/questions/129819/showing-that-coulomb-and-lorenz-gauges-are-indeed-valid-gauge-transformations)
They actually kind of throw
Griffiths under the bus for calling it a gauge transformation.


Here's my summary of what's on that page.  "The Coulomb and Lorenz gauges are gauge fixing conditions, not gauge transformations."  A gauge transformation looks
like this

$$
\tilde{A}_\mu = A_\mu + d_\mu\Lambda
$$

(This is a 4-dimensional version of 
our criteria using $$\lambda$$. You can make the scalar and the vector 
potential into a 4-d tensor $$\tilde{A}$$. The $$\lambda$$ we added to
$$V$$ and $$\vec{A}$$ into a 4-D tensor called $$\Lambda$$. And $$d_{\mu}$$ is
a 4-dimensional operator that take the time derivative of the first
dimensional and the spatial derivatives of the other three dimensions.
If you've studied spacetime, you're starting to see this all hang
togther. )


And what we did was use a condition that constrained the gauge, such as 

Coulomb gauge:

$$
\nabla \cdot \vec{A} = 0
$$

Lorenz gauge:

$$
\nabla \cdot \vec{A} = \mu_0\epsilon_0\frac{\partial V}{\partial t}
$$

It turns out neither of these conditions even fully specifies $$V$$ or $$\vec{A}$$.

"For the Coulomb gauge condition we need 

$$0 = \nabla\cdot\vec{A'} = \nabla\cdot(\vec{A} + \nabla\lambda) = \nabla\cdot\vec{A} + \nabla^2\lambda.$$

That's Poisson's equation which can be solved for $$\lambda$$ with Green's functions.
The Lorenz case is easier if you use four-vectors, in which case you get a 3+1 dimensional version of Poisson's equation."

## Today: The deferred potential (and a hint on the boundary matching problem
on the homework)

The following V and A satisfy the inhomogenous wave equation (which is the fancy
name for the one with the d'Alembertian's in it).  I'm going to assert that it's
a solution. Griffith's proves it on page 446.  Notice that he doesn't actually
derive it, but rather just proves that this is a solution.

$$
V(\vec{r}, t) = \frac{1}{4\pi\epsilon_0}\int\frac{\rho(\vec{r}^\prime, t_d)}{\mathscr{r}}d\tau^\prime
$$

$$
\vec{A}(\vec{r}, t) = \frac{\mu_0}{4\pi}\int\frac{\vec{J}(\vec{r}^\prime, t_d)}{\mathscr{r}}d\tau^\prime
$$

The t's ($$t$$ and $$t_d$$) are not the same t's.  The $$t$$ on the left is the
normal t.  It's the "I would like to know the value of the potential at the 
time $$t$$ t".  The one on the right is called the deferred time. It's deferred
in that it's evaluated at some earlier time. (It could be called the former time.)

What does the deferred time correspond to?  

$$
t_d = t - \frac{\mathscr{r}}{c}
$$

So if you've got some charges moving around here (draw a picture), 
and you are over here, and you
want to find the potential now, you have to know what the charges were doing
a certain amount of time ago.  The amount of time is how long it takes a signal
to travel from the moving charges to you.  It's the light-travel time from
the charges to the place you're evaluating the potential.

When you're doing the integral, all the different pieces of charge or current
have different distances from the place you're evaluating the potential.  
It's like looking at the night sky.  You have a deferred view of the night
sky.  You're looking at it as it was some time in the past.  How much time
in the past depends upon how far away the thing you're looking at is.

Incidentally, these potentials are called the deferred potentials. 

### Example 10.2
This example is in the book.

An infinite straight wire carries the current:

$$
I(t) = 0 {\rm ~for~} t\le 0
$$

$$
I(t) = I_0 {\rm ~for~} t>0
$$

That is, a constant current $$I_0$$ is turned on abruptly at $$t=0$$.  Find the
resulting electric and magnetic fields.

Since this one is in the book, don't look at the book.  
Talk about what you expect E and B
to be in the end. You know what they look like in the static case. What
will they look like in the dynamic case where the wire gets turned on?

My specific three questions:
* Will there be an E-field (at the beginning? for very long times?)? 
* What should the B-field  be at long times?
* What's a way to think about the deferred time in this case?  

Answers to above:
* There will be an E-field because B is changing. That's a difference from
the static case. At long times there should be no E-field.
* The B-field should be $$\mu_0I_0/2\pi s$$ at long times.
* The only thing that changes in time is how much of the wire the current
is running in at the deferred time.  For example, if we're one light-second
away from the wire, and the current was only turned on half a second ago,
the vector potential at our location is still zero.  If it was turned on
two seconds ago, then only some of the wire has the current in it.  The parts
of the wire that are farther away from us than 2 light seconds are still off 
(according to us.) 

Solution:
The scalar potential is zero because the wire is neutral.

We put the wire along the z-axis.  
The general formula for the vector potential is:

$$
\vec{A}(\vec{r}, t) = \frac{\mu_0}{4\pi}\int\frac{\vec{J}(\vec{r}^\prime, t_d)}{\mathscr{r}}d\tau^\prime
$$

We don't have J we have I.  J times an area is a current.  So basically we
just integrated over the area first, and we just have to integrate
over the length of the current.

$$
\vec{A}(\vec{r}, t) = \frac{\mu_0}{4\pi}\int_{-\infty}^\infty\frac{I(t_d)}{\mathscr{r}}dz^\prime
$$

The situation has cylindrical symmetry, so let's find A as a function
of the cylindrical coordinate $$s$$ and time $$t$$.

$$
\vec{A}(\vec{r}, s) = \frac{\mu_0}{4\pi}\hat{z}\int_{-\infty}^\infty\frac{I(t_d)}{\mathscr{r}}dz^\prime
$$

So now this is fun...how do we get the deferred time in here?    $$I$$
depends upon time, but it sort of doesn't.  It's not a nice function
of time so we can't just replace $$t$$ with $$t - \frac{\mathscr{r}}{c}$$
in the equation for I.  (We could, by the way do that, if I was a nice
function of time.)

Take a stab at
writing down the scalar and vector deferred potentials for this source.  
Everyone put the wire (it's infinite) along the z-axis so that our
solutions look kind of the same. 

How much of the wire is on?
The part where:

$$
d^2 \le (ct)^2
$$

$$
z^2 + s^2 \le (ct)^2
$$

$$
|z| \le \sqrt{(ct)^2 - s^2}
$$

So then our integral should only go from/to $$\mp z$$.

$$
\vec{A}(\vec{r}, s) = \frac{\mu_0I_0}{4\pi}\hat{z}\int_{-\sqrt{(ct)^2 - s^2}}^{\sqrt{(ct)^2 - s^2}}\frac{dz^\prime}{\sqrt{s^2 + {z^\prime}^2}}
$$

I put in the distance from $$s$$ to the source $$\sqrt{s^2 + z^2}$$ for $$\mathscr{r}$$.

After you do the integral you get:

$$
\vec{A}(\vec{r}, s) = \frac{\mu_0I_0}{2\pi}\ln\left(\frac{ct + \sqrt{(ct)^2 - s^2}}{s}\right)\hat{z}
$$

Then the electric field is:

$$
\vec{E}(s,t) = -\frac{\partial \vec{A}}{\partial t} = -\frac{\mu_0 I_0 c}{2\pi\sqrt{(ct)^2 - s^2}}\hat{z}
$$

And the electric field is:

$$
\vec{B}(s,t) = \nabla \times \vec{A} = \frac{\mu_0 I_0}{2\pi s} \frac{ct}{\sqrt{(ct)^2 - s^2}}\hat{\phi}
$$

Does it satisfy our criteria?  (long times in particular, $$t-> \infty$$ makes
E go to zero and B go to the familiary result.)

## An example that's not in the book
This is actually your first homework problem. Let's start it.

Griffiths 10.12. 
