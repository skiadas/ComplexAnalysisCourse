# Closed Curve Theorem

## Reading

Section 4.2

## Problems

Practice problems (page 56): 7, 8, 9, 10

Challenge problems (optional): 11, 12

## Topics to know

Statements in these notes will be slightly more general than in the book. Pay attention to the differences.

1. Warmup problem: If $K_1\supset K_2\supset K_3\supset \cdots$ is a sequence of compact sets, then their intersection is nonempty: $\cap_{n=1}^\infty K_n\neq\emptyset$.
    - Form sequence $(z_n)_{n\in\mathbb{N}}$ where $z_n\in K_n$.
    - Must have a convergent subsequence, that converges to $z_0$.
    - Show it must belong to all the $K_n$.
2. Rectangle Theorem for Linear functions: A linear function around any rectangle has integral $0$.
    - Any function that has an antiderivative would have zero integral along a closed curve.
3. If $f$ is differentiable at $z_0$ then $f(z) = f(z_0) + f'(z_0)(z-z_0) + g(z)(z-z_0)$ where $g$ is continuous at $z_0$ and $g(z_0) = 0$.
    - It is also differentiable/continuous anywhere else where $g$ is differentiable/continuous.
    - The converse is also true.
4. Rectangle Theorem: If $f$ analytic on an open set containing a rectangle, then its integral around the rectangle is $0$.
    - Say integral equal $I\neq 0$.
    - Split rectangle in 4 quarters. At least one quarter must have integral that is $\gg I/4$.
    - Split *that* quarter up in 4 quarters. At least one of those must have integral $\gg I/16$.
    - Continue in this manner. Have a sequence of rectangles each containing all the remaining ones, the $n$-th rectangle having an integral $\gg I/4^n$.
    - Let $z_0$ be a point contained in all those rectangles (by first item).
    - Write $f(z) = f(z_0) + f'(z_0)(z-z_0) + g(z)(z-z_0)$.
    - $\int_\Gamma f(z)dz$ = $\int_\Gamma g(z)(z-z_0)dz$ (difference is linear, 3rd item applies).
    - Let $\epsilon > 0$. There is a $\delta>0$, which we can further assume is $\delta \leq 1$, such that $|z-z_0|<\delta$ implies $|g(z)|<\epsilon$.
    - Choose $N$ such that the $N$-th rectangle is fully contained in $D_{z_0}(\delta)$. This is possible as the diameters of these rectangles go to $0$.
    - We now consider the integral of $g(z)(z-z_0)$ along that $N$-th rectangle. It has length $L/2^n$ where $L$ is the length of the original integral.
        - Along the path of integration, $|z-z_0|$ is bounded by the diameter of the rectangle, since the whole rectangle is contained in $D_{z_0}(\delta)$. The diameter is no more than the perimeter, $L/2^n$. The integrand is thus bounded by $\epsilon \delta < \epsilon L / 2^n$.
    - Therefore the integral over the $N$-th rectangle is $\ll \frac{L^2\epsilon}{4^n}$ by the ML-formula.
    - But we built those rectangles so that the integral is $\gg I/4^n$.
    - Putting the two together we have $\frac{I}{4^n}\ll \frac{L^2\epsilon}{4^n}$.
    - So $I\ll L^2\epsilon$. For all $\epsilon > 0$. This is clearly not true the moment we pick an $\epsilon < I / L^2$.
    - This contradicts the assumption that $I\neq 0$.
5. If $f$ is analytic on a domain (open connected set) $U$, fix a point $z_0$. Assume the domain is convex (can go from any one point to any other in a straight line). For any other point $z\in U$, consider a path $C$ from $z_0$ to $z$ consisting entirely of horizontal and vertical segments. Define $F(z) = \int_C f(z)dz$. This integral is independent of the path chosen.
    - Think about why there are such paths.
    - Think about why the question of independence of the value from the path boils down to looking at small rectangles and going from one corner to the opposite along the two possible ways.
    - Part 4 showed that the integral around a rectangle is $0$. This implies that going from one corner to the opposite gives the same answer whichever side we choose to go around the rectangle.
6. With $f$ and $F$ as in the previous part, $F$ is differentiable and $F'(z) = f(z)$.
    - $F(z+h) - F(z) = \int_z^{z+h} f(t)dt$ where the path from $z$ to $z+h$ is one of the two paths around the rectangle, say the one that goes along the real direction first.
    - Also have $f(z) = \frac{1}{h} \int_z^{z+h} f(z) dt$.
    - Then $\displaystyle\frac{F(z+h) - F(z)}{h} - f(z) = \frac{1}{h}\int_z^{z+h}f(t) -f(z) dt$.
    - For a given $\epsilon > 0$, and since $f$ is continuous at $z$, we can choose $h$ small enough so that $f(t) - f(z) \ll \epsilon$ for all $t$ in the rectangle with edges $z$ and $z+h$.
    - Then $\displaystyle\frac{F(z+h) - F(z)}{h} - f(z) \ll \frac{1}{h}2h\epsilon = 2\epsilon$ by ML-formula.
    - This proves that $F'(z) = f(z)$.
7. Closed Curve Theorem: If $U$ is a convex domain and $f$ is analytic on $U$, then $\int_C f(z)dz = 0$ for any closed curve contained in $U$.
    - The previous part tells us that $f(z)$ has an antiderivative on $U$.
