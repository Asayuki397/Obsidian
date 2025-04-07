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


