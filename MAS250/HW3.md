# 10

## (a)
A function is a valid joint probability density function if:

$$
\int_0^1 \int_0^2 f(x, y)\, dy\, dx = 1
$$

So we compute:

$$
\int_0^2 \frac{6}{7}\left(x^2 + \frac{xy}{2}\right)\, dy\, dx = \frac{6}{7} \int_0^1 \int_0^2 \left(x^2 + \frac{xy}{2}\right)\, dy\, dx
$$

**Inner integral (with respect to y):**

$$
\int_0^2 \left(x^2 + \frac{xy}{2}\right)\, dy = \int_0^2 x^2\, dy + \int_0^2 \frac{xy}{2}\, dy = x^2(2) + \frac{x}{2} \cdot \frac{2^2}{2} = 2x^2 + \frac{x}{2} \cdot 2 = 2x^2 + x
$$

**Outer integral (with respect to x):**

$$
\frac{6}{7} \int_0^1 \left(2x^2 + x\right)\, dx = \frac{6}{7} \left[\frac{2x^3}{3} + \frac{x^2}{2}\right]_0^1 = \frac{6}{7} \left(\frac{2}{3} + \frac{1}{2}\right) = \frac{6}{7} \cdot \frac{7}{6} = 1
$$

it **is** a valid joint density function.

## (b)


The marginal density of X, denoted by $f_X(x)$, is obtained by integrating out y:

$$f_X(x)=\int_0^2 f(x,y)\,dy = \int_0^2 \frac{6}{7}\left(x^2+\frac{xy}{2}\right)dy$$

From our previous calculation in part (a), we already computed:

$$
\int_0^2 \left(x^2+\frac{xy}{2}\right)dy = 2x^2+x
$$

Thus,

$$
f_X(x)=\frac{6}{7}\left(2x^2+x\right),\quad 0<x<1
$$

## (c)

We need to find the probability that X>Y. Since the support is 0<x<1 and 0<y<2, the condition X>Y implies that y must be less than x.

Thus, the probability is given by:

$$
P(X>Y)=\int_{0}^1\int_{0}^{x} f(x,y)\,dy\,dx
$$

First, compute the inner integral with respect to y:

$$
\int_0^x \left(x^2+\frac{xy}{2}\right)dy = x^2\int_0^x dy+\frac{x}{2}\int_0^x y\,dy
$$

- The first term:
$$
x^2\int_0^x dy = x^2\cdot x = x^3
$$
- The second term:
$$
\frac{x}{2}\int_0^x y\,dy = \frac{x}{2}\cdot\frac{x^2}{2} = \frac{x^3}{4}
$$

Thus,

$$
\int_0^x \left(x^2+\frac{xy}{2}\right)dy = x^3+\frac{x^3}{4} = \frac{5x^3}{4}
$$

Now, substitute back into the double integral:

$$
P(X>Y)=\int_{0}^{1}\frac{6}{7}\cdot\frac{5x^3}{4}\,dx = \frac{30}{28}\int_{0}^{1} x^3\,dx
$$
And compute the remaining integral:

$$
\int_0^1 x^3\,dx = \frac{1}{4}
$$
Thus,

$$
P(X>Y)=\frac{15}{14}\cdot\frac{1}{4}=\frac{15}{56}
$$
# 13
## (a)

To find the marginal density of X, integrate f(x,y) with respect to y. For a given x, note that y must satisfy x<y<1 (and x must be between 0 and 1).

$$
f_X(x)=\int_{y=x}^{1} f(x,y)\,dy=\int_{y=x}^{1} 2\,dy=2\int_{y=x}^{1} dy=2(1-x)
$$

for 0<x<1. Otherwise, $f_X(x)=0$
## (b)

To find the marginal density of Y, integrate f(x,y) with respect to x. For a given y, the variable x must satisfy 0<x<y (with y between 0 and 1).

$$
f_Y(y)=\int_{x=0}^{y} f(x,y)\,dx=\int_{x=0}^{y} 2\,dx=2\int_{x=0}^{y} dx=2y
$$

for 0<y<1. Otherwise, $f_Y(y)=0$.
## (c)

Two random variables X and Y are independent if and only if

$$
f(x,y)=f_X(x)f_Y(y)
$$

for all x and y.

Thus, their product is

$$
f_X(x)f_Y(y)=\bigl[2(1-x)\bigr]\bigl[2y\bigr]=4y(1-x)
$$

Compare this to the joint density $f(x,y)=2$ for $0<x<y<1$. Clearly,

