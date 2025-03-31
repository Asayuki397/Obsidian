# Definition
If $P(X = i) = e^{-\lambda} \cdot \frac{\lambda^i}{i!}$ and $i = 0, 1, \dots$
$$
Poi(\lambda)
$$

# Facts
$$
\sum_{i = 0}^{\infty} e^{-\lambda} \frac{\lambda^i}{i!} = e^{-\lambda}\sum \frac{\lambda^i}{i!} = 1
$$
- [[Expected Value]] $= e^{-\lambda}\sum_{i=0}^\infty i \cdot \frac{\lambda^i}{i!} = \lambda$

Compute [[Moment Generating Function]]
$$
Ee^tx
= \sum e^{ti}e^{-\lambda}\cdot \frac{\lambda^i}{i!} = e^{-\lambda} \sum \frac{(e^t \cdot \lambda)^i}{i!} = e^{-\lambda}e^{e^t\lambda}
 $$
 - [[Variance]] $$
\phi'(t) = \lambda e^t \cdot e^{(e^t-1)\lambda}
$$
$$
\phi''(t)|_{t=0} = E[X^2] = \lambda^2 + \lambda
$$
$$
Var X = E[X^2] - [EX]^2 = \lambda^2 + \lambda - \lambda^2 = \lambda
$$
# Theorem

When $n \to \infty$ and $\lambda$ is fixed, you get:
$$
Bin\left( n, \frac{\lambda}{n} \right) \approx Poi(\lambda)
$$
Note : What this approximation means is like
$$
\lim_{ n \to \infty } P\left( Bin\left( n, \frac{\lambda}{n}  \right)= i \right) = P(Poi(\lambda) = i) 
$$
for every fixed $i$

