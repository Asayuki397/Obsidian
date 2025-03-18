# Example
$$
f(x) = \begin{cases}
c(4x - 2x^2) & (0<x<2) \\
0 & (\text{Otherwise})
\end{cases}
$$

# Fact
$$
P(X \in B) = \int_{B} f(x)dx
$$

# Joint probability density function
$$
P((X,Y) \in B) = \int \int _{B} f(x,y)dxdy
$$
$B\in \mathbb{R}$

# Marginal Probability density function

$$
P(X\in A) = P(X\in A, Y \in \mathbb{R})
$$
$$
= \int \int_{Ax\mathbb{R}} f(x,y)dxdy = \int_{A}\left[ \int_{R} f(x,y)dy \right]dx
$$
when $f(x)$ is marginal probability density function for [[Random Variable]] $X$

Joint -> Marginal
Marginal ->X Joint