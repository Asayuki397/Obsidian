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

 - limitation of [[Probability mass function]]
 $$
P\left( Bin\left( n, \frac{\lambda}{n} \right)=i \right)
$$ $$
 = \binom{n}{i} \binom{\lambda}{n}^i \left( 1-\frac{\lambda}{n} \right)^{n-i}
$$
$$
= \frac{n(n-1)\dots(n-i+1)}{n^2} \frac{\lambda^i}{i!}\left( 1-\frac{\lambda}{n} \right)^{n-i}
$$

- Summation
Let $$
X_{1} = Poi(\lambda_{1}), X_{2} = Poi(\lambda_{2})
$$ independent Poisson random variable
$$
X_{1} + X_{2} = Poi(\lambda_{1} + \lambda_{2})
$$

Pf. using [[Moment Generating Function]]

$$ 
\mathbb{E}e^{tX} = \mathbb{E}e^{tY}
$$
for all $t \in \mathbb{R}$
$\Rightarrow X,Y$ has same distribution. $$
Ee^{t(X_{1} + X_{2})} = E[e^{tX_{1}} \cdot e^{tX_{2}}] = Ee^{tX_{1}} \cdot Ee^{tX_{2}}
$$
It only applies when $X_{1}, X_{2}$ are independent.
$$
 = e^{(e^t-1)(\lambda_{1} + \lambda_{2})} = \text{M.G.F of} Poi(\lambda_{1 + \lambda_{2}})
$$
It uniquely determines distribution of [[Random Variable]]

- Thinning property of Poisson

	Let $X : Poi(\lambda)$, Every element in X many things is classified as being one of types of $1, 2, \dots, r$ with probability $p_{1}, \dots, p_{r}$ Then, number of k-type = $Poi(p_{k}\lambda)$ & they are independent
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

