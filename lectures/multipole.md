---
layout: page
title:  "Multipole Expansion (and Legendre Polynomials)"
permalink: "/lectures/multipole"
---

(Start this lecture with the "Crash Course in Chapter 3" notes to
remind everyone where we've come to, because I've thrown a lot of different
methods at you.  That's the point of chapter 3, actually.)

This is kind of a lecture about Legendre polynomials and kind of a lecture
about multipole expansion.

The Legendre Polynomials come in two ways:
* They arise naturally when you separate variables in spherical coordinates
* They arise naturally when you use Coulomb's equation for potential, and
consider it at large distances.  In other words, they arise in the multipole
expansion.

# Separation of Variables in Spherical Coordinates
Again, to separate variables we start out with the hope that we will
be able to come up with a potential that is the produce of two
functions, in this case, one that depends on $$r$$ and one that depends
on $$\theta$$.

$$
V(r, \theta) = R(r)\Theta(\theta)
$$

Notice that we're assuming the problem has azimuthal symmetry. In other words,
we're assuming the problem doesn't depend upon $$\phi$$.

Put our $$V(r, \theta)$$ above into Laplace's equation in spherical coordinates (bottom of page 141, equation 3.53) and we end up with two terms as we did
before.  This time, one of them depends only on $$r$$ and the other one
depends only on $$\theta$$ and the sum of them has to be zero by Laplace's
equation.  In the cartesian case we set one equal to $$k^2$$ and one equal
to $$-k^2$$.  This time (because we're heading toward Legendre Polynomials and we
want to make our life easier) we set the $$r$$ term equal to $$l(l+1)$$ and
the $$\theta$$ term equal to $$-l(l+1)$$. 
When the dust clears we end up with

$$
R(r) = Ar^l + \frac{B}{r^{l+1}}
$$

and

$$
\Theta(\theta) = P_l(\cos\theta)
$$

where $$P_l(\cos\theta)$$ are the Legendre polynomials.

$$
P_0(x) = 1\\
p_1(x) = x \\
P_2(x) = (3x^2 -1)/2\\
p_3(x) = (5x^3 - 3x)/2
$$

I don't actually recognize them until I put in the $$\cos\theta$$ and
then they start to look familiar to me

$$
P_0(\cos(\theta))) = 1\\
P_1(\cos(\theta))) = \cos(\theta)) \\
P_2(\cos(\theta))) = (3\cos(\theta))^2 -1)/2\\
p_3(\cos(\theta))) = (5\cos(\theta))^3 - 3\cos(\theta)))/2 
$$

So let's just remember where we were in the case of cartesian
coordinates, because I think we're more familiar with the sines
and cosines and exponentials that entered there.

We came up with the sines and cosines and exponentials because
for example our equation in $$X$$ looked like this

$$
\frac{d^2X}{dx^2} = -k^2 X
$$

and we knew that $$\sin$$ and $$\cos$$ were solutions to that.  

Same thing here we end up with (for $$\Theta$$)

$$
\frac{1}{\Theta\sin\theta} \frac{d}{d\theta} \left(\sin\theta \frac{d\Theta}{d\theta}\right) = -l(l+1)
$$

and the solutions to that are Legendre polynomials. 

And just as before we know our solution is some combination of
them (because the Legendre polynomials are complete, i.e. you can express
any function as the sum of them.)

So now we have:

$$
V(r, \theta) = \sum_{l=0}^{l=\infty} \left(A_lR^2 + \frac{B_l}{r^{l+1}}\right) P_l(\cos \theta)
$$

and as before, we use boundary conditions to figure out what the $$A_l$$'s
and $$B_l$$'s are. 

Example 3.6 (page 143). The potential $$V_0(\theta)$$ is specified on the surface
of a hollow sphere of radius $$R$$. Find the potential inside the sphere.

*For the sake of noticing when you use which technique to solve which problem,
note that if instead of $$V_0(\theta)$$ we were just told that the 
potential on the sphere was was constant, what would you do?  (Talk with
your neighbor.)  Ans: Image charge wouldn't work, because you can't
put the charge inside the sphere like we did on the last homework.
I would actually write down Laplace's equation in spherical coordinates (you only need the $$r$$ term), 

$$
\frac{1}{r^2} \frac{\partial V}{\partial r} \left( r^2 \frac{\partial V}{\partial r} \right) = 0
$$

integrate it twice, and then use the very
simple boundary condition $$V(r) = V_0$$ to figure out what the constants
were.

But let's go back to our problem with the function of $$\theta$$ on the boundary.

Talk with your neighbor about what you're planning on doing with the boundary conditions from here.  Hint: before you do anything else, make your life easier by deciding that either
$$A$$ or $$B$$ has to be zero.

Answer, yes $$B$$ has to be zero, because otherwise the potential blows
up in the center of the sphere.

And then you can use the other boundary condition to find the $$A_l$$'s:

$$
V_0(\theta) = \sum_{l=0}^{l=\infty} A_l R^l P_l(\cos\theta)
$$

and then you do Fourier's trick again to find the values of $$A_l$$. I will
leave that to your book to describe (page 144).

## Legendre polynomials
### Point #1 of Legendre Polynomials
They are easily integrable, because they're just polynomials (the
$$r$$ part is also a polynomial, so both things you can integrate.
In your second homework you will actually integrate one of them to
get the answer.)

### Point #2 of Legendre Polynomials
They form a complete set of functions, so you can express any function
as a sum of them. Thus, they let us do the same kind of Fourier's trick
we did with the sine and cosine.

### Point #3 of Legendre Polynomials
They arise naturally
when you separate variables in a problem with azimuthal symmetry.
They also arise naturally owing to the form of the potential being
$$1/R$$ where $$R$$ is the distance between the source and the point
you're calculating the potential.  
 
### Point #4 of Legenedre Polynomials (related to point #2)
They work great for anything with azimuthal symmetry so you just
have $$\theta$$ (and not $$\phi$$).  

## Legendre polynomials as being generated by 1/R

### Let's look at your homework problem #2 as a way to
get to the Legendre Polynomials.

The problem is...

Get them up V on the bottom of page 1

Then show what you set epsilon equal to

and show it's small

Then show that this gives you a polynomial that you can integrate, albeit a little bit of a pain...


## Two punchlines

In spherical coordinates Laplace's equation is separable (with azimuthal
symmetry) and gives you solutions that look like this:

$$
V(r, \theta) = \sum_{l=0}^{l=\infty} \left(A_lR^2 + \frac{B_l}{r^{l+1}}\right) P_l(\cos \theta)
$$

The same Legendre Polynomials arise as soon as you expand $$1/R$$ in terms
of $$r&\prime/r$$ , in other words when you're calculating the potential
some distance away from the source. In this case there's actually
just a solution for the potential that looks like this:

$$
V(P) = \frac{1}{4\pi\epsilon_0} \sum_{n=0}^\infty \frac{1}{r^(n+1} \int (r^\prime)^nP_n(\cos\theta) \rho d\tau
$$

This is a sum over integrals over $$P_n$$'s.  Each term in the sum
as a successively higher factor of $$1/r$$ which means each term is getting
less important as you go out in space away from the source.  Normally
this expression is dominated by a monopole (n=0) or dipole (n=1) term.  The
dipole term will become very important when we do radiation.

With your neighbor, figure out what the n=0 and n=1 terms are. 
(Ans - the field of a point
charge, and the field of a dipole).  You should now read the section called
"The Monopole and Dipole terms" (Page 154.)