$$
2 \neq 4y(1-x)
$$

for all (x,y) in the support. For example, at $x = 0.25$ and $y=0.5$
Since the joint density does not factor as a product of the marginal densities, **X and Y are not independent**.

# 16
Given that X and Y are independent with density functions $f_X(x)$ and $f_Y(y)$ respectively, we know their joint density is

$$f_{X,Y}(x,y)=f_X(x)f_Y(y)$$

We will derive each result using the definition of probability and Fubini's theorem.
## (a)

1. **Start with the definition:**$$P\{X+Y\le a\} = \iint_{x+y\le a} f_X(x)f_Y(y) \, dx\,dy$$
2. **Change the order of integration:**
    Fix a value of y. For each y, the condition$x+y\le a$ becomes $x\le a-y$. Thus, the integral can be rewritten as:
$$P\{X+Y\le a\} = \int_{-\infty}^{\infty} \left[\int_{-\infty}^{a-y} f_X(x) \, dx \right] f_Y(y) \, dy$$
3. **Recognize the inner integral as the CDF of X:**
$$\int_{-\infty}^{a-y} f_X(x) \, dx = F_X(a-y)$$
4. **Substitute back:**$$P\{X+Y\le a\} = \int_{-\infty}^{\infty} F_X(a-y) f_Y(y) \, dy$$

### (b)
1. **Start with the definition:**
$$P\{X\le Y\} = \iint_{x\le y} f_X(x)f_Y(y) \, dx\,dy$$
2. **Change the order of integration:**
    For a fixed y, the condition $x\le y$ means x ranges from $-\infty$ to y. Thus, we have:
$$P\{X\le Y\} = \int_{-\infty}^{\infty} \left[\int_{-\infty}^{y} f_X(x) \, dx \right] f_Y(y) \, dy$$
3. **Recognize the inner integral as the CDF of X:**
  $$\int_{-\infty}^{y} f_X(x) \, dx = F_X(y)$$
4. **Substitute back:**
$$P\{X\le Y\} = \int_{-\infty}^{\infty} F_X(y) f_Y(y) \, dy$$

# 20
## (a)

1. **Definition of Independence:**  
    X and Y are independent if, for all x and y,
$$p_{X,Y}(x,y)=p_X(x)p_Y(y)$$
2. **Definition of Conditional Probability:**  
    For $p_Y(y)>0$, the conditional probability of X given $Y=y$ is defined by
$$p_{X|Y}(x|y)=\frac{p_{X,Y}(x,y)}{p_Y(y)}$$
3. **Proof that Independence Implies $p_{X|Y}(x|y)=p_X(x)$:**  
    If X and Y are independent,
$$p_{X|Y}(x|y)=\frac{p_X(x)p_Y(y)}{p_Y(y)}=p_X(x)$$

4. **Proof of the Converse:**  
    Conversely, assume that for all x and y (with $p_Y(y)>0$) we have
$$p_{X|Y}(x|y)=p_X(x)$$
    Then, by the definition of conditional probability,
$$\frac{p_{X,Y}(x,y)}{p_Y(y)}=p_X(x)$$
    which implies
$$p_{X,Y}(x,y)=p_X(x)p_Y(y)$$
    This is exactly the definition of independence. Hence, X and Y are independent.

### Continuous Case

1. **Definition of Independence:**  
    X and Y are independent if, for all x and y,
$$f_{X,Y}(x,y)=f_X(x)f_Y(y)$$
2. **Definition of Conditional Density:**  
    For $f_Y(y)>0$, the conditional density of X given $Y=y$ is defined by
$$f_{X|Y}(x|y)=\frac{f_{X,Y}(x,y)}{f_Y(y)}$$
3. **Proof that Independence Implies $f_{X|Y}(x|y)=f_X(x)$:**  
    If X and Y are independent,
    $$f_{X|Y}(x|y)=\frac{f_X(x)f_Y(y)}{f_Y(y)}=f_X(x)$$
4. **Proof of the Converse:**  
    Conversely, assume that for all x and y (with $f_Y(y)>0$) we have$$f_{X|Y}(x|y)=f_X(x)$$Then, by the definition of conditional density,
    $$\frac{f_{X,Y}(x,y)}{f_Y(y)}=f_X(x)$$
    which implies
$$f_{X,Y}(x,y)=f_X(x)f_Y(y)$$
    This is the definition of independence. Thus, X and Y are independent.

# 29

## (a)

Let $M = \max(X_1, \dots, X_n)$

