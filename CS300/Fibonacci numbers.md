# *Naive* recursive algorithm

## Recursive Definition : 

$$
F_{n} = 
\begin{cases}
0 & (n = 0) \\
1 & (n = 1) \\
F_{n-1} + F_{n-2} & (n \leq 2)
\end{cases}
$$

	0 1 1 2 3 5 8 13 21 34 ...

```
function fib1(n)
if n = 0: return 0
if n = 1: return 1
return fib1(n-1) + fib1(n-2)
```

## Analysis

- Let Y(n) denote *computer steps* needed to compute fib1(n).
- T(n) $\leq$ 2 for $n \leq 1$.
- $T(n) = T(n-1) + T(n-2) + 3 \space \text{for} \space n > 1$
- $T(n)$ is *exponential in n!* ~ very slow except for very small n

# *Better* algorithm

```
function fib2(n)
if n = 0 return 0
create an array f[0...n]
f[0] = 0, f[1] = 1
for i = 2...n:
	f[i] = f[i-1] + f[i-2]
return f[n]
```

#### $\Theta(n)$ time


