# Cauchy Integral Formula

## Reading

Section 5.1 (up to bottom of page 62)

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
    - Alternative analytic proof on page 62 (lemma 5.4).
