---
layout: page
title:  "Polarization"
permalink: "lectures/polarization"
---

Announcements:  
* Talks Tuesday and Wednesday by candidates for next year, 4pm.
Tuesday evening there's a reception for all of you.
* No Walter/Feynman notion on problem sets.

You've actually learned all the ways to deal with static distributions of charges.  Now we have to deal with the fields in matter.

This is the chapter where we go from Electric fields to Displacement Field,
which is the more general field.

I mentioned that dipoles would figure prominently in this chapter. It happens right away. And my example of an atom with a dipole moment comes up immediately.
This chapter is about electric fields in matter (that's what the chapter is
called.) So immediately if you put an atom in an electric field, the positive
part of the atom is forced in the direction of the electric field, 
and the negative part of the atom is forced in the opposite direction. 
Different atoms are able to **polarize** by different amounts depending
upon their electronic configuration. Their *atomic polarizability* is designated
by $$\alpha$$ and is the constant of proportionality between the applied
electric field $$\vec{E}$$ and the dipole moment $$\vec{p}$$.

$$
\vec{p} = \alpha \vec{E}
$$

Your book (top of page 168) lists some $$\alpha$$'s.  They range from
almost 1 for Hydrogen to almost 60 for Cesium.

Because of the opposite forces on the positive and negative side of
the atom, or dipole, there's a torque on the dipole:

$$
\vec{N} = \vec{p} \times \vec{E}
$$

The above is the torque on a dipole $$\vec{p}$$ in a uniform field $$\vec{E}$$.
Griffiths derives that handily, in case you'd like to see that.
The effect of the torque is to align the dipole with the electric field
in which case we say the material is *polarized*. We'll get to that in a 
second.

There's also a force on the dipole:
$$
\vec{F} = (\vec{p} \cdot \nabla) \vec{E}.
$$

And the energy of a dipole in an electric field....

What do you think?  By the $$\vec{N}$$ above it should have a lot of energy
if the dipole and electric field are anti aligned, and none if they're
aligned.

$$
U = - \vec{p} \cdot \vec{E}
$$

Does that work?  If they're aligned the dot product is a maximum and $$U$$
is a minimum.  If they're anti-aligned the dot product is a minimum and
$$U$$ is  maximum.  Yes!

## Polarization
A material is said to be polarized if its atoms are roughly lined up. 
Polarization $$\vec{P}$$ is defined as

$$
\vec{P} = {\rm dipole~moment~per~unit~volume}
$$

## The field of a polarized object
(First we deal with the field from this object by itself, then in the next
section we'll add the applied field to the induced field and get the total
field.)

So how do you get the field of this polarizaed object?   It's a whole
bunch of little dipoles pointing all in roughly the same direction. 

Imagine a volume of dipoles, all lined up.  The stuff in the middle
won't give you much field, because right next to any positive charge
is a negative charge, so that won't have much bulk effect. But at any
edge you'll get a whole bunch of one sign of charge hanging out along the
edge, as long as that edge is normal to the direction of the polarization.
You can write this as an effective surface charge on the material like
this:

$$
\sigma_b \equiv \vec{P}\cdot\vec{n}
$$

where $$\vec{n}$$ is the normal to the surface.   So if $$\vec{P}$$ and
$$\vec{n}$$ are parallel, you get a lot of effective charge there.
Officially the "b" stands for bound charge, to indicate it can't be removed.
And Griffiths argues that it's real charge. I agree it's a real charge
excess on the surface. I just like to acknowledge that there's charge
all the way through the material.  This just happens to be the charge
we care about because it doesn't have an opposite charge on both
sides of it.  

Similarly:

$$
\rho_b \equiv -\nabla \cdot \vec{P}
$$

so notice that $$\vec{P}$$ has to have a divergence in order for
there to be an effective (bound) charge density. (Sketch a small
circle of negative charges surrounded by a larger circle of positive
charges.) That's the situation (i.e. spherical symmetry) in which a polarization
would give you a bound volume charge density.

Assuming the handwaivey-ness is not totally satisfying, let's actually
see how these $$\sigma_b$$ and $$\rho_b$$ pop out of the integral when
we actually rigorously calculate the field of the polarized material.

For a single dipole:

