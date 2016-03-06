# Standard Functions

## Reading

Section 3.2

## Problems

Practice problems:

(Pages 41-42) 12, 13, 14, 15, 17, 18

Challenge: 16

Be ready to present problems 14, 15

## Topics to know

1. Can define $e^z$ via its power series. We will offer an alternative definition.
    - Denote the function we are after as $f(z)$. We are looking for:
        - $f$ analytic.
        - $f(z+w) = f(z)f(w)$.
        - $f$ is the exponential when restricted to real numbers.
    - If $z=x+iy$, then $f(z) = f(x)f(iy)$. But $f(x)= e^x$. Suppose $f(iy) = A(y) + i B(y)$, where $A,B$ are differentiable real functions.
    - Then $f(z) = e^x A(y) + i e^x B(y)$. Also $B(0) = 0$ and $A(0) = 1$.
    - Cauchy-Riemann equations must hold. We compute $f_x(z) = f(z)$, and $f_y(z) = e^x A'(y) + i e^x B'(y)$. In order for $f_y = if_x$ to hold, must have $B' = A$ and $A' = -B$.
    - These two real-variable differentiable equations are solved by $A(y) = \cos y$ and $B(y) = \sin y$.
    - We therefore have $f(z) = e^x (\cos y + i\sin y) = e^x \textrm{cis} y$.
2. Properties:
    - $|e^z| = e^{\textrm{Re}(z)}$.
    - $e^z\neq 0$.
    - $e^{iy} = \textrm{cis} y$.
    - $e^z = a$ has infinitely many solutions (explain!!!!).
    - $(e^z)' = e^z$. Check it!
3. Can define:
    - $\sin z = \frac{1}{2i}\left(e^{iz} - e^{-iz}\right)$.
    - $\cos z = \frac{1}{2}\left(e^{iz} + e^{-iz}\right)$.
    - These make sense: Can use the two equations $e^{\pm iy} = \cos y \pm i\sin y$ to show that when $z$ is real these equations are indeed correct.
