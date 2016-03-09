# Cauchy-Riemann Equations

## Reading

Section 3.1

## Problems

Practice problems:

(Pages 41-42) 1. 2, 5, 6, 7, 8, 9, 10

Be ready to present propositions 3.6 and 3.7, problems 8, 9, 10

## Topics to know

1. If $f$ is complex-differentiable, then $f_x$ and $f_y$ both exist and relate to complex derivative $f'$:
    - For real $h$: $\displaystyle \lim_{h\to 0}\frac{f(z+h) - f(z)}{h} = f_x$.
    - For imaginary $h=it$, $\displaystyle \lim_{h\to 0}\frac{f(z+h) - f(z)}{h} = \frac{f_y}{i}$.
    - So $f_y = if_x$. Equivalently $u_x = v_y$ and $u_y = -v_x$.
2. Converse is true if the partial derivatives are continuous: If $f_x$ and $f_y$ exist in a neighborhood of $z$ and $f_y = i f_x$. Then $f$ is complex-differentiable and $f'(z) = f_x = -i f_y$.
    - Rewrite of mean value theorem: $\displaystyle \frac{f(x+h) - f(x)}{h} = f'(x+\theta h)$ where $0<\theta < 1$ is some specific but unknown number. ($x+\theta h$ is a way to specify an element between $x$ and $x+h$)
    - Suppose $h = h_1 + i h_2$, z = x + i y.
    - $\displaystyle \frac{f(z+h) - f(z)}{h} = \frac{u(z+h) - u(z)}{h} + i \frac{v(z+h) - v(z)}{h}$.
    - $u(z+h) - u(z) = u(x+h_1, y+h_2) - u(x+h_1, y) + u(x+h_1, y) - u(x, y)$ which equals $h_2 u_y(x+h_1, y+\theta_2 h_2) + h_1 u_x(x+\theta_1 h_1, y)$ where $\theta_1,\theta_2\in (0,1)$.
    - That becomes $h_2 u_y(z_2) + h_1 u_x(z_1)$ where $z_2 = (x+h_1) + i(y+\theta_2 h_2)$, $z_1 = x + \theta_1 h_1 + i y$. In both cases $z_1,z_2\to z$ as $h\to 0$.
    - Similarly $v(z+h) - v(z) = h_2 v_y(z_4) + h_1 v_x(z_3)$ where $z_3,z_4\to z$ as $h\to 0$.
    - Therefore $\displaystyle \frac{f(z+h) - f(z)}{h} = \frac{h_2}{h} \bigl[u_y(z_2) + iv_y(z_4)\bigr] + \frac{h_1}{h} \bigl[u_x(z_1) + iv_x(z_3)\bigr]$
    - Since $f_y = if_x$, we can write $\displaystyle f_x(z) = \frac{h_2}{h} f_y(z) + \frac{h_1}{h}f_x(z)$
    - Take the difference: $\frac{f(z+h) - f(z)}{h} - f_x(z) = \frac{h_2}{h} \bigl[(u_y(z_2) - u_y(z)) + i(v_y(z_1) - v_y(z))\bigr] + \frac{h_1}{h} \bigl[(u_y(z_4) - u_y(z)) + i(v_y(z_3) - v_y(z))\bigr]$
    - Because of continuity, each of the terms goes to $0$. The factors in front are bound by $1$. Therefore the whole thing goes to $0$.
    - Geometrically, instead of trying to go straight from $z+h$ to $z$, we instead move vertically then horizontally.
3. $f$ is called **analytic** at $z$ if it is complex-differentiable everywhere in a neighborhood of $z$. It is called analytic on a set $S$ if it is complex-differentiable everywhere in an open set containing $S$.
