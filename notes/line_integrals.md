# Line Integrals

## Reading

Section 4.1

## Problems

Practice problems (page 56): 1, 2, 3, 4

## Topics to know

1. Notions of piecewise-differentiable curves and of smooth curves (4.2)
2. Integral of a complex-valued function of a real variable (4.1).
3. Integrate $1/z$ and $1/z^2$ over a circle around $0$. (page 48)
4. Integral of $f(z)$ along a smooth curve.
5. Integrals of $f(z)$ over equivalent curves are equal.
6. Integral over the opposite curve is the negative of the integral over the curve.
7. Linearity of the integral (proposition 4.8).
8. $\displaystyle\int_a^b G(t)dt \ll \int_a^b |G(t)|dt$.
    - $\int_a^b G(t) dt = Re^{i\theta}$
    - $\int_a^b e^{i\theta} G(t) dt = R$ is real
    - $e^{i\theta} G(t) = A(t) + i B(t)$
    - Then $R = \int_a^b A(t)dt = \int_a^b \textrm{Re}\left(e^{-\theta}G(t)\right)dt\leq \int_a^b |G(t)|dt$.
9. ML-formula: If $f\ll M$ along a curve $C$ of length $L$, then:
    $$\int_C f(z)dz = \int_a^b f(z(t))\dot z(t)\ll \int_a^b|f(z(t))\dot z(t)|dt\ll M\int_a^b|\dot z(t)|dt = ML$$
10. If $f_n\to f$ uniformly on $C$, then $\int_C f_n(z)dz\to \int_C f(z)dz$.
    - Notion of uniform convergence: For every $\epsilon > 0$ there is an $N$ such that for all $n\geq N$ and for all $x\in C$ we have $|f_n(x) - f(x)|<\epsilon$.
    - Key idea: $n$ depends only on $epsilon, but works for all $x$.
11. If $F'(z) = f(z)$ then $\int_C f(z)dz = F(z(b)) - F(z(a))$.
    - If $\lambda(t)$ is the curve, $\gamma(t) = F(\lambda(t))$
    - Then $\dot\gamma(t) = F'(\lambda(t))\dot\lambda(t) = f(\lambda(t))\dot\lambda(t)$
    - $\int_C f(z)dz = \int_a^b f(\lambda(t))\dot\lambda(t)dt = \int_a^b \dot\gamma(t) = \gamma(b) - \gamma(a) = F(z(b)) - F(z(a))$
