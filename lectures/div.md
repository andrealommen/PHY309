---
layout: page
title:  "Divergence Theorem (Green's Theorem, Gauss's Theorem)"
permalink: "/lectures/div"
---

Here's the divergence theorem.  It's mathematical, and can be applied to physics, but I think it's important to realize that it's math.

$$
\int_V (\nabla \cdot \vec{v})d\tau = \oint_S \vec{v}\cdot d\vec{a}
$$

Like all three of the calculus theorems (grad, div, curl) the thing on the right has one fewer dimension than the thing on the left.

Griffiths has an explanation of faucets that you should read, but I don't quite understand it, so you should explain it to me if you get it. The gist is that the left-hand integral is the sum over the faucets, and the right-hand integral is the total flow out through the surface.  That makes sense to me (that the more faucets you have, the more water you'll get flowing) but I want to understand it as a purely mathematical concept.  In all cases, I would be pleased to hear the ways you reconcile the divergence theorem for yourself.

By way of reconciling it for ourselves, let's do the example 1.10 on page 32. The example makes it pretty clear that it's a mathematical theorem, and that you could repeat the exercise for any function you can think of, and it would still be true!! 

How are we going to use this?  Very important question. I'm glad you asked.  We will use this to get from Maxwell's equation for Electric fields (which you may have seen before):

$$
\nabla \cdot \vec{E} = \frac{1}{\epsilon_0} \rho
$$

to Gauss's law (actually both the equations above and below are called Gauss's law), which I know you've seen before, but you may not yet love it as much as you're going to.

$$
\oint \vec{E}\cdot d\vec{a} = \frac{1}{\epsilon_0}Q_{enc}
$$

You can already see it, right?   If you start from $$\nabla \cdot \vec{E} = \frac{1}{\epsilon_0} \rho$$ and interate both sides over the whole volume, the right side turns into $$Q_{enc}$$ and the left side turns into $$\oint \vec{E}\cdot d\vec{a}$$ by the divergence theorem.



