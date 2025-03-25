20240625 장민혁

# 14
let the other two values $a, b$ 
since 
$$
\bar{x} = \frac{{a + b + 102 + 100 + 105}}{5} = 104
$$
$$
a+b+102+100+105 = 520
$$
we get:
$$
a + b = 213
$$

since
$$
s^2 = \frac{{(102-104)^2 +(100-104)^2 + (105-104)^2 + (a-104)^2 + (b - 104)^2}}{5-1} = 16 
$$
$$
21 + (a-104)^2 + (b-104)^2 = 64
$$
substituting $b = 213-a$: we get

$$
a^2 -213a +11327 =0
$$
Solving the quadratic equation:
we get:
$$
D =61
$$
$$
 a = \frac{{213\pm \sqrt{ 61 }}}{2}
$$
The two values are:

$$
\frac{{213+\sqrt{ 61 }}}{2}, \frac{{213- \sqrt{ 61 }}}{2}
$$





# 26
## A
| Stem | Leaves          |
| ---- | --------------- |
| 3.4  | 6 8 9           |
| 3.5  | 0 5 6           |
| 3.6  | 1 2 5 6 7 9     |
| 3.7  | 0 1 2 2 2 4 5 9 |
| 3.8  | 0 2 3 6 7       |
| 3.9  | 0 1 3 5 6       |
## B
The sample mean $\bar{x}$:
$$
\bar{x} = \frac{{\sum_{i=1}^nx_{i}}}{n}
$$
The sum is 112.74
dividing it by 30 gives us: 3.758
$$
\bar{x} = 3.7207
$$
## C
The sample standard deviation $s$:
$$
s = \sqrt{ \frac{{\sum_{i = 1}^n}(x_{i}-x)^2}{n-1} } = 0.1457
$$
### D
Calculate the range for $\bar{x}\pm 1.5s$:
$$
[3.5021, 3.9392]
$$
24 out of 30 values are within this range.
$$
Proportion = 0.8
$$
Chebyshev’s inequality for $k = 1.5$
$$
1-\frac{1}{1.5^2} = 0.556
$$
The observed proportion is greater than the lower bound given by the Chebyshev's inequality.

## E
Calculate the range for $\bar{x}\pm 2s$:
$$
[3.4718, 4.0262]
$$
30 out of 30 values are within this range.
$$
Proportion = 1.0
$$
Chbyshev's inequality for $k = 2$
$$
1 - \frac{1}{2^2} = 0.75
$$
The observed proportion is greater than the lower bound given by the Chebyshev's inequality.







# 33
Compute the sample pearson correlation coefficient:
$$
r = {\frac{\sum(x_{i}-\bar{x})(y_{i}-\bar{y})}{\sqrt{ \sum(x_{i}-\bar{x})^2 }\cdot \sqrt{ \sum (y_{i}-\bar{y})^2 }}}
$$
Computing everything:
$$
\begin{align}
\sum x = 156 \\
\sum y = 40.6 \\
\sum x^2 = 2444 \\
\sum y^2 = 140.61 \\
\sum xy = 545.3
\end{align}
$$

We get:
$$
r = \frac{163.2}{269.2} \approx 0.606
$$








# 40

![[output (2).png]]
## A
Since the Gini index is scale-invariant
-> It remains the same

## B
Adding a constant to all values will reduce the relative differences, and will lead to more equal distribution
-> The Gini index will decrease.
