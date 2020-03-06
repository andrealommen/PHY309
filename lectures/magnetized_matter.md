---
layout: page
title:  "Magnetic Fields in Matter"
permalink: "/lectures/magnetized_matter"
---

It may be useful to review magnetic dipoles which I wasn't able to include in my chapter 5
lectures, but which I included at the end of the [crash course for Chapter 5](chapt5).

Review of torque on a dipole:

$$
\vec{N} = \vec{m}\times\vec{B}
$$

Force on a dipole:

$$
\vec{F} = \nabla(\vec{m}\cdot \vec{B})
$$

Compare to it's electrical ``twin":
$$
\vec{F} = \nabla(\vec{p}\cdot \vec{E})
$$

### The "Gilbert" model:

You can do a lot of magnetostatic problems by using electrostatic results
and replacing:
* $$\vec{p}$$ with $$\vec{m}$$
* $$1/\epsilon_0$$ with $$\mu_0$$
* $$E$$ with $$B$$

Once you get really close-up to the dipole (where it looks like a ring
of current instead of a perfect magnetic dipole) then this breaks down.
Griffiths' advice is to use the Gilbert model to get intuition, but
don't rely on it for quantitative results.

### Paramagnetism

We saw in chapter 4 that an electric field can induce polarization
in individual atoms by sending all the electrons to one side and
all the nuclei to the other.  How would you guess a magnetic field
induces magnetism in an atom?  

There are actually (at least) two answers. The one you've probably heard of
more is that that a magnetic field can make the spins of an electron
align with the magnetic field (see the torque equation above, it's effect
is to align the dipole moment with the field).  

**Why does an electron spinning have a magnetic dipole moment?**  Well, it's
like a spinning sphere of charge.

The spin alignment with the magnetic field creates an additional magnetic
field in the same direction.   This is called paramagnetism.  Para in latin means
"defense, protection agains".  I'm not sure I would've called it that.

**What about the "current" of the electron going around the nucleus?**
(Spoiler alert/punchline. This gives you diamagnetism, where the magnetization
is opposite the applied field. Why???  That doesn't make any sense!!  It does
actually.  It turns out that it's hard to actually change the orientation of
an orbit, so the torque that happens in paramagnetism isn't the most
important thing.  The most important thing is the increase in velocity of
the electron.)

See if you can come up with what the magnetic dipole of an electron in an orbit would
be.
Ans: You can think of the electron's orbit as a current. Let's look at that!! Current
is charge per time, or linear current density times velocity. $$I = \lambda v = ev/2\pi R$$.  
And magnetic moment is Ia, where a is the area. 
The area is $$\pi R^2$$. So the magnetic moment of an electron orbit is....

In case you're bothered by that (because I told you magnetic fields
can't do work, so they can't speed a particle up).... A changing
magnetic field induces a electric field, and the electric field
can accelerate the electrons.

The argument goes like this...

Let's start without a magnetic field, just an electric field.  As
you know, a central $$1/r^2$$ force can give you an orbit.  To find
its radius you equate the force to $$mv^2/r$$.  I'm using $$v_e$$
in this equation to specify the velocity in the presence of the
Electric field only.

$$
\frac{1}{4\pi\epsilon_0} \frac{e^2}{R^2} = m_e\frac{v_e^2}{R}
$$

The thing on the left is the electric field of a point charge multiplied
by charge $$e$$.  (We're assuming there's an electron orbiting a proton).

To this expression we can add a magnetic field contribution:

Let's say the magnetic field is perpendicular to the plane of the orbit,
so v and B are always perpendicular to each other.

$$
\frac{1}{4\pi\epsilon_0} \frac{e^2}{R^2} + ev_BB= m_e\frac{v_B^2}{R}
$$

So how much faster is the electron going with the addition
of the magnetic field, i.e. how much larger is $$v_B$$ than $$v_e$$?
Subtract those two equations from each other...

$$
ev_BB = m_e\frac{v_e^2 - v_B^2}{R}
$$

$$
ev_BB = m_e\frac{(v_e - v_B)(v_e + v_B)}{R}
$$

As long as the difference is small (which it surely is.  Recall our
earlier discussion on how much small magnetic forces are than
electrical forces) we can approximate...

$$
ev_BB = m_e\frac{(\Delta v)(2v)}{R}
$$

$$
\Delta v = \frac{eRB}{2m_e}
$$

If the velocity changes by that much then the dipole moment changes by

$$
\Delta \vec{m} = -\frac{1}{2} e(\Delta v)R\hat{z} = -\frac{e^2R^2}{4m_e}\vec{B}
$$

Notice the change in $$\vec{m}$$ is opposite the direction of $$\vec{B}$$.
This is called diamagnetism.

### How does this produce an overall magnetic field in the materials?

Excellent question.  It's not obvious.  The atoms are all aligned
in different ways, so the bulk magnetization is zero.  When you
apply the magnetic field, this effect (above) adds a small magnetic
moment to most of them, **all in the same direction** so the
material becomes polarized.

### Magnetization

$$\vec{M}$$ is the magnetic dipole moment per unit volume (just like $$\vec{P}$$
is the electric dipole moment per unit volume.)

The vector potential due to some magnetized matter is:

$$
\vec{A}(\vec{r}) = \frac{\mu_0}{4\pi} \int \frac{\vec{M}(\vec{r}^\prime) \times \hat{\mathscr{r}}}
{\mathscr{r}^2} d\tau^\prime
$$

In a manner very similar to what we did for electric dipoles, we can
define a bound volume current and a bound surface current.

$$
\vec{J}_b = \nabla \times \vec{M}
$$

$$
\vec{K}_b = \vec{M} \times \hat{n}
$$

where $$\hat{n}$$ is the normal unit vector (normal to the surface.)

With those definitions:

$$
\vec{A}(\vec{r}) 
= \frac{\mu_0}{4\pi} \int_V \frac{\vec{J}_b(\vec{r}^\prime)}{\mathscr{r}} d\tau^\prime
+ \frac{\mu_0}{4\pi} \int_S \frac{\vec{K}_b(\vec{r}^\prime)}{\mathscr{r}} da^\prime
$$

### Should you be excited about using that equation to calculate the vector potential?

No. 

Why?  Because it's really laborious.  First you have to calculate J and K, and then
you have to integrate over each of them, and then you have to take the curl of the result.  Oi.

Mostly I would avoid
dealing with it if you can. If you can use the auxiliary field $$H$$
to calculate $$B$$ in a problem then you should. $$\vec{H}$$ was invented 
to make your life easier so that you don't have to calculate
the bound current.

The idea of bound current and bound charge give you a way
to think about why the field is changed by the material, but it's
not a good way to calculate anything.

After break Dave is going to tell you about the auxilliary field
$$H$$ which is the better way to calculate the field in magnetized
matter.
I'm pretty sure I was taught that it's the torque on the atoms that
makes the material polarize.  I think the 
