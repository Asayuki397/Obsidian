# Notations

![[Pasted image 20250309011433.png]]
**Theta is the tight bound**

$$
\begin{align}
\Theta(g(n)) = \{f(n) \text{ : There exist positive constants } c_{1},c_{2} \text{ and } n_{0} \\
\text{ s.t. } 0 \leq c_{1}g(n) \leq f(n) \leq c_{2}g(n)
\text{ for all }n \geq n_{0} \}
\end{align}
$$

Here, $g(n)$ is an *asymptotic tight bound* for $f(n)$

asymptotic : 점근적인

$O(n)$ provides *asymptotic upper bound*
$\Omega (n)$ provides *asymptotic lower bound*
$o(n)$ when $f(n)$ is *asymptotically smaller* than $g(n)$
$\omega(n)$ when $f(n)$ is *asymptotically larger* than $g(n)$

$$
f(n) = \Theta(g(n)) \iff f(n) = O(g(n)) \cap f(n) = \Omega (g(n))
$$

# Properties

### Let $f,g,h : \mathbb{N} \to \mathbb{R}^*$

1. Transitivity (Holds for all notations)$$
f \in O(g) \cap g \in O(h) \Rightarrow f \in O(h)
$$
2. Duality $$
\begin{gather}
f \in O(g) \iff g \in \Omega(f) \\
f \in o(g) \iff g \in \omega(f)
\end{gather}
$$
3. Symmetry(Only holds for $\Theta$)
$$f \in \Theta(g) \Rightarrow g \in \Theta(f)$$
4. $\Theta$ is an equivalence relation
> From deepseek:
> ![[Pasted image 20250309021700.png]]
5. $$
O(f+g) = O(max\{f,g\})
$$
# Theorem

$\log n$ is in $o(n^\alpha)$ for any $\alpha>0$. $n^k$ is in $o(2^n)$ for any $k>0$.
