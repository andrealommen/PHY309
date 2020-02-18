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
P_1(x) = x \\
P_2(x) = (3x^2 -1)/2\\
p_3(x) = (5x^3 - 3x)/2
$$

I don't actually recognize them until I put in the $$\cos\theta$$ and
then they start to look familiar to me

$$
P_0(\cos\theta) = 1\\
P_1(\cos\theta) = \cos\theta \\
P_2(\cos\theta) = (3\cos^2\theta -1)/2\\
p_3(\cos\theta) = (5\cos^3\theta - 3\cos\theta)/2 
$$

So let's just remember how separation of variables worked in the case of Cartesian
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
any azimuthally symmetric angular function as the sum of them.)

So now we have:

$$
V(r, \theta) = \sum_{l=0}^{l=\infty} \left(A_lr^2 + \frac{B_l}{r^{l+1}}\right) P_l(\cos \theta)
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

#### Let's look at your homework problem #2 
as a way to get to the Legendre Polynomials.

The problem is...

Positive charge +Q is distributed uniformly along the $$z$$ axis from $$-a$$ to
$$a$$. Show:

$$
V(r,\theta) = \frac{Q}{4\pi \epsilon_0} \frac{1}{r} \left[ 1 + \frac{1}{3} \left(\frac{a}{r}\right)^2 P_2(\cos\theta) + \frac{1}{5}\left(\frac{a}{r}\right)^4 P_4(\cos\theta) + ...\right]
$$

We start by writing down the potential (nothing fancy - just using $$V = Q/4\pi\epsilon_0R$$)

$$
V = \frac{1}{4\pi\epsilon_0}\int_{-a}^a \frac{\lambda dz}{R}
$$

where $$\vec{R} = \vec{r} - \vec{r}^\prime$$

When Griffiths does this he uses the *law of cosines* but I actually just
like to use vector algebra.

$$
\vec{r} = r\sin\theta \hat{s} + r\cos\theta \hat{z}
$$

$$
\vec{r}^\prime = z\hat{z}
$$

So then

$$
\vec{R} = r\sin\theta \hat{s} + r\sin\theta \hat{z} - z\hat{z}
$$

And then we can easily get the magnitude of $$R$$.

$$
R = (r^2 \sin^2\theta + (r\cos\theta -z)^2)^{1/2}
$$

$$
R = (r^2 \sin^2\theta + r^2\cos^2\theta -2rz\cos\theta + z^2)^{1/2}
$$

$$
R = (r^2  -2rz\cos\theta + z^2)^{1/2}
$$

$$
R = r \left[1 -2\frac{z}{r}\cos\theta + \left(\frac{z}{r}\right)^2\right]^{1/2}
$$

We let $$\epsilon$$ be:

$$
\epsilon = -2\frac{z}{r}\cos\theta + \left(\frac{z}{r}\right)^2
$$

As long is $$r>>z$$ then $$\epsilon$$ is small.

Now we can rewrite our integral...

$$
V = \frac{1}{4\pi\epsilon_0}\int_{-a}^a \frac{\lambda dz}{r(1 - \epsilon)^{1/2}}
$$

You can expand out the $$1/(1 - \epsilon)^{1/2}$$ in a Taylor's series. Griffiths does something very similar in the book. Once you collect all the terms,
you'll notice you have Legendre Polynomials.

This gives you a polynomial that you can integrate, albeit a little bit of a pain...


## Two punchlines

In spherical coordinates Laplace's equation is separable (with azimuthal
symmetry) and gives you solutions that look like this:

$$
V(r, \theta) = \sum_{l=0}^{l=\infty} \left(A_lr^2 + \frac{B_l}{r^{l+1}}\right) P_l(\cos \alpha)
$$

