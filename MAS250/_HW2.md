# 11

## Base case (n = 2)

$$
P(A \cup B) = P(A)  + P(B)  - P(A \cap B )
$$
Since $P(A\cap B) \geq 0$, we get

$$
P(A\cup B) \geq P(A)+P(B) 
$$
Boole's inequality holds

## Inductive Step (Finite case)

Assume Boole's inequality holds for n events:

$$
P\left(\bigcup_{i=1}^{n} A_i\right) \leq \sum_{i=1}^{n}P(A_{i})
$$

We now prove it for n+1 events. Consider:

$$
P\left( \bigcup _{i=1}^{n+1} A_{i} \right) = P\left( \left( \bigcup_{i=1}^{n}A_{i} \right) \cup A_{n+1} \right)
$$

Applying the two-event inequality from above, we have:

$$
P\left(\left(\bigcup_{i=1}^{n} A_i\right) \cup A_{n+1}\right) \leq P\left(\bigcup_{i=1}^{n} A_i\right) + P(A_{n+1})
$$


By the inductive hypothesis, this becomes:

$$
\leq \sum_{i=1}^{n} P(A_i) + P(A_{n+1}) = \sum_{i=1}^{n+1} P(A_i)
$$

Thus, by mathematical induction, Boole’s inequality holds for all finite n.

## Extension to countably infinite case

Consider a countably infinite sequence of events $A_1, A_2, A_3, \dots$ Define:

$$
B_n = \bigcup_{i=1}^{n} A_i
$$

Then $B_{n}$​ is an increasing sequence of events, and we have:

$$
\lim_{n \to \infty} B_n = \bigcup_{i=1}^{\infty} A_i
$$

Using continuity of probability measures (countable monotonicity), we have:

$$
P\left(\bigcup_{i=1}^{\infty} A_i\right) = \lim_{n \to \infty} P(B_n)
$$

Using the inequality for finite n proven above, we have for each n:

$$
P(B_n) = P\left(\bigcup_{i=1}^{n} A_i\right) \leq \sum_{i=1}^{n} P(A_i)
$$

Taking limits as $n \to \infty$:

$$
P\left(\bigcup_{i=1}^{\infty} A_i\right) = \lim_{n \to \infty} P(B_n) \leq \lim_{n \to \infty} \sum_{i=1}^{n} P(A_i) = \sum_{i=1}^{\infty} P(A_i)
$$
# 13

# 17

# 28

# 29

# 36

# 39

# 40

# 45
# 47

# 51