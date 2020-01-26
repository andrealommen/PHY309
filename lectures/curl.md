---
layout: page
title:  "Curl Theorem (Stokes' Theorem)"
permalink: "/lectures/curl"
---

The fundamental theorem for curls, which almost always gets called Stokes' theorem is:

$$
\int_S (\nabla \times \vec{v})\cdot d\vec{a} = \oint_P \vec{v} \cdot d\vec{l}
$$

Like all three of the calculus theorems (grad, div, curl) the thing on the right has one fewer dimension than the thing on the left, and the derivative is on the left.

In this case the higher-dimension integral is over a $$S$$urface, and the lower-dimensional integral is over the $$P$$erimeter of the surface.

Griffiths has a wonderful geometrical explanation of this (page 34) which I will put into my own words.  The curl measures how much something is swirling around. You can also get a sense of swirliness by measuring how much the vector is pointing _along_ the boundary.  So, let's say you're measuring the velocity every where inside a tornado.  Velocity is the vector we're considering.  You take a slide of the tornado, calculate the curl over that area, and integrate the curl over the area.  That integral will be equal to the integral of the velocity parallel to the outside edge of the tornado.

I think it's kind of amazing that those are always exactly equal.  I will admit that it makes sense to me that they should be proportional, but equal seems a little bit like magic.  The proportionality makes sense because imagine you can conduct the same measurements of the tornado as its slowing down. As the tornado slows down, the curl will get smaller, and the line integral around the edge will get smaller. Eventually when the tornado had dissipated, both sides will be zero.

How are we going to use this?  Good question!  Stokes theorem will let us transform Ampere's law into something useful (which we usually also call Ampere's Law because they're physically identically).

Here's Maxwell's version of Ampere's law

$$
\nabla \times \vec{B} = \mu_0\vec{J}+\mu_0\epsilon_0\frac{d\vec{E}}{dt}
$$

by "Maxwell's version" I mean "the one that's not very useful, but is most general."

The version I usually call Stokes law results after you apply 
Stokes Theorem (the 
curl theorem) to the above. Can you see how that shakes out? First you integrate
over both sides (just like we did to get what I call Gauss's Law).  By Stokes
theorem $$\int\nabla \times \vec{B}$$ becomes $$\oint_P \vec{B} \cdot d\vec{l}$$
and $$\int \mu_0\vec{J}$$ becomes $$\mu_0 I_{\rm enclosed}$$.  I don't 
actually want to talk about the 2nd term on the right side right now, but
you can tell that for all static cases (where the $$E$$-field isn't changing)
it goes away.  And you get:

$$
\oint_P \vec{B} \cdot d\vec{l} = \mu_0 I_{\rm enclosed}
$$


Stokes Theorem is a mathematical theorem, so as long as you can write
down the function, the theorem applies. 
Notice Stokes' Theorem (unlike the Divergence Theorem) applies to an open surface, not a closed one. (I'm going to show you a bubble wand when
I talk about this, hopefully.)  The integral is over the area of a surface
that does not enclose anything.   The area has to have a perimeter (a place
where it's open) or the theorem isn't very useful.  Interestingly, it 
_is_ useful
in the following way. By Stokes Theorem the integral of a curl over any closed 
surface is zero.  There are two ways to see this:

* A closed surface is the same as a surface whose perimeter is so small it
doesn't exist.  So the closed-line integral on the right-side of Stokes' Theorem
is zero because the length of the perimeter is zero. (In this case think of
the bubble wand with a HUGE bubble coming out of it. If the bubble is so big
compared to the wand that the perimeter is essentially a point, and the bubble
is essentially a complete sphere, that's the the case we're talking about.)
* You can think of a closed surface (a sphere for example) as two open surfaces (two hemi-spheres for example each bounded by the same circle with the radius
as the sphere). You can apply Stokes' theorem twice in that case, once to the 
upper hemisphere and once to the lower hemisphere.  The integral of the curl
over the whole surface will be the sum of the two line integrals, one around the perimeter in one direction, and one around the perimeter in the other direction. Those two line-integrals will be equal and opposite, and the sum of them
will be zero.  Therefore the integral of the curl over the closed sphere will
be zero.
* _Note that the direction the area vector points on the left-hand side of
Stokes Law is determined by the direction in which the line-integral on the
right-hand side goes.  They are related by the right-hand rule._

**Question from class about cylinder open at both ends**

On Friday there was a question about whether
Stokes law is applicable in the case where you have a cylinder with both 
ends open, i.e. two boundaries.

**Does Stokes' Theorem apply to a cylinder open at both ends?**
No, the right-hand line-integral must be a closed-line integral, i.e. the line has to be continuous and it has to stop where it started.  To draw the perimeter
of the open cylinder, you have to "pick up your pencil" so the integral over
the perimeter doesn't count as a closed-line integral.

However, I think you can do a trick. Let's make your open cylinder into
two surfaces, two cylinders that are both only open at one end. Their closed
ends are face-to-face in the middle of the original open cylinder.  Arrange
the $$d\vec{a}$$ for the bottom surface so that it points up, and arrange
the $$d\vec{a}$$ for the top surface so that it points down (recall you can do
this by the direction in which you do the line-integral).  Then there's one
part of the surface integral that the two cylinders have in common, and the
$$d\vec{a}$$ for each is pointing in opposite directions, so the integral
over that part of the surface will cancel out. 

So that means we can write a Stokes-ish Law for our open cylinder that
would look something like this:

$$
\int_S (\nabla \times \vec{v})\cdot d\vec{a} = \oint^{top~part}_{P(pointing~down)} \vec{v} \cdot d\vec{l} +  \oint^{bottom~part}_{P(pointing~up)} \vec{v} \cdot d\vec{l}
$$

where $$d\vec{a}$$ points out of the cylinder everywhere.