where $$\alpha$$ is the angle between $$\vec{r}$$ and $$\vec{r}^\prime$$.
(In the example we did above, we had the charge laid out along the $$z$$ axis
so the angle was $$\theta$$.  In general, though, the angle that belongs
there is the one in between the source and the point you're evaluating the
potential.

The same Legendre Polynomials arise as soon as you expand $$1/R$$ in terms
of $$r^\prime/r$$ , in other words when you're calculating the potential
some distance away from the source. 
The potential that looks like this:

$$
V(P) = \frac{1}{4\pi\epsilon_0} \sum_{n=0}^\infty \frac{1}{r^{n+1}} \int (r^\prime)^nP_n(\cos\alpha) \rho d\tau^\prime
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

This multipole expansion is most useful when you're far away from the 
source, because then you only need a couple of terms in the expansion.  However,
I would like to point out that as long as your sum is converging, i.e.
as long as $$r>r^\prime$$ then this sum exact solution of the potential.

This way of finding the potential is a little different than the other
ways we've talked about recently because you don't need boundary conditions.  Rather, you just need the charge distribution.

-----------------------------------------------------------
## Dipoles
(We didn't get to talk about this in class at all.)

I wanted to include some notes on dipoles, because we didn't get to
talk about them in class at all and they figure **prominently** in the
polarization chapter.

Part of the answer to Ethan's question "when would I use this?" is that
we often use the dominant term in the series as an approximation to the
potential everywhere.  This might seem like a strange thing to do when
given modern computing, we can easily calculate the potential exactly,
everywhere.  I have two responses to that. 

(1) Sometimes you can't!  Suppose
you have a solid material composed of neutral atoms and you want to calculate
the bulk properties of the material. Calculating the potential everywhere
is actually not what you want, and it's also impossible, because there
are too many charges (electrons and protons).  Rather, you want to know how can you model the
material approximately so as to understand the bulk properties.  In this case
you will likely model the atoms as dipoles, the 2nd term in the
approximation. (For a neutral atoms the monopole term is zero, because
it's proportional to the total charge.)

(2) Sometimes the problem you're trying to solve requires an approximation.  I was thinking of Nathan and their work with sound in theatres.  If they've got a
theatre with a weird column in the middle of it that dominates the way
the sound reverberates through the theatre.  Let's say the theatre has
the budget only to build two additional structures to change the resonant
properties of the theatre.  Nathan actually wouldn't want to know the details
of the effect everywhere in the theatre. Rather, if the reverberant properties
of the theatre can be expressed as the sum of an infinite series, they
want the dominant term, and they want to mitigate for that dominant term
using their two additional structures.  

Let's look at the dipole term because it figures so prominently in Chapter 4. Recall that all the terms in the multipole approximation are $$\frac{1}{4\pi\epsilon_0 r^{n+1}}$$ times the integral of $$r^{\prime n} P_n\cos{\alpha}$$ times
the charge density $$\rho(\vec{r}^\prime)$$ over the whole volume of the
charge distribution.

So the 0th term is our old friend the potential of a single charge. Recall $$P_0(x) = 1$$

$$
V_{\rm monopole} = \frac{1}{4\pi\epsilon_0} \frac{1}{r} \int (r^\prime)^0P_0(\cos\alpha) \rho d\tau^\prime
$$

where $\alpha$ is the angle the dipole vector makes with the vector pointing to
the place you're evaluating the potential.

$$
V_{\rm monopole} = \frac{1}{4\pi\epsilon_0} \frac{1}{r} \int \rho d\tau^\prime
$$

$$
V = \frac{1}{4\pi\epsilon_0} \frac{1}{r} Q
$$


So if the total charge (like on an atom) is zero then the dipole term
dominates. Let's look at that term:

$$
V_{\rm dipole} = \frac{1}{4\pi\epsilon_0} \frac{1}{r^2} \int (r^\prime)^1P_1(\cos\alpha) \rho d\tau^\prime
$$

where $$\alpha$$ is the angle between $$\vec{r}$$ and $$\hat{r}$$ (so at the moment this
integral depends upon the place you're evaluating the potential.)

$$
V_{\rm dipole} = \frac{1}{4\pi\epsilon_0} \frac{1}{r^2} \int r^\prime\cos\alpha \rho d\tau^\prime
$$

So that integral, without the $$\cos\alpha$$ in it, (and WITH a vector on $$r^\prime$$)  
is called the **dipole moment** of the distribution, $$\vec{p}$$,

$$
\vec{p} = \int \vec{r}^\prime \rho d\tau^\prime
$$

-------Here's how I went wrong in class today------------------
(For the record, what Shufan said was totally correct.)
In class today I defined the dipole moment this way.

$$
\vec{p} = \int r^\prime\cos\theta \rho d\tau^\prime  ~~~~~{\rm~Wrong~Formula}
$$

It's wrong (a) because it's not clear how $$p$$ is a vector, because nothing on
the right-hand-side is a vector, and (b) because it's not clear what coordinate
system $$\theta$$ is in.  It turns out once you remember how that angle is defined
it solves problem (a) as well as (b).  The angle that should be there is called 
$$\alpha$$ by Griffiths and is officially in neither coordinate system.  Rather
it's the angle between $$\vec{r}$$ and $$\vec{r}^\prime$$.  In the example we
did above the source was all on the z-axis so in fact $$\alpha$$ was always
$$\theta$$ in spherical coordinates. In general though the angle is the one we'd
get in this equation:

$$
\hat{r}\cdot\vec{r}^\prime = r^\prime \cos\alpha
$$

so in fact we can use that relationship to take the angle out of the integral
explicitly.  We define

$$
\vec{p} = \int \vec{r}^\prime \rho d\tau^\prime
$$

and then we get the same angle $$\cos\alpha$$ back by dotting $$\vec{p}$$ with
$$\hat{r}$$.

So now we can define the potential of a dipole as

$$
V(\vec{r}) = \frac{1}{4\pi\epsilon_0} \frac{\vec{p}\cdot\hat{r}}{r^2}
$$

Notice that the dipole moment doesn't depend on where you are trying to calculate the
potential, i.e. it doesn't depend on $$\vec{r}$$, but rather only depends
on the source coordinate $$\vec{r^\prime}$$.  The location where you're
trying to calculate the potential comes in the distance between dipole and the
calculation point in the denominator, and in the dot product between those
two directions.

You may remember from PHY106 that you had a formula for a dipole

$$
\vec{p} = q\vec{d}
$$

where $$d$$ is the distance between two charges $$+q$$ and $$-q$$
and the vector points from the negative charge to the positive charge. 

Those two definitions are the same thing!  We could practice
using delta functions in order to show that they are the same.  For
two point charges at $$x=0$$ and $$x=a$$ we can write the charge
density like this:

$$
\rho(x,y,z) = -q\delta(x,y,z) +  q\delta(x-a,y,z)
$$

Now let's put that into the integral:

$$
\vec{p} = \int \vec{r}^\prime \left(-q\delta(x,y,z) +  q\delta(x-a,y,z)\right) d\tau^\prime
$$

We have a mix of coordinate systems, but the integral is so easy with the
delta functions we don't even have to convert our charge density into
spherical coordinates.  We just evaluate the integrand at the two
points $$(0,0,0)$$ and $$(a,0,0)$$. The first term is super boring and goes
to zero right away. The second term leaves us with something...

$$
\vec{p} =  qa\hat{x}
$$

which is what we remembered it should be from PHY106.  Yay!!

And the field due to the dipole is:

$$
V_{\rm dip} = \frac{1}{4\pi\epsilon_0} \frac{\vec{p}\cdot\hat{r}}{r^2}
$$

So notice (a) that the potential of a dipole drops off like $$r^2$$ instead
of just $$r$$ like it did for a point charge. (b) That the potential
is maximized in the direction that the dipole moment points.

