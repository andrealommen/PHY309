---
layout: page
title:  "The Potential Formulation"
permalink: "/lectures/potentialformulation"
---

### This week 
* Then we need to go back to potentials, particularly vector potentials, so that we can understand deferred potentials, so that we can understand how radiation occurs. (We've talked about electromagnetic waves, but you'll notice we haven't talked about how we generate them at all. We
ve just assumed they're there and tried to understand their properties. In this very last section of the course, we need to generate them.

### What we did last time. 

### Dispersion
The phase velocity of a single wave is

$$
v = \frac{\omega}{k}
$$


A packet of waves travels at the group velocity

$$
v_g = \frac{d\omega}{dk}
$$

So if you know the so-called `dispersion relation' (the relationship between 
$$\omega$$ and $$k$$) you can find the velocity of the wave.

Then we figured it out for a plasma.
A plasma is really just a gas of electrons and positrons.  We considered
a collisionless plasma.  Plasmas are conductors and we figured out the
conductivity by making some basic arguments about the relationship between
the velocity of the electrons and the applied electric field (which in this
case is the electric field component of the EM wave).  

$$
\sigma = \frac{ie^2n_0}{\omega m_e}
$$

And again, it's imaginary because the velocity is out of phase with the E.
(The imaginary part came from integrating $$e^{i\omega t}$$, which we did
to get the velocity, because the derivative of the velocity was the force
which is proportional to $$E$$ which had and $$e^{i\omega t}$$ in it because
it's an EM wave.)

$$
k^2 = \mu_0\epsilon_0\omega^2\left(1 + \frac{i\sigma}{\epsilon_0\omega}\right)
$$

Using the expression above for $$k$$ and the formula for group velocity, and
a new definition of the plasma frequency we got:

$$
v_g = \frac{c}{\sqrt{1 + \frac{\omega_p^2}{\omega^2 - \omega_p^2}}}
$$

And we noted that waves above the plasma frequency can propagate forever, but at
velocities that depend on $$\omega$$.  Waves below the plasma frequency
don't propagate.  (At the plasma frequency they have 0 velocity.)


### Chapter 10
**The potential formulation**
Now we want the **general** solution to these laws.  In the static case, we got
Coulomb's law (for E-fields) and the Bio-Savart law (for B-fields).
But that was when we assumed all the time-derivatives were zero.  We don't
have that anymore, and now we want the general solution.

Here are the steps of the lecture.

1. **We messed up our ability to express E and B as potentials**<br>
It really helps to be able to express E and B as potentials, but we temporarily messed up
our ability to write potentials when we made E no-longer curl-free.  

2. **We fix it**<br>
We make E the negative gradient of the potential minus the time
derivative of the vector potential.  Then everything is okay again.

3. **Gauge transformations**<br>
We can add the gradient of any scalar to A as long as we subtract the time derivative
of the same scalar from V. (You've been doing this already when you set
potential to zero at infinity. We just didn't call that a gauge transformation then.)

4. **Lorenz gauge**<br>
We introduct the gauge we'll be in for the rest of the semester.

### Start with Maxwell's equations

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

First let's deal with that fact that the curl of E is no longer 0, so can
we still somehow write it as the gradient of something?  Sort of...

B is still divergenceless so we still have

$$
\vec{B} = \nabla \times \vec{A}
$$

Put this into Faraday's law and we get

$$
\nabla \times \vec{E} = -\frac{\partial}{\partial t}(\nabla \times \vec{A})
$$

$$
\nabla \times \left(\vec{E} +\frac{\partial\vec{A}}{\partial t}\right) = 0
$$

So that quantity on the left in parentheses is indeed curl-free, and we
can express it as the gradient of a scalar V.

$$
\vec{E} +\frac{\partial\vec{A}}{\partial t} = -\nabla V.
$$

So then

$$
\vec{E} = - \nabla V - \frac{\partial\vec{A}}{\partial t} 
$$

** Yay we fixed it!! **

Notice that this reduces to the familiar form when $$\vec{A}$$ is constant.

This automatically fulfills the two homogenous Maxwell equations (they don't
depend upon $$\rho$$ or $$\vec{J}$$).

How about Gauss's law?  Put our equation for E into Gauss's law.

$$
\nabla \cdot \vec{E} = - \frac{1}{\epsilon_0} \rho
$$

$$
\nabla^2 V  +\frac{\partial}{\partial t}(\nabla \cdot \vec{A}) = -\frac{1}{\epsilon_0} \rho
$$

This replaces Poisson's equation (which you'll notice it reduces to in the static case).

Now we can get all the E's and B's out of Ampere's law:

$$
\nabla \times (\nabla \times \vec{A}) 
 = \mu_0 \vec{J}
+ \mu_0 \epsilon_0 \nabla \left(\frac{\partial V}{\partial t}\right) - \mu_0 \epsilon_0 \frac{\partial^2 \vec{A}}{\partial t^2 }
$$

Now use the vector identity

$$
\nabla \times (\nabla \times \vec{A}) = \nabla(\nabla \cdot \vec{A}) - \nabla^2\vec{A}
$$

to arrange it into:

On the left:

* a term that looks like the wave equation (del-squared of something, minus
two time derivatives of that same thing) 
* a term that is the gradient of something

On the right:
* the current density

Ans:

$$
\left(\nabla^2\vec{A} - \mu_0 \epsilon_0 \frac{\partial^2 \vec{A}}{\partial t^2 }\right)
- \nabla\left(\nabla\cdot\vec{A} + \mu_0\epsilon_0\frac{\partial V}{\partial t}\right) = -\mu_0\vec{J}
$$

That equation and the modified Poisson's equation contain all the information
in Maxwell's equations.

### Gauge Transformations (10.1.2)

Just as before, our two new equations do not uniquely determine the potentials.  We
can add things to V and $$\vec{A}$$ as long as they don't change E and B.  That's
called "gauge freedom".

Griffiths does a nice simple derivation of this (pg 339 and 340) but I will
tell you the answer.
To A we can the gradient of any scalar $$\lambda$$ as long as we subtract the
time-derivative of that same scalar from $$V$$.

$$
\vec{A}^\prime = \vec{A} +\nabla \lambda
$$

$$
V^\prime = V - \frac{\partial \lambda}{\partial t}
$$

Since the thing you're adding to $$\vec{A}$$ is the gradient of something, it's curl
is zero, so you know you'll get the same B.

And if you plug those into this equation:

$$
\vec{E} = - \nabla V - \frac{\partial\vec{A}}{\partial t} 
$$

You'll see that on the right you get the gradient of the time derivative of $$\lambda$$
minus the time derivative of the gradient of $$\lambda$$ which gives you
the same E you had before.

### Why do we like gauge transformations?  
Because they let us adjust the problem to being an easier one.

The two most famous ones or the Coulomb Gauge and the Lorenz Gauge.

### The Coulomb Gauge

We pick 

$$
\nabla \cdot \vec{A} = 0
$$

Does it mean the magnetic field is zero?  No.  It just means the divergence of
A is zero.  In fact it means we're sort of back in a magnetostatics situation. 
Watch this:

Once we put in our new formula for E:

$$
\vec{E} = - \nabla V - \frac{\partial\vec{A}}{\partial t} 
$$

we had this:

$$
\nabla^2 V  +\frac{\partial}{\partial t}(\nabla \cdot \vec{A}) = -\frac{1}{\epsilon_0} \rho
$$

but now that we have $$\nabla \cdot \vec{A} = 0$$ we have:

$$
\nabla^2 V = -\frac{1}{\epsilon}\rho
$$

We got back our familiar Poisson's equation!

And then we can use all our favorite formulas for potential such as:

$$
V(\vec{r},t) = \frac{1}{4\pi\epsilon_0}\int\frac{\rho(\vec{r}^\prime, t)}{\mathscr{r}}d\tau^\prime
$$

At first this seems great, but then you realize it's weird.  Talk with
your groups for a minute and see if you can figure out why it's weird.  Also
compile any questions you have about gauge transformations. 

Ans: It's weird because the potential for somebody else - many miles away, is
the same as the potential for you here.  So if you move your charge, their potential
will change instantaneously.  Does that violate causality?

No, because their field won't change.  The E-field is

$$
\vec{E} = -\nabla V - \left(\frac{\partial\vec{A}}{\partial t}\right)
$$

so A must encode all the information about the change. It does, and it's a pain.  
The simplicity of calculating V in the Coulomb gauge is compensated for by
the complexity of calculating A.  I'm not gonna write down the equation for A.
It's Griffiths 10.11.

(It's not obvious that the Coulomb gauge meets our criteria:
"To A we can the gradient of any scalar $$\lambda$$ as long as we subtract the
time-derivative of that same scalar from $$V$$.''  There's a note about that 
at the bottom of this lecture. What's important is that
the gauge criterion $$\nabla\cdot \vec{A}=0$$ sets a relationship between
A and V.)

### The Lorenz gauge

Here we pick

$$
\nabla \cdot \vec{A} = \mu_0\epsilon_0\frac{\partial V}{\partial t}
$$

If you do that you get rid of the middle term in the equation I had you rearrange
above

$$
\left(\nabla^2\vec{A} - \mu_0 \epsilon_0 \frac{\partial^2 \vec{A}}{\partial t^2 }\right)
- \nabla\left(\nabla\cdot\vec{A} + \mu_0\epsilon_0\frac{\partial V}{\partial t}\right) = -\mu_0\vec{J}
$$

So now it's:

$$
\left(\nabla^2\vec{A} - \mu_0 \epsilon_0 \frac{\partial^2 \vec{A}}{\partial t^2 }\right)
= -\mu_0\vec{J}
$$

That operator on the left has a name:

$$
\nabla^2 - \mu_0 \epsilon_0 \frac{\partial^2 }{\partial t^2 } = \square^2
$$

It's called the d'Alembertian.

The equation for V becomes similarly simpler and you get.
In the Lorenz gauge you can write our final two equation as:

$$
\square^2V = -\frac{1}{\epsilon_0}\rho
$$

$$
\square^2\vec{A} = -\mu_0\vec{J}
$$

The d'Alembertian is a natural generalization of the Laplacian.  
Both V and A satisfy the wave equation.
The wave equation

$$
\square^2f = 0
$$

So the
equations above can be regarded as 4-D versions of Poisson's equations. 

We will use the Lorenz gauge from now on.

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