1. **Find the CDF of M:**
    Since the $X_i$​ are independent,$$F_M(x)=P(M \le x)=P(X_1 \le x, \dots, X_n \le x)=\prod_{i=1}^n P(X_i \le x)=x^n,\quad 0\le x\le 1$$
2. **Differentiate to get the density function of M:**
    $$f_M(x)=\frac{d}{dx}F_M(x)=nx^{n-1},\quad 0\le x\le 1$$
3. **Compute the expected value:**
$$E[M]=\int_0^1 x\,f_M(x)\,dx=\int_0^1 x\cdot nx^{n-1}\,dx=n\int_0^1 x^n\,dx.$$
    The integral is
$$\int_0^1 x^n\,dx=\frac{1}{n+1}$$
    Therefore,
$$E[M]=n\cdot\frac{1}{n+1}=\frac{n}{n+1}$$

## (b)

Let $m = \min(X_1, \dots, X_n)$.

1. **Find the CDF of m:**
$$F_m(x)=P(m \le x)=1-P(m > x)=1-P(X_1 > x,\dots,X_n > x)$$
    Since $P(X_{i}​>x)=1−x \text{ for } 0≤x≤1$, we have
$$P(m > x)=(1-x)^n$$
    hence,
$$F_m(x)=1-(1-x)^n,\quad 0\le x\le 1$$
2. **Differentiate to get the density function of m:**
$$f_m(x)=\frac{d}{dx}F_m(x)=n(1-x)^{n-1},\quad 0\le x\le 1$$
3. **Compute the expected value:**
$$E[m]=\int_0^1 x\,f_m(x)\,dx=n\int_0^1 x(1-x)^{n-1}\,dx.
    $$
    Recognize that the integral is a Beta integral. In general,
$$\int_0^1 x^{a-1}(1-x)^{b-1}\,dx=B(a,b)=\frac{\Gamma(a)\Gamma(b)}{\Gamma(a+b)}$$
    Here, set $a=2$ and $b=n$:
$$\int_0^1 x(1-x)^{n-1}\,dx = B(2,n)=\frac{\Gamma(2)\Gamma(n)}{\Gamma(n+2)}$$

    Since $\Gamma(2)=1! = 1$ and $\Gamma(n+2)=(n+1)n\,\Gamma(n)$, we have
$$B(2,n)=\frac{1\cdot\Gamma(n)}{(n+1)n\,\Gamma(n)}=\frac{1}{n(n+1)}$$
    Thus,

$$E[m]=n\cdot\frac{1}{n(n+1)}=\frac{1}{n+1}$$

# 33
### (a) Using Indicators for Each Draw

1. **Define the Indicators:**
    
    For $i = 1, 2, \dots, 10$ let
    $$X_i = \begin{cases} 1, & \text{if the \(i\)th ball drawn is white}, \\ 0, & \text{otherwise}. \end{cases}$$
    Then, $$X = \sum_{i=1}^{10} X_i$$
2. **Calculate the Expectation:**
    
    By symmetry (each draw is equally likely to be any ball from the urn), the probability that a given draw is white is
    $$P(X_i = 1) = \frac{17}{40}$$
    Therefore,
    
    $$E[X_i] = \frac{17}{40}$$
    Using the linearity of expectation,
    $$E[X] = \sum_{i=1}^{10} E[X_i] = 10 \cdot \frac{17}{40} = \frac{170}{40} = \frac{17}{4} = 4.25$$

### (b) Using Indicators for Each White Ball

1. **Define the Indicators:**
    
    For each white ball $j = 1, 2, \dots, 17$ let
$$Y_j = \begin{cases} 1, & \text{if white ball \(j\) is selected in the 10 draws}, \\ 0, & \text{otherwise}. \end{cases}​$$
    Then,
$$X = \sum_{j=1}^{17} Y_j$$
2. **Calculate the Expectation:**
    Since 10 balls are chosen out of 40, the probability that any specific white ball is selected is
$$P(Y_j = 1) = \frac{10}{40} = \frac{1}{4}$$
    Thus,
$$E[Y_j] = \frac{1}{4}$$
    Then, by linearity of expectation,
    $$E[X] = \sum_{j=1}^{17} E[Y_j] = 17 \cdot \frac{1}{4} = \frac{17}{4} = 4.25$$

# 35

![[Pasted image 20250408223929.png]]

# 40
![[Pasted image 20250409214409.png]]
# 50
![[Pasted image 20250409214432.png]]
# 52 & 54

![[Pasted image 20250409214450.png]]

# 57
![[Pasted image 20250409214517.png]]