$$
V(\vec{r}) = \frac{1}{4\pi\epsilon_0} \frac{\vec{p}\cdot\vec{\mathscr{r}}}{\mathscr{r}^2}
$$

where $$\vec{\mathscr{r}}$$ is the vector from the dipole to the point where we
want to calculate the potential.

Instead of one dipole $$p$$ we have a zillion dipoles spread through
the volume and the polarization $$P$$ describes the dipole moment
per volume.  Whenever you have a zillion of anything you need an integral.
So if we integrate $$P$$ over the volume we can use the same formula:

$$
V(\vec{r}) = \frac{1}{4\pi\epsilon_0} \int_{\mathscr{V}}\frac{\vec{P}(\vec{r}^\prime)\cdot\vec{\mathscr{r}}}{\mathscr{r}^2} d\tau^\prime
$$

Remember we're only integrating over $$r^\prime$$ but $$\mathscr{r}$$ depends
upon $$r^\prime$$ so this is a pretty irritating integral.

We can recast it using:

$$
\nabla^\prime\left(\frac{1}{\mathscr{r}}\right) = \frac{\hat{\mathscr{r}}}{\mathscr{r}^2}
$$

(The above formula you can get by remembering $$\vec{\mathscr{r}} = \vec{r} - \vec{r}^\prime$$  and using the chain rule to take the gradient.)

Putting that into our integral we have:

$$
V = \frac{1}{4\pi\epsilon_0} \int_\mathscr{V} \vec{P}\cdot \nabla^\prime\left(\frac{1}{\mathscr{r}}\right) d\tau^\prime
$$

Then you can use one of the vector identities (#5) in the front of your book (Notice
the identity below is just a vector chain rule, and what we're about to do is analogous
to integration by parts!):

$$
\nabla\cdot(f\vec{A}) = f(\nabla \cdot \vec{A}) + \vec{A} \cdot (\nabla f)
$$

Which we rewrite as:

$$
\vec{A} \cdot (\nabla f) = \nabla\cdot(f\vec{A}) - f(\nabla \cdot \vec{A}) 
$$

In our case $$P$$ is $$A$$ and $$f$$ is $$1/\mathscr{r}$$ so we have:

$$
\vec{P} \cdot \nabla \left(\frac{1}{\mathscr{r}}\right) = \nabla\cdot(\frac{1}{\mathscr{r}}\vec{P}) - \frac{1}{\mathscr{r}}(\nabla \cdot \vec{P}) 
$$

Do you see that divergence of $$\vec{P}$$ emerge??  It just happened!!!

So now we put that into our equation for $$V$$ and we have: 

$$
V = \frac{1}{4\pi\epsilon_0} \left[\int_\mathscr{V} \nabla^\prime\cdot\left(\frac{\vec{P}}{\mathscr{r}}\right) d\tau^\prime - \int_\mathscr{V} \frac{1}{\mathscr{r}}(\nabla^\prime \cdot\vec{P}) d\tau^\prime\right]
$$

Keeping in mind that we said we were going to get a surface term and a volume term, and you
see the volume term emerging, how do I get that first term to look like a surface term??

Ans: The Divergence Theorem.

$$
V = \frac{1}{4\pi\epsilon_0} \oint_\mathscr{S} \frac{1}{\mathscr{r}}\vec{P}\cdot d\vec{a}^\prime  - \frac{1}{4\pi\epsilon_0} \int_\mathscr{V} \frac{1}{\mathscr{r}}(\nabla^\prime \cdot\vec{P}) d\tau^\prime
$$

If we say that $$\vec{P}\cdot \hat{n}$$ is a surface charge, that 
the first term looks like the potential of surface charge.

$$
\sigma_b \equiv \vec{P}\cdot\hat{n}
$$

The second term  similarly, if we make the following definition...

$$
\rho_b \equiv -\nabla\cdot\vec{P}
$$

looks the potential of a volume charge.  And then we can rewrite...

$$
V = \frac{1}{4\pi\epsilon_0} \oint_\mathscr{S} \frac{\sigma_b}{\mathscr{r}}da^\prime  + \frac{1}{4\pi\epsilon_0} \int_\mathscr{V} \frac{\rho_b}{\mathscr{r}} d\tau^\prime
$$

