---
layout: page
title:  "Gradient Theorem (Fundamental Theorem for Gradients)"
permalink: "/lectures/grad"
---

The fundamental theorem for gradients is:

$$
\int_a^b (\nabla T)\cdot d\vec{l} = T(\vec{b}) - T(\vec{a})
$$

Griffiths makes the point that all of the fundamental theorems are
analogous to the fundamental theorem of calculus

$$
\int_a^b \left(\frac{df}{dx}\right)dx= f(b) - f(a)
$$

or

$$
\int_a^b F(x)dx= f(b) - f(a)
$$

where F is the derivative of f.  (Even though those two are the same
thing, I agree with Griffiths that it's easier to see it in the 2nd one.)

The fundamental theorem for gradients is definitely the most similar
this. In fact, it's really just the three-dimensional vector version of it.
In my brain, I do think of the gradient as the derivative.  I know I'm
suppose to think of the divergence and the curl as derivatives, too, 
but the gradient to me is the simple derivative.  It's simply the slope
with the vector pointing in the direction of largest slope.

So when you're walking around you can see the gradient of the surface on
which you're walking.  You can see at what points it's greater than others, and you can estimate its direction.

**The closed-line integral of the gradient of any function is zero.**

$$
\oint (\nabla T)\cdot d\vec{l} = 0
$$

Another kind of silly way of writing this is:

$$
\int_a^a (\nabla T)\cdot d\vec{l} = T(\vec{a}) - T(\vec{a}) = 0
$$

In other words, when you look at the right side of the equation, you'll notice
that for any closed-loop, i.e. one that starts and stops at the same place,
the right side is the difference between two things that are the same. We'll see this again in Stokes' theorem, by the way.

Since it's fun to think about the gradient when you're walking around,
let's think about what $$\oint (\nabla T)\cdot d\vec{l} = 0$$ means when
you're walking around. It means that if you start at a particular place on
campus, and walk around for 20 minutes and come back to the same point, you will
have gone up some of the time, and down some of the time, but if you are
coming back to the same point, you must've gone up the same amount as you
went down, and your total change in elevation must be zero.

