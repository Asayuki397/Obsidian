# Definition

$$
z_{1}, \dots, z_{n} \text{ are independent}
$$
and follows [[Standard Normal Distribution]]

$$
z_{1}^2 + \dots + z_{n}^2
$$
is called Chi-square with n degrees of freedom

# Notation
$$
\chi^2_{n}
$$
# Facts
- [[Expected Value]] = n
- [[Variance]]$$
\sum_{i=1}^n Var(z_{i}^2) = 2n
$$
- $\chi_{n}^2$, $\Gamma\left( \frac{n}{2}, \frac{1}{2} \right)$ has same[[Probability density function | density]]
	proof) using MGF
	$$
Ee^{t\chi^2_{n}} = Ee^{t(z_{1}^2 + \dots + z_{n}^2)} = \left( \frac{\frac{1}{2}}{\frac{1}{2} - t} \right)^{n/2} =\int e^{tx^2} \frac{1}{\sqrt{ 2\pi }}e^{-x^2/2}dx = \frac{1}{\sqrt{ 1-2t }}
$$
while $t < \frac{1}{2}$
