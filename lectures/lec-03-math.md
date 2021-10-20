
# Stage-structured Model

So we can write this as what's called a stage projection matrix, or Lefkovich matrix after the person credited with ith. Now importantly here, there are two properties we want to look at. The first is the top row, these are the fecundities. So in this example, there is only one stage that has any reproduction, and that's the last one. Now the other thing we want to look at is the **subdiagonal** which will holod the surivivorship values. This is true for all transition matrices. 

**write on board**

$$N_c(t+1) = N_R(t) b$$

$$N_I(t+1) = N_C(t) s_{IC} + N_I(t) s_{II}$$

$$N_M(t+1) = N_I(t) s_{MI} + N_M(t) s_{MM} + N_R(t)s_{MR}$$

$$N_R(t+1) = N_I(t)s_{RI} + N_M(t)s_{RM} + N_R(t)s_{RR}$$

but this is annoying, so let's do it in a matrix:

$$
\begin{pmatrix}
N_C(t+1) \\
N_I(t+1) \\
N_M(t+1) \\
N_R(t+1)
\end{pmatrix} = 
\begin{pmatrix}
0 & 0 & 0 & b \\
S_{IC} & S_{II} & 0 & 0 \\
0 & S_{MI} & S_{MM} & S_{MR} \\
0 & S_{RI} & S_{RM} & S_{RR}
\end{pmatrix}
\begin{pmatrix}
N_C(t) \\
N_I(t) \\
N_M(t) \\
N_R(t)
\end{pmatrix}
$$

Let's assume that if we take this model and simulate it, that eventually we will have what's called a stable stage distribution, wherein there will be a stable **proportion** of individuals in each stage. It's a pretty well accepted fact that if you have some constant mortality and natality then you will end up at a stable stage distribution. 

But what is that value going to be? Well let's find it. So first things first, this is messy, let's simplify:

$$\bold{N_{t+1}} = \bold{P}\bold{N_t}$$

Now it turns out if we're at this SSD, then the rate of increase of each of the seaparate equations $$N_i(t+1) = \lambda N_i(t)$$ for all values of $i$ so the constant $\lambda$ can be brought back, so in *matrix* notation we have $$\bold{N_{t+1}} = \lambda\bold{N_t}$$ and if $N$ is equal to the total population, we have the regular $$N_{t+1} = \lambda N_t$$ which you might remember from yesterday is identical to the exponential equation!!!

Any structured population at its stable age distribution increases in an
exponential fashion. We can quite easily take such a population and simply
project it into the future and calculate the rate at which it is growing. That
rate will be the same as we have seen before, the intrinsic rate of natural
increase. But there is another way of calculating the rate of increase directly
from the matrix. **Mathematically speaking, the finite rate of increase is the
same as the dominant eigenvalue of the projection matrix**

So from here, we're actually ready to go forward and calculate that, and it's going to come from the most important equation in matrix population models, which we discussed this morning. 

So we can see that $\bold{N_{t+1}} = \bold{P}\bold{N_t}$ and $\bold{N_{t+1}} =\lambda\bold{N_t}$ have the same left hand side, so let's set them equal to each other so $$\bold{P}\bold{N_t} = \lambda \bold{N_t}$$ 

From here, we're going to go about solving this system. For a large system like our whale system, doing it by hand isn't actually a great idea, it's cumbersome and unweildy, but it IS a good idea to get a handle on it with pen & paper. So let's pick a nice simple version of  $\bold{P}$:
$$
\begin{pmatrix}
2 & 4 \\
0 & 3
\end{pmatrix}
$$ where
$$
\bold{P}
\bold{N_t} =
\lambda \bold{N_t}
$$. 

First things first, let's get this set to zero, so $$\bold{PN_t} -\lambda \bold{N_t}=0$$ and we can factor the $\bold{N_t}$ which gets us $$(\bold{P} -\lambda \bold{I})\bold{N_t}=0$$ and because math is fun we can AGAIN rewrite as $$\text{Det}(\bold{P} - \lambda \bold{I}) = 0$$ so in our example, that gives us 
$$
\begin{pmatrix}
2 - \lambda & 4 \\
0 & 3 - \lambda
\end{pmatrix}
$$
and so from here we're actually looking at the zeroes already since $$\text{Det}(\bold{P} - \lambda \bold{I}) = (2-\lambda)(3-\lambda) - (0)(4)$$ so what are the two values to make the right hand side zero? 2 & 3 in this case. And **those** are the eigenvalues: $$\lambda = 2$$ $$\lambda = 3$$

##### somethng happens here - page 243 of otto & day 

So remember now what we're working with, let's assume there's some vectors $$\bold{P} \bold{u} = \lambda \bold{u}$$. So here, $\bold{u}$ is the stable stage distribution vector. 

 And the eigenvalue is important why?? 

So to start, we choose one eigenvalue, let's pick 2. So we now have
$$
\begin{pmatrix}
2  & 4 \\
0 & 3 
\end{pmatrix}
\begin{pmatrix}
\bold{u_1} \\
\bold{y=u_2}
\end{pmatrix} =
2
\begin{pmatrix}
\bold{u_1} \\
\bold{u_2}
\end{pmatrix}
$$

that provides us with two equations that must both be satisfied by the eigenvector $\begin{pmatrix}
\bold{u_1} \\
\bold{u_2}
\end{pmatrix} $ now let's put those into two equations, so $$2u_1 + 4u_2 = 2u_1$$ $$ 3u_2 = 2u_2$$

So here the second equation can only be satisfied if $u_2 = 0$ so in which case, the first equation becomes $u_1 = u_1$, so any value of $u_1$ will satisfy the first equation when $u_2 = 0$. Therefore, let's arbitrarily chose $u = \begin{pmatrix}
1 \\
0
\end{pmatrix} $
associated with the eigenvalue $\lambda = 2$. Now let's turn to the second eigenvalue, $\lambda = 3$ and find that eigenvector. So again, $$
\begin{pmatrix}
2  & 4 \\
0 & 3 
\end{pmatrix}
\begin{pmatrix}
\bold{u_1} \\
\bold{y=u_2}
\end{pmatrix} =
3
\begin{pmatrix}
\bold{u_1} \\
\bold{u_2}
\end{pmatrix}
$$ and then $$2u_1 + 4u_2 = 3u_1$$  $$ 3u_2 = 3u_2$$ and if we look at the second one, it's always true, so let's choose $u_2 = 1$, and if we plug that into the equation up there it's $u_1 = 4$, so the eigenvector associated with $\
lambda = 3$ is $$u = \begin{pmatrix}
4 \\
1
\end{pmatrix} $$

So we have TWO eigenvalues here. The one with the highest magnitude is called the **dominant eigenvalue** and THAT is the rate of increase for a population. 

GO TO VANDERMEER's BOOK

So we talked about sensitivity, but I want to back up a bit. So we have the equation $$\bold{Pu} = \lambda \bold{u}$$. Recall here that $\bold{u}$ is the stable stage distribution vector. From here, it turns out we can also write $$\bold{P^T}\bold{\nu} = \lambda \bold{\nu}$$ where $\nu$ is a new special vector that satisfies our equation and technically rewrite it as $$\bold{\nu}\bold{P^T} = \lambda \bold{\nu}$$

So we're now going to differentiate between these two vectors $\bold{u}$ and $\nu$. So according to formal definitions, the vector $\bold{u}$ is the RIGHT eigenvector and the vector $\nu$ is the LEFT eigenvector. We write these two expanded very similarly:

$$
\begin{pmatrix}
p_11 & p_12 & p

