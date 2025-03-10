Datas: $(X_{1}, Y_{1}),\space (X_{2}, Y_{2}), \cdots (X_{n}, Y_{n})$

## Definition

$$
r = \frac{\Sigma_{i=1}^n(X_{i}-\bar{X})(y_{i}-\bar{y})}{\sqrt{ \Sigma_{1}^n(X_{i}-\bar{X})^2}\cdot\sqrt{\Sigma_{1}^n(y_{i}-\bar{y})^2 }}
$$

- r > 0 : Positively correlated
- r < 0 : Negatively correlated
- r = 0 : uncorrelated

## Property
- $-1\leq r \leq 1$
- $r = 1 \Leftrightarrow y_{i} = a + bX_{i}, b>0$
- $r = -1 \Leftrightarrow y_{i} = a+bX_{i} b< 0$
- Sample correlation coefficient of $(a + bX_{i}, c + dy_{i}) \rightarrow \text{(sign of the bd)}\cdot r$

## Proof
### Cauchy-Schwarz inequality
$$
\Sigma(\frac{X_{i}-\bar{X}}{S_{x}}-\frac{y_{i}-\bar{y}}{S_{y}})^2
$$
$$
= \Sigma \frac{(X_{i}-\bar{X})^2}{S_{x}^2} +\frac{(y_{i}-\bar{y})^2}{S_{y}^2} - 2 \Sigma \frac{(X_{i}-\bar{X})(y_{i}-\bar{y})}{S_{x}S_{y}}
$$
$$
=(n-1) + (n+1) - 2(n-1)r
$$
$$
\therefore r\leq 1
$$

Simillary, $r \leq 1$
