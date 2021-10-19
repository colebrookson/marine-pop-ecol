# Algebra Review

Let's say we have the system:

$$Y_1 = a_1X_1 + b_1X_2 + c_1X_3$$ $$Y_2 = a_2X_1 + b_2X_2 + c_2X_3$$ $$Y_3 = a_3X_1 + b_3X_2 + c_3X_3$$

and as a matter of convenience, we could represent this as:

$$
\begin{vmatrix}
Y_1 \\
Y_2 \\
Y_3 \\
\end{vmatrix} = 
\begin{vmatrix}
a_1 & b_1 & c_1 \\
a_2 & b_2 & c_2 \\
a_3 & b_3 & c_3
\end{vmatrix}
\begin{vmatrix}
X_1 \\
X_2 \\
X_3 \\
\end{vmatrix}
$$

Here we have three matrices: first a matrix with a single column (the Ys),
second a square matrix with three columns (sometimes referred to as the
detached coefficient matrix), and third a matrix with a single column (the Xs).
Sometimes the various matrices are simply referred to using a single letter, but
it is customary when speaking of matrices to put them in boldface type, so the
above equation could be

$$\bold{Y = AX}$$

Equation here is identical to the system above, except it is obviously more com-
pact. This way of writing a set of linear equations becomes especially conve-
nient when dealing with large systems. A system of 500 equations could be
just as easily written as equation A2.

Equation A2 is interpreted in the same way as any other equation—the
matrix Y (when there is only a single column, we sometimes refer to the
matrix as a “column vector”) is equal to the column vector X multiplied by
the matrix A. But multiplying matrices is not as simple as multiplying scalars
(nonmatrix variables—that is, regular numbers).

## Operations

### Addition

Let's say you have some equation, something you know how to solve: $$3x = 6.$$ We know how to solve this!! But what about two equations with who unknowns? $$3x_1 + x_2 = 10$$ $$2x_1 - x_2 = 0$$

You could probably figure this out if I gave you enough time by eliminating variables, and eventually getting $x_1= 2, x_2 = 4$. Next would be three equations in three unkowns: $$4x_1 + 3x_22 + 2x_3 = 0$$ $$2x_1 - 2x_2 + 5x_3 = 6$$ $$x_1 - x_2 - 3x_3 = 1$$ 

and this would actually be hard. The solution is still tractable but becomes difficult to just keep track of. However, as we increase the number of unkowns further, the solution becoems even MORE difficult. However, we can write the above system as:

$$
\begin{pmatrix}
4 & 3 & 2 \\
2 & -2 & 5 \\
1 & -1 & -3
\end{pmatrix}
\begin{pmatrix}
x_1 \\
x_2 \\
x_3 \\
\end{pmatrix} =
\begin{pmatrix}
0 \\
6 \\
1
\end{pmatrix}
$$

However this works only if we agree to some strict rules reagrading order of the variables and positions of coefficients. But this is **more** than a convenient way to write the previous equation. *Talk about how this may be intuitive*. 

**The rules of matrix algebra have only one purpose: to ensure this equation (just above) is the same as the equation above that.**

#### Definitions:

**Matrix:** a rectangular array of symbols (i.e. numbers, variables, functions, etc)
**Element:** one of the sybols contained in a matrix, identified by subscripts denoting row and column
**Dimensions:** number of rows and columns
**Column Vector:** an $(m \times 1)$ matrix
**Row Vector:** a $(1 \times n)$ matrix
**Scalar:** an ordinary number

## Operations

### Addition

$$
\begin{pmatrix}
a_{11} & a_{12} \\
a_{21} & a_{22} 
\end{pmatrix} + 
\begin{pmatrix}
b_{11} & b_{12} \\
b_{21} & b_{22} 
\end{pmatrix} =
\begin{pmatrix}
a_{11} + b_{11} & a_{12} + b_{12} \\
a_{21} + b_{21} & a_{22} + b_{22} 
\end{pmatrix}
$$

So here, $\bold{A +B}$ is defined only if $\bold{A}$ and $\bold{B}$
 are of the same dimension, and that if they are defined, $\bold{A + B} = \bold{B + A}$

 ### Scalar Multiplication
 $$
 2
\begin{pmatrix}
a & b \\
c & d 
\end{pmatrix} = 
\begin{pmatrix}
2a & 2b \\
2c & 2d 
\end{pmatrix}
$$

### Transpose 

The *transpose* of $\bold{A}$, denoted $\bold{A^T}$ is obtained by switching rows and columns:

$$
\begin{pmatrix}
1 & 2 & 3 \\
4 & 5 & 6 
\end{pmatrix}^T = 
\begin{pmatrix}
1 & 4 \\
2 & 5 \\
3 & 6 
\end{pmatrix}
$$
and vice versa. 

### Matrix Multiplication

Recall ALWAYS that:

$$
\begin{pmatrix}
1 & 2 \\
3 & 4 
\end{pmatrix}
\begin{pmatrix}
x_1 \\
x_2 
\end{pmatrix}=
\begin{pmatrix}
5 \\
6
\end{pmatrix}
$$
and that MUST be equivalent to:

$$
1x_1 + 2x_2 = 5 \\
3x_1 + 4x_2 = 6
$$
and so the rule for matrices of all dimensions is:

