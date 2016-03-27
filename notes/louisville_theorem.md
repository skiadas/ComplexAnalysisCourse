# Louisville's Theorem

## Reading

Section 5.2

## Problems

Practice problems (page 74): 6b, 8, 9, 10, 12, 15

Challenge (optional): 13

## Topics to know

1. Louisville's Theorem: An entire bounded function is constant.
    - Fix two points $a, b$. Consider $R\to \infty$, and focus on circle $C$ around $0$ with radius $R$.
    - $f(b) - f(a) = \frac{1}{2\pi i}\left(\int_C \frac{f(z)}{z-a}dz - \int_C \frac{f(z)}{z-b}dz\right) = \frac{1}{2\pi i}\int_C \frac{f(z)(b-a)}{(z-a)(z-b)}dz$
    - If $f \ll M$, then this integral is $\ll \frac{M(b-a) R}{(R-|a|)(R-|b|)}$.
    - As $R\to \infty$, this goes to $0$.
    - So $f(b)-f(a)$ must equal $0$.
2. Extended Louisville Theorem: If $f$ is entire and $|f(z)| \leq A + B|z|^k$, then $f$ is a polynomial of degree at most $k$.
    - Proof by induction on $k$, base case being Louisville's Theorem.
    - $|g(z)| = \left|\frac{f(z) - f(0)}{z}\right| \leq C + D|z|^{k-1}$
        - Near $0$ it can be extended to be entire, so is bounded
        - For $|z| \geq 1$: $\frac{|f(z) - f(0)|}{|z|}\leq \frac{|f(z)| + |f(0)|}{|z|} \leq \frac{A + |f(0)| + B |z|^k}{|z|}\leq C + B|z|^{k-1}$
    - By induction $g$ must be a polynomial of degree at most $k-1$.
    - $f(z) = f(0) + z g(z)$ is a polynomial of degree at most $k$.
3. Alternative proof of the above two facts (exercises 6, 7):
    - If $f$ is bounded by $M$ along the circle of radius $R$ around $0$ and $a_k$ is the $k$-th coefficient in its power series expansion around $0$, then $|a_k|\leq \frac{M}{R^k}$. This follows from $M-L$ formula on $a_k = \frac{1}{2\pi i}\int_C \frac{f(z)}{z^{k+1}} dz$
    - So if $f$ is bounded on the entire complex plane, $R$ can be arbitrarily large, forcing $a_k=0$ for all $k\geq 1$. So power series is just constant, so $f$ is constant.
    - If $|f(z)|\leq A + B|z|^k$, and $j > k$, then $|a_j| \leq \frac{A + B R^k}{R^j}$ must be valid for all $R > 0$, so it must equal $0$ if we consider $R\to \infty$. Therefore the power series terminates at the $k$-th term, hence a polynomial.
4. Fundamental Theorem of Algebra: Any non-constant polynomial $P$ must have a zero. And by induction, it has exactly $\textrm{deg} P$ zeroes.
    - Suppose not. Consider $f(z) = \frac{1}{P(z)}$.
    - $f$ is entire.
    - $P(z) \to \infty$ as $z\to\infty$. So $f$ is bounded.
    - So $f$ must be constant. Then $P$ is constant, a contradiction.
5. Gauss-Lucas theorem (proof on page 68): The zeroes of the derivative of a polynomial lie within the convex hull of the zeros of the polynomial.
