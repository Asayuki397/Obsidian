Assignment 1. 20240625 장민혁 

Problem 1. 

(a) 

[수식] 

P(n-1) : The total number of users who have seen the meme by the previous hour.  

2P(n-1) : The number of new users exposed to the meme in the current hour, which is twice the number of users who have already seen it. 

+1: The influencer who learns about the meme separately in the current hour. 

(b) 

1st unroll : [수식] 

2nd unroll : [수식] 

kth unroll : [수식] 

base case : 

When k = n, we reach the base case P(0) = 1: 

[수식] 

Final non-recursive formula (using the formula for the sum of a geometric series) 

[수식] 

Complexity (grow rate) : 

Exponential, [수식] 

 Problem 2. 

Inductive hypothesis :  

Let’s assume that for all [수식] 

Substitute the inductive hypothesis into the recurrence relation:
$$
T(n) = 5T\left( \frac{n}{5} \right)\log\left( \frac{n}{5}
\right)
$$

Using the inductive hypothesis:
$$
T\left( \frac{n}{5} \right) \leq c_{1} \left( \frac{n}{5} \right) \log \left( \frac{n}{5} \right) + n
$$
Simplify:
$$
T(n) \leq c_{1} n \log \left( \frac{n}{5} \right) + n
$$
$$
T(n) \leq c_{1}n \log n - c_{1}n \log 5 + n
$$
We want to show that $c_{1}n  \log n$
We need:
$$
-c_{1}n \log 5 + n \leq 0
$$
This implies:
$$
c_{1} \geq \frac{1}{\log 5}
$$
Which is not like our initial hypothesis, $c{1 \geq \frac{1}{\log 5}}$
If $n = 1, T(1) \leq 0$, which may not hold.

Let's use the form $T(k) \leq c_{1}(k - c_{2}) \log(k-c_{2})$ from the hint.


