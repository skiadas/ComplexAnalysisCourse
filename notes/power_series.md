# Power Series

## Reading

Section 2.2, 2.3

## Problems

Practice problems:

1. (Page 32) 8, 9b, 10, 13, 14, 21, 23

Challenge: 12, 17, 18

## Topics to know

1. Definition of $\displaystyle\overline{\lim_{n\to\infty}} a_n = \lim_{n\to\infty}\left(\sup_{k\geq n} a_k\right)$. If $\displaystyle\overline{\lim_{n\to\infty}} a_n = L$, then:
    - For each $N$ and $\epsilon > 0$ there is a $k > N$ such that $a_k \geq L-\epsilon$.
    - For each $\epsilon > 0$ there is an $N$ such that for all $k\geq N$ we have $a_k \leq L+\epsilon$.
2. Radius of convergence for $\sum C_k z^k$ dependent on $\displaystyle L =\overline{\lim}\left|C_k\right|^{1/k}$.
    - If $L = 0$, then $\displaystyle L =\overline{\lim}\left|C_k\right|^{1/k}|z| = 0$, so $|C_k z^k|\leq\frac{1}{2^k}$. Series converges absolutely for all $z$.
    - If $L = \infty$, then $\left|C_k\right|^{1/k}\geq \frac{1}{|z|}$ for infinitely many $k$. Hence $|C_kz^k|\not\to 0$. Diverges for all $z\neq 0$.
    - If $L = 1/R \in (0,\infty)$:
        - If $|z| = R(1-2\delta) < R$, then $\displaystyle\overline{\lim} \left|C_k\right|^{1/k}|z| = 1 - 2\delta$, so $\left|C_k\right|^{1/k}|z| < 1-\delta$ for all $k$ sufficiently large. Series converges.
        - If $|z| > R$ then $\displaystyle\overline{\lim} \left|C_k\right|^{1/k}|z| > 1$ so $C_k z^k\not\to 0$.
3. Examples 1-7 (page 27)
4. Differentiability of power series:
    - If $\sum C_n z^n$ converges on some disc $D(0, R)$, then so does $\sum n C_n z^{n-1}$, since $\displaystyle\overline{\lim}\left|n C_n\right|^{1/(n-1)} = \overline{\lim}\left|C_n\right|^{1/n}$.
    - Key idea for case where $R=\infty$: $\displaystyle \frac{f(z+h) - f(z)}{h} - \sum_{n=0}^\infty n C_n z^{n-1} = \sum_{n=2}^\infty C_n b_n$ where $b_n = \frac{(z+h)^n - z^n}{h} - nz^{n-1}\leq |h|\left(|z| + 1\right)^n$.
    - So $\displaystyle \left|\frac{f(z+h) - f(z)}{h} - \sum_{n=0}^\infty n C_n z^{n-1}\right| \leq A |h|$ (because $\sum |C_n|(|z|+1)^n$ converges).
    - Let $h\to 0$.
    - If $R<\infty$ the proof is technically more difficult (see page 29).
5. Power series are infinitely differentiable.
6. Power series coefficients depend on the higher order derivatives at 0.
7. Uniqueness theorem: If series is zero when evaluated at all points of a sequence $z_n\to 0$, then series is identically zero.
    - Inductively compute $C_n = \lim_{z\to 0}\frac{f(z)}{z^n} = \lim_{k\to \infty}\frac{f(z_k)}{z_k^n} = 0$
8. If two series agree on a sequence that goes to $0$, then they are identical series.
