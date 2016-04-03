# Uniqueness, Mean Value, Maximum Modulus Theorems

## Reading

Section 6.3

## Problems

Practice problems (page 90): 4, 5, 6, 7, 8, 10

Challenge: 12, 13


## Topics to know

1. Uniqueness Theorem: On a domain $U$, if there is a sequence $z_n\subset U$ and $z\in U$ such that $z_n\to z$, and $f(z_n) = 0$, then $f$ is identically zero on $U$.
    - Note that power series uniqueness says: If $y_n\to y \in U$ and $f(y_n) = 0$ and $D(y, r)\subset U$, then $f(z) = 0$ for all $z\in D(y, r)$.
    - Define $A = \{a \in U \mid a \textrm{ is the limit point of a sequence of zeros } \}$ (in particular $f(z) = 0$ for all $z\in A$).
    - Define $B$ be the rest.
    - We will show they are both open sets. Because U is connected one of them has to be empty. Since $A$ is nonempty, $B$ must be empty.
    - $A$ is open because of the power series uniqueness: If $z\in A$ then we can find a sequence of zeros going to $z$. Since $U$ is open there is an $D(z, r)\subset U$, and $f$ is identically $0$ there. All these points are limit points of zeros of $f$, so $D(z, r)\subset A$.
    - $B$ is open: If $z\in B$, then there must be an $r>0$ such that $D(z, r)\subset B$. If not, we will build a sequence of zeros going to $z$:
        - For each $\epsilon > 0$ there is a $w\in D(z, \epsilon/2)$ with $w\not\in B$.
        - This $w$ must be the limit point of a sequence of zeros, so there is a zero $y$ such that $y\in D(w, \epsilon/2)$.
        - Then $y$ is in $D(z, \epsilon)$.
        - So for each $\epsilon > 0$ there is a zero of $f$ within $\epsilon$ of $z$.
        - So $z$ would be a limit point of zeros. Contradiction.
    - NOTE: A function *can* have infinitely many zeros. But their limit point must be outside the domain of analyticity $U$.
2. Corollary: If two functions agree on a converging sequence in a domain $U$, then they must be equal throughout the domain $U$.
    - Use case: An identity between analytic functions, that holds for real numbers, must also hold for complex numbers.
3. Corollary: If $f$ is an entire function and $f(z)\to\infty$ as $z\to \infty$, then $f$ must be a polynomial.
    - There is an $M$ so that $|f(z) \geq 1|$ for all $|z|\geq M$.
    - All zeros are restricted to $D(0, M)$. So there must be finitely many of them.
    - $g(z) = \frac{f(z)}{(z-a_1)(z-a_2)\cdots(z-a_n)}$ is entire, and has no zeros.
    - $h(z) = 1/g(z)$ satisfies $|h(z)|\leq A + |z|^n$. So is polynomial.
    - But $h(z)\neq 0$, so it must be constant. So $f(z) = C (z-a_1)(z-a_2)\cdots(z-a_n)$.
4. Mean Value Theorem: $f(a)$ equals the mean value taken around the boundary of a disc: $f(a) = \frac{1}{2\pi}\int_0^{2\pi} f\left(a + re^{i\theta}\right)d\theta$
    - Follows directly by Cauchy Integral Formula.
5. Maximum Modulus Theorem: A non-constant analytic function has no interior maximum points: For each $z\in D$ and $\delta > 0$ there is a $w\in D_z(\delta)$ such that $|f(w)| > |f(z)|$.
    - From mean value theorem: $|f(z)|\leq \max_\theta|f\left(z + re^{i\theta}\right)$
    - Since $f$ cannot be constant on any such circle, there must be a point such that $|f(z)| < |f(w)|$.
6. Minimum Modulus Theorem: An interior point for an analytic function can only be a relative minimum for the modulus if it is actually $0$.
    - Apply Maximum Modulus to $1/f$.
