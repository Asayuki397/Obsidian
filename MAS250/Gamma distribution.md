# Definition

**X is $\Gamma(\alpha, \lambda)$** if

$$
\text{density} = \begin{cases}
\frac{1}{\Gamma(\alpha)} \lambda e^{-\lambda x}(\lambda x)^{\alpha-1} & (x>0) \\
0 & (x\le 0)
\end{cases}
$$

# Facts
- $\Gamma(1,\lambda) : Exp(\lambda)$
	**Theorem** $$
\begin{align}
X_{1}, X_{2}, \dots,X_{n} : \text{independent} \exp(\lambda)  \\
X_{1}+X_{2}+\dots+X_{n} : \Gamma(n, \lambda)
\end{align}
$$

# [[Moment Generating Function]]
$$
\text{MGF of} \Gamma(\alpha, \lambda) = \int_{0}^{\infty} e^{tx} \cdot \frac{1}{p(\alpha)} \lambda e^{-\lambda x} \cdot(\lambda x)^{\alpha-1}dx = \left( \frac{\lambda}{\lambda-t} \right)^\alpha
$$

Matches with the [[Exponential Random Variable]] 's MGF