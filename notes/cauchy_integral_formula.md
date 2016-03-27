# Cauchy Integral Formula

## Reading

Section 5.1, 6.1, 6.2

## Problems

Practice problems (page 74): 2, 3, 4, 5

Practice problems (page 90): 1, 2, 3

## Topics to know

1. If $f$ is analytic on a convex domain $U$, $a\in U$ a point, and $g(z)$ is the continuous function such that $f(z) = f(a) + f'(a)(z-a) + g(z)(z-a)$, then the rectangle theorem applies to $g$: $\int_\Gamma f(z)dz = 0$
    - If $a$ is in the exterior of the rectangle, then the previous proof basically works.
    - If $a$ is a boundary point, let $M$ be a bound of $g$ on the rectangle (since $g$ is continuous).
        - Break rectangle into six rectangles, one small around $a$ with boundary less than an arbitrary $\epsilon>0$.
        - The other 5 rectangles have integral $0$.
        - The remaining one has integral $\gg M\epsilon$, which can be made arbitrarily small.
        - Total integral is $0$.
    - If $a$ is an interior point, break into two rectangles that have $a$ as boundary point. Then previous part applies.
2. For $g$ as above, the integral theorem and the closed curve theorem also hold.
3. Note: All we really needed was that $g$ is everywhere continuous, and analytic except at finitely many points. We can do similar decompositions of the rectangle as long as there are only finitely many points to worry about.
4. Cauchy Integral Formula: Suppose $f$ is analytic on an open set $U$ and $a\in U$ a point. Suppose $R>0$ is small enough so that the closed disc around $a$ of radius $R$ is contained in $U$. Suppose $C$ is the curve that traces the circle of radius $R$ centered at $a$, with parametric equation $z(\theta) = a + Re^{i\theta}$, $\theta\in[0,2\pi]$. Then:
    $$f(a) = \frac{1}{2\pi i}\int_C \frac{f(z)}{z-a}dz$$
    - By the previous parts, $\int_C \frac{f(z)-f(a)}{z-a}dz = 0$.
    - So $f(a) \int_C \frac{1}{z-a}dz = \int_C \frac{f(z)}{z-a}dz$.
    - Direct computation shows that $\int_C \frac{1}{z-a}dz = 2\pi i$ and the result follows.
5. Same result holds for any other circle containing $a$, even if it is not centered at $a$.
    - A way to see this is to consider both that circle $C$ as well as a circle $C_2$ centered at $a$ and with a radius small enough so that it is fully contained in the interior of $C$.
    - We can join the combination $C-C_2$ with two radial lines, then decompose it into two pieces that are both closed curves for which the closed curve theorem applies.
    - Alternative analytic proof on page 62 (lemma 5.4), using power series expansion of $\frac{1}{z-a}$ around the circle's center $\alpha$.
6. Series expansion of analytic function: If we have an analytic function $f(z)$ defined on a domain $U$, and $a\in U$ is a point. Then the function equals a power series centered at $a$, the equality holding on the largest open disc centered at $a$ that is fully contained in $U$.
    - Let $z\in U$ be in that disc. Let $R > |z-a|$ be smaller than this disc's radius.
    - Let $C_R$ be the disc centered at $a$ with radius $R$.
    - Then $f(z) = \frac{1}{2\pi i}\int_{C_R}\frac{f(w)}{w-z} dw$
    - $\frac{1}{w-z} = \frac{1}{(w-a) - (z-a)} = \frac{1}{(w-a)(1-\frac{z-a}{w-a})}$
    - Let $\rho = \frac{z-a}{w-a}$. It is less than and bounded away from $1$ when $w\in C_R$.
    - $\frac{1}{1-\rho} = 1 + \rho + \rho^2 + \cdots$ uniformly in $\rho\in C_R$.
    - $f(z) =  \frac{1}{2\pi i}\int_{C_R} \frac{f(w)}{(w-a)(1-\rho)} dw = \frac{1}{2\pi i} \int_{C_R}\frac{f(w)}{w-a} \left(1 + \rho + \rho^2 + \cdots\right)$
    - Let $a_k = \frac{1}{2\pi i}\int_{C_R} \frac{f(w)}{(w-a)^{k+1}}dw$.
    - Then $f(z) = \sum a_k (z-a)^k$.
    - By previous discussions, the radius $R$ on $\int_{C_R} \frac{f(w)}{(w-a)^{k+1}}dw$ doesn't affect the value as long as the disc stays within the domain of analyticity of $f$. Also, $a_k$ must equal $\frac{f^{(k)}(a)}{k!}$ (i.e. the $k$-the derivative must exist and equal $k! a_k$).
    - So the above power series can be pushed to be valid on the largest disc around $a$ contained in $U$.
7. Consequence: An analytic function is infinitely differentiable (since power series are).
8. Special case: If $f$ is entire, then it equals a power series everywhere. In particular, it equals its Taylor series expansion around any point.
9. Consequence: If $f(z)$ is analytic with a zero at a point $a$, then $\frac{f(z)}{z-a}$ can be extended to $a$ (with value $f'(a)$) and be analytic.
10. Same result for finitely many zeros: $\frac{f(z)}{(z-a_1)(z-a_2)\cdots (z-a_k)}$ is analytic in the same set as $f(z)$.
