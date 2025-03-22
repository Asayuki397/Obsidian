# Definition

X is continuous [[Random Variable]]

If there is non-negative function $f(x)$ such that for any $B \subseteq \mathbb{R}$,$$
P(X\in B) = \int _{B} f(x)dx
$$
This f is called [[Probability density function]]

# Fact
1. Take $B = [a, b]$$$
P(a \leq X \leq b) = \int_{a}^{b}f(x)dx
$$
2. Take $B = {c}$ $$
P(X = c) = \int_{c}^{c} f(x)dx = 0
$$
3. Take $B = \mathbb{R}$ #important $$
P(X \in \mathbb{R}) = \int_{-\infty}^{\infty} f(x) \, dx = 1 
$$
4. $F' = f$ $$
F(x) = P(X\leq x) = \int_{-\infty}^{x} f(t)dt \, dx $$
$$
\frac{d}{dx}F(x) = f(x)
$$
# Probability functions
- [[Probability mass function | Joint probability mass function]]
- [[Probability mass function|Marginal probability mass function][]