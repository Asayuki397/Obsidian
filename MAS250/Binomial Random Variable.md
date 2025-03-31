# Definition
Do n many independent [[Bernoulli Random Variable|Bernoulli trials]] 
$$
X = \text{number of "success"}
$$
called **Binomial Random Variable**

# Notation
$$
Bin(n,p)
$$

# Facts

- [[Expected Value]] $= np$
- [[Variance]] $= Var\left( \sum X_{i} \right) = \sum Var(X_{i}) = np(1-p)$
- [[Probability mass function]] $=P(X=i) = \binom{n}{i}p^i(1-p)^{n-i}$

- let $X_{1} = Bin(n,p), X_{2} = Bin(m,p)$ and $X_{1}, X_{2}$ are independent, then $$
X_{1} + X_{2} = Bin(n+m, p)
$$

# Example
Throw a dice 100 times

let $X = \text{number of multiple of 3} = Bin\left( 100, \frac{1}{3} \right)$
