---
layout: 12pt,review
title: "Lec 01 Math"
author: 
  - name: Cole Brookson
    affiliation: uab
    email: cole.brookson(at)gmail.com
    footnote: Corresponding author
address: 
  - code: uab
    address: | 
      Department of Biological Sciences, 
      University of Alberta,
      Edmonton, AB XXXXXX, CAN
abstract: |

keywords:

bibliography: components/references.bib
csl: filters/ecology-letters.csl
documentclass: components/elsarticle

output:
  pdf_document:
    fig_caption: true
    template: components/elsarticle.latex
    keep_tex: true

---

## Lecture 01 Math Stuff

### After slides on exp. growth eq

We are actually just saying this: 

$$N_{t+1} = 2N_t$$

which is essentially just saying that the number of lily pads next week will be twice the number this week. 

More generally, we can state this as:

$$N_{t+1} = \lambda N_t $$ where lambda is the *population growth rate*. 

Recall in our example of $\lambda = 2$ that the number of indvidiauls if we think about consecutive weeks is actually 2, 4, 8, 16, 32 or $2^1, 2^2, 2^3, 2^4, 2^5$. 

So we can rewrite the equation as $$ N_t = \lambda^t$$ which is just another way of describing the previous equation. 

Okay but $\lambda$ isn't super helpful here but we can fix this via a fun little math trick

## -------- 
##### Divergence
Since $\lambda$ is an abstract number, let's rewrite it as $\lambda = 2^b$. It is a general rule that any number can be written in a large num-
ber of ways. In this case, $b = ln(\lambda)/ln(2)$. 

If we represent $\lambda$ as $2.7183^r$, we now have a lot more of formal mathematical tools at our disposal since that number is actually Euler's constant ($e$). It has the important mathematical property that its natu-
ral logarithm is equal to 1. ($ln(e) = 1$).
##### End Divergence
## -------- 
We can rewrite the previous equation as $$N_t = e^{rt}$$ which is the classic integrated form of the exponential equation. Here $\lambda$ has been replaced with $e^r$. 

So while this is the integrated version, we also might want to think about this equation in terms of the rate of change. That is, how fast is the number of individuals *changing*, not just how many are there at a given time $t$. 

## -------- 
##### Divergence
From calculus, we may remember that the rate of change of the log of any variable is equal to the derivative of that variable divided by the value of the variable. $$\frac{d(ln N)}{dt} = \frac{dN}{Ndt} $$

So if we take the natural logarithm of the previous equation at $$ ln(Nt) = rt$$ and differentiate with respect to $t$, we get $$\frac{d(ln N)}{dt} = r $$ now you can see that if we multiply both sides by $N$ we get $$\frac{dN}{dt} = rN$$ 
##### End Divergence
## -------- 
Without going through the math, if we take the natural log of out previous equation, we end up with $$\frac{dN}{dt} = rN$$ which is the classic expression (in differntiated form) of the exponential equation. So this is saying that the rate of change of N as dt approaches infinity is equal to $rN$. These are the basic equations that formally describe an exponential process. Equation 8 is the differentiated form of equation 5, and equation 5 is the integrated form of equation 8.

So we just kind of previously assumed that $r$ was a birth process, but taht's not super accurate, it is actually the growth rate, which we think of as just $r = b - d$ and here $r$ is the intrinsic rate of natural increase. 

Also, we just sort of assumed taht we stsarted with one individual in our lily pad example, but that's also hardly ever true. We can modify the integrated form of that equation to relax that assumption: $$N_t = N_0e^{rt}$$

and now THIS is the most common form of writing the integrated exponential equation. This has the number of individuals and the rate of natural increase. 

So now lets use this, we can imagine something like some aphids on a plant:

| Date      | # aphids | ln(# aphids)
| ----------- | ----------- | ----------- |
| March 25      | 0.02       | −3.91 |
| April 1   | 0.50        | −0.69 |
| April 8 | 1.50 |0.40|
| April 15 |5.00 |1.61|
| April 22|14.50|2.67|

So in a very conventient form, let's use the natural logarithm, recalling that $ln(e) = 1$ so we take the $ln$ of both sides: $$ln(N_t) = ln(N_0) + rt$$,

and now this looks very similar to $$y=mx + b$$ which you might remember is the slope of the line. So we actually here have a lienar equation relating the natural logarithm of the number of aphids to time. 

So if we plot this out, with $ln(N)$ on the y and time on the x, we get this plot, and if we fit a line through these points, then find the slope of that line, we get the slope of the line, which I calculated before and in this case happens to be $r = 1.547$, and if I take this line down through the y axis, I know that the y-intercept is actually equal to -4.626. And I know this might seem trivial but it's actually INCREDIBLY useful, because what we now have is the **very** simple equation of a line, and what can we famously get when we have all of this components here?? $$1.547t - 4.626 = ?$$ We have the $ln(N_t)$ for any future $t$. Therefore we have (approxiamtely) how many organisms there will be at time $t$. Or we could obviously rearranged this and ask when in time we will get some critical number of organisms. 


In practice, calculations like these exclude many complicating factors, and
we should never take too seriously exact predictions the model makes. On the
other hand, we might only have data like these, and while it may not be a very good prediction, but it is the only one available sometimes, and that itself is useful. 

## Density Depdendence 

**start back on slides**

So we start with $$\frac{dN}{dt} = rN$$ but now let's presume that $r$ is proportional to some $F$ (i.e. $$r = bF$$) where $F$ is the amount of resources, so now this becomes $$\frac{dN}{dt} = bFN$$, but we should assume there's no inflow, so there's a total amount of resources and we need to divide that so a part has already been used and some is still avilable. So $$F_T = F + cN$$ where $F_T$ is the total amount of resources, and $c$ is the amount of $F$ held within each individaul. So we can maniuplate the previous equation such that $$F = F_T - cN$$. We could then substitute F into our equation above and we now have $$\frac{dN}{dt} = b(F_T - cN)N$$. So you might be able to see already that this is a quadratic equation (because if you expand this you'll get $N^2$, $bF_TN - bcN^2$), and **DRAW QUADRATIC ON THE BOARD WITH THE ROOTS CROSSING ZERO** you might remember from math class that you can find the equilibrium points (the points at which the population neither increases nor decreses), by setting the derrivative to zero, $$0 = b(F_T - cN)N$$, you get two equilibria (which I won't go through), The first solution is at N = 0, which simply says that the rate of change of the population is zero when there are no individuals in the population. The second solution is at $F_T/c$, which is the maximumvalue that N can have. This is the value of N for which F = 0 (when all theresources in the system are contained within the bodies of the individuals in the population).

So while this might just seem like pointless math, we've actually discovered two maybe obvious but *fundamental* principles of population growth. First, the trivial fact that populations that go extinct stay extinct, and second, that there is this value, $F_T/c$ that we often call the carrying capacity, usually written $K$, which is the capacity of the environment to sustain individuals. 

So we can actually rewrite our equation here as $$\frac{dN}{dt} = bF_TN\left(\frac{\frac{F_T}{c} - N}{\frac{F_T}{c}} \right)$$, and if we sub back in $r$ for $bF_T$ and $K$ for $F_T/c$ then we get $$\frac{dN}{dt} = rN\frac{K-N}{K}$$ which is the classic form of the logistic equation. has a very simple biological interpretation. The quantity (K − N)/K is the fraction of the carrying capacity that has not yet been taken up by the individuals in the population.












