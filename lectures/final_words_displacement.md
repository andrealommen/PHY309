---
layout: page
title:  "Final Words on Displacement"
permalink: "lectures/final_words_displacement"
---

I wrote this lecture, because I watched many of you work problems using
$$\vec{D}$$ and I realized we needed to talk about the raison d'etre of $$\vec{D}$$.

$$\vec{D}$$ was invented to make your life easier, believe it or not.  It's
not a physical quantity, but it's a convenient non-physical quantity. You
can't compute anything you can measure with it.  For example, for
potential you still need $$\vec{E}$$.  For Work or Energy you 
need $$V$$ which means you need $$\vec{E}$$.  For Force you need $$\vec{E}$$.

### Some things that make sense to me

The Displacement vector is not a physical thing.  You couldn't measure it. 
If you divide it by the permittivity it's the field that would be there
if you only had free charge and no bound charge.  So the only time it's
physical (and you could measure it) is when there's no dielectric, in which case $$\vec{D} = \epsilon_0\vec{E}$$.

So then, you have to be careful about when you use it.  There's a Gauss'
Law for displacement, as we have seen:

$$
\nabla\cdot\vec{D} = \rho_f
$$

which is generally REALLY useful for starting problems involving dielectric.
If you start with that formula (or its integral version) you never get
in trouble putting $$\epsilon$$'s or $$\epsilon_0$$'s in the wrong places.

## Going back to our roots

In order to use $$\vec{D}$$ appropriately
I think it's useful to remember where we started.  We started with:

$$
\rho = \rho_b + \rho_f
$$

So if we want to calculate the field $$\vec{E}$$ everywhere, we need to
use the total charge.

Then we wrote down
our familiar Gauss' law for this total charge:

$$
\epsilon_0\nabla \cdot \vec{E} = \rho = \rho_b + \rho_f =  −\nabla \cdot \vec{P} + \rho_f
$$

**So $$\vec{E}$$ is the total field, not just the portion generated
by polarization.** 

Then we took the divergence term on the right over to the left, which is
sort of like subtracting the effect of the bound charge from both sides:

$$
\nabla \cdot (\epsilon_0 \vec{E} + \vec{P}) = \rho_f 
$$

so it makes sense that we get something that only depends on free charge.
But, mind you, that was the step where we created an unphysical quantity
on the left that we are about to call "electric displacement."

We define $$\vec{D}$$ the electric displacement as:

$$
\vec{D} =  \epsilon_0 \vec{E} + \vec{P} 
$$

and it is the TOTAL electric field (times $$\epsilon_0$$), PLUS the polarization.  

Adding the polarization is sort of like adding back in the field
that we lost to the polarization.  That's confusing. Remember, the
polarization will (almost) always serve do *undo* the electric
field a little (or a lot), **so $$\epsilon_0 \vec{E} + \vec{P}$$ will
almost always be larger than 
$$\epsilon_0 \vec{E} $$ by itself. And $$\vec{E}$$ is the total
field, not $$\vec{D}$$.**  (I'm saying "almost" because when
we start to deal with dielectric functions, that are functions of the
frequency of the electromagnetic wave, you can get negative
dielectrics).  

I think this equation is confusing because it looks like $$\vec{D}$$ is
the field of the free charges plus the field of the polarization, but
that's not what it is.  $$\vec{E}$$ is the total field, the field
of the bound and the free charges, and when you add $$\vec{P}$$ you're
replacing the field lost to the bound charges. 

So now Gauss's law is just

$$
\nabla \cdot \vec{D} = \rho_f 
$$

and the integral version is

$$
\oint \vec{D} \cdot d\vec{a} = Q_{f,{\rm enc}}
$$

That's why it's convenient, because now we don't have to worry about the
infinite cycle of
the polarization contributing to the field, and thereby changing the polarization,
and changing the contribution of the polarization to the field...


$$
\vec{D} =  \epsilon_0(1 + \chi_e)\vec{E} = \epsilon\vec{E} 
$$

where $$\chi_e$$ is called the electric susceptibility and $$\epsilon$$
is the permittivity.

$$\chi_e$$ is always positive, so $$\epsilon$$ is always larger
than 1, so $$\vec{D}$$ is always larger than $$\epsilon_0\vec{E}$$ which
makes sense because $$\vec{D}$$ is the electric field times $$\epsilon_0$$ that we
would have if we didn't have any bound charge. 