$$
\begin{pmatrix}
a_{11} & a_{12} \\
a_{21} & a_{22} 
\end{pmatrix} + 
\begin{pmatrix}
x_1 \\
x_2
\end{pmatrix} =
\begin{pmatrix}
a_{11}x_1 & a_{12}x_2 \\
a_{21}x_1 & a_{22}x_2 
\end{pmatrix}
$$
Now note this is a matrix (2x2) multiplied by a vector. If we want to multiply a matrix $\bold{A}$ by another matrix $\bold{B}$, then we can write as such

$$
\bold{A} = 
\begin{pmatrix}
a_{11} & a_{12} \\
a_{21} & a_{22} 
\end{pmatrix}
$$ and
$$
\bold{B} = 
\begin{pmatrix}
b_{11} & b_{12} \\
b_{21} & b_{22} 
\end{pmatrix}
$$ then 
$$
\bold{AB} =
\begin{pmatrix}
a_{11}b_{11} +  a_{11}b_{12} & a_{12}b_{12} + a_{12}b_{22}  \\
a_{21}b_{11} + a_{22}b_{21} & a_{21}b_{12} + a_{22}b_{22}
\end{pmatrix}
$$

### Determinant

The determinant is important, but hard to convey intuitively, so just stick with me for a bit. The formula for a $2 \times 2$ matrix is 
$$ \text{det}
\begin{pmatrix}
a & b \\
c & d
\end{pmatrix} = 
ad - bc
$$

### Identity Matrix

This is a special square matrix with ones on the diagonal and zeros elsewhere: 
$$ \bold{I} = 
\begin{pmatrix}
1 & 0 & 0 \\
0 & 1 & 0 \\
0 & 0 & 1 
\end{pmatrix}
$$
And it's important because it behaves like the number $1$ in scalar arithmetic: 
$$\bold{IA} = \bold{AI} = \bold{A}$$  and $$\bold{Ix} = \bold{x}$$ similar to how in a normal equation, $$x * 1 = x.$$ for any nonzero matrix $\bold{A}$ and vector $\bold{x}$ that you can multiply. 
### Eigenvalues and eigenvectors

The eigenvalues of a square matrix play a fundamental role in the solution of linear systems of differential equations. They provide complete dynamic information from the solution to a set of static, algebraic equations. Since matrix population models are based on a set of matrix difference equations $$ \bold{n}(t+1) = \bold{An}(t)$$ eigenvalues and eigenvectors are the basis on which most of demographic analysis rests. 

#### Eigenvectors

If we consider some arbitrary vector $x$ being multiplied by a given matrix $\bold{A}$ to get some vector $y$: 

$$
\begin{pmatrix}
3 & -6 \\
2 & -5 
\end{pmatrix}
\begin{pmatrix}
4 \\
1
\end{pmatrix}=
\begin{pmatrix}
6 \\
3
\end{pmatrix}
$$
there is no obvious relationship between $x and y$. And if a different $x$ vector had been cosen, the change in $x_1 and x_2$ would be different. However, consider the special vector $\bold{x} = (1 \space{}1)^T$, then we have the following:
$$
\begin{pmatrix}
3 & -6 \\
2 & -5 
\end{pmatrix}
\begin{pmatrix}
1 \\
1
\end{pmatrix}=
\begin{pmatrix}
-3 \\
-3
\end{pmatrix}
$$
Now we can see an obvious relationship, matrix multiplication multiplied both entries of $x$ by the same factor, $-3$. A vector with the property that matrix multiplication is equivalent to scalar multiplication, so that $$\bold{Ax} = \lambda \bold{x}$$ for some scalar $\lambda$ is called an **eigenvector** of $\bold{A}$. The scalar $\lambda$ is called the *eigenvalue*. "Eigen" is from German for "self", and you can see that the eigenvectors of a matrix retain their identity, in a sense, under the transformation defined by the multiplication of $\bold{A}$. 

## Characteristic Equation

If we have some matrix $A$ we want to find some $\lambda and x$ such that $$\bold{Ax} = \lambda x$$. This way, $\lambda$ and $\bold{x}$ will satisfy $$\bold{Ax} - \lambda\bold{x} = 0.$$ where $0$ is a vector of zeroes, so that $$(\bold{A} - \lambda\bold{I})\bold{x} = 0.$$ So here, we want a solution to this unknown parameter, $\lambda$. To find some values for $\lambda$ we can restate the above as $$\text{det}(\bold{A} - \lambda\bold{I}) = 0$$ and this is the **characteristic equation** of $\bold{A}$. What does it look like? Well if we take our last numerical example of $\bold{A}$ above, we can state   
$$\bold{A} - \lambda\bold{I} = 
\begin{pmatrix}
3 - \lambda & -6 \\
2 & -5 - \lambda
\end{pmatrix}
$$ because if we think back what we actually have here is 
$$
\begin{pmatrix}
3 & -6 \\
2 & -5
\end{pmatrix} - 
\lambda
\begin{pmatrix}
1 & 0 \\
0 & 1
\end{pmatrix}
$$

So if we try to find 
$$ \text{det}(\bold{A} - \lambda I) = (3-\lambda)(-5-\lambda) - (2)(-6)$$ or $$\lambda^2 -2\lambda -3 = 0$$ which is the characteristic equation. **So now we can find the roots!!!**

## Wrap Up

So what did we just figure out??? Well, what we ACTUALLY did was figure out that if you have some large system of equations, you can represent it in a matrix!! Why is that important? Because it turns out if you simplify things down and get to the point that you **can figure out the stability of the system from just these values**!!!! 
