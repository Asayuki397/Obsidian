# Definition
When x is [[Random Variable]] and P(x) is [[Probability function]]
$$
E(x) = \sum xP(x)
$$

# Theorem
$$
E(X+Y) = E(X) + E(Y)
$$
Even true for *dependent case*

### Proof
$$
\begin{align}
E[x+y] = \int \int(x+y)f(x,y)dxdy \\
=\int \int xf(x,y)dydx + \int \int yf(x,y)dxdy \\
=\int x \int f(x,y)dydx + \int y \int f(x,y)dxdy \\
=\int xf_{x}(x)dx + \int yf_{y}(y)dy \\
=E[x] + E[Y]
\end{align}
$$

# Notations
$$
E(X), E[X], EX
$$
we can use $\mathbb{E}$ instead of $E$
