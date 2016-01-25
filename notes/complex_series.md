# Sequences and Series in the Complex Plane

## Reading

Section 1.4, part I

## Problems

Practice problems:

1. Show that $z_n\to z$ if and only if $\bar z_n\to \bar z$.
2. Suppose that $|z| < 1$. Show that $a_n = z^n\to 0$.
3. True or False: The series $\sum_{n=0}^\infty a_n$ converges if and only if the series $\sum_{n=0}^\infty \textrm{Re}(a_n)$ and $\sum_{n=0}^\infty \textrm{Im}(a_n)$ both converge.
4. True or False: If $\sum_{n=0}^\infty a_n$ converges then $\sum_{n=0}^\infty \bar a_n$ also converges.
5. If $\sum_{n=0}^\infty a_n$ converges, show that $\sum_{n=0}^\infty a_n^2$ also converges.

## Topics to know

1. Sequence $z_n$ converges to $z$ iff $|z_n - z|\to 0$.
    - Alternative definition
    - Laws for convergent sequences
2. Sequence converges if and only if its real parts converge and its imaginary parts converge.
    - Key inequality: $|\textrm{Re(z)}|,|\textrm{Im(z)}|\leq |z|\leq |\textrm{Re(z)}| + |\textrm{Im(z)}|$
3. Cauchy sequences, for both real numbers and complex numbers.
    - Laws for Cauchy sequences
4. Convergent sequences are Cauchy.
5. Cauchy sequences of real numbers converge. Key steps:
    - Cauchy sequences are bounded.
    - Any sequence contains a monotone subsequence.
        - Key statement: There is an $N$ such that for all $M\geq N$ there is a $K\geq M$ such that $a_K\geq a_M$.
        - If that is true, then can build an increasing subsequence.
        - If it is false, then we can build a decreasing subsequence.
    - If a Cauchy sequence has a convergent subsequence then it converges.
6. Cauchy sequences of complex numbers converge.
    - Go through their real/imaginary parts.
7. Series of complex numbers. Review of results from Calculus 3. How do they carry over to complex numbers?
    - Definition of Convergent Series.
    - Divergence test.
    - Geometric series.
    - Definition of absolute/conditional convergence.
    - Alternating series test.
    - Absolute convergence implies conditional convergence.
    - Root and ratio tests.
