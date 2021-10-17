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
Without going through the math, if we take the natural log of out previous equation, we end up with $$\frac{dN}{dt} = rN$$ which is the classic expression (in differntiated form) of the exponential equation. So this is saying that the rate of change of N as dt approaches infinity is equal to $rN$. 










