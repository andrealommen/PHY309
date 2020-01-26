---
layout: page
title:  "The Dirac Delta Function"
permalink: "/lectures/dirac"
---

Griffiths goes into some background on the Dirac delta function. I think I just want to tell you
how to deal with it.

* First, condition yourself so that when you come to an integral with a delta function in it
you say "Phew, that'll make this easy" rather "Oh crap."  It will actually make your life easier.
* Second, recognize that delta functions are only useful (and very useful) inside integrals. Outside of integrals they're just terribly designed functions.

The basic thing that you need to know is Griffiths 1.92:

$$
\int_{-\infty}^\infty f(x) \delta(x-a) dx = f(a)
$$

The $$\delta(x-a)$$ in the integral tells you "Pretend the integral and the delta function
aren't there, and just evaluate $$f(x)$$ at a."

Sometimes the integral looks more like this:

$$
\int_{-\infty}^\infty f(x) \delta(x) dx
$$

which is really just the same as above with $$a=0$$, so therefore..

$$
\int_{-\infty}^\infty f(x) \delta(x) dx = f(0)
$$

The three-dimensional delta function is very similar

$$
\int_{\rm all space} f(\vec{r}) \delta(\vec{r}-\vec{a}) d\tau = f(\vec{a})
$$

The $$\delta(\vec{r}-\vec{a})$$ in the integral tells you "Pretend the integral and the 
delta function
aren't there, and just evaluate $$f(\vec{r})$$ at $$\vec{a}$$."

Let me give you an example of something that could make you say "Phew!"  Let's say you're
doing a problem and you end up with this integral:

$$
\int_{-\infty}^\infty \Sigma_{l=0}^{47} Y_l^0(\theta, \phi) \delta(\theta-\pi/17, \phi-\pi/42) d\theta d\phi
$$

Will you panic?  Well, maybe at first, but then you'll realize the problem is basically
done for you.  You pretend the integral isn't there and the delta function isn't there
and you evaluate that dumb sum of spherical harmonics that I invented at $$\theta=\pi/17, \phi=\pi/42$$.

$$
\int_{-\infty}^\infty \Sigma_{l=0}^{47} Y_l^0(\theta, \phi) \delta(\theta-\pi/17, \phi-\pi/42) d\theta d\phi=
\Sigma_{l=0}^{47} Y_l^0(\pi/17, \pi/42) 
$$

Two super important things that I just want you to remember (or maybe remember they're here) are that:

$$
\nabla^2\frac{1}{\mathbb{r}} = -4\pi\delta^3(\mathbb{r})
$$

and

$$
\nabla\cdot\frac{\vec{\mathbb{r}}}{\mathbb{r}^2} = 4\pi\delta^3(\vec{\mathbb{r}})
$$

These will become really important when we start applying these various derivatives to
charge distributions that include point sources!

($$\mathbb{r}$$ is what I'm currently using for Griffith's script "r" until I figure out
a way to import mathcalligra into the markdown interpreter that is rendering this page!)
