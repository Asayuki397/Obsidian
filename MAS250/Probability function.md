$$
P : \{ \text{Set of events} \} \to [0,1]
$$
is *Probability function* if 
- $0 \leq P(E) \leq 1$ for any event $E$
- $P(\{ \text{Sample space} \})$  = 1
- *Countable additivity* For any mutually exclusive events $E_{1}, E_{2}, E_{3}$ (i.e. $E_{i}\cap E_{j} = \emptyset$ for any $i \neq j$) $$
P(U_{i = 1}^nE_{i}) = \Sigma_{i = 1}^n
P(E_{i})$$ here $n$ should be either finite or countable. n can be $\infty$ or $n \in \mathbb{N}$

# Fact
1. $P(\emptyset) = 0$
proof. combine axiom 2+3. $$
P(\{\text{Sample space}\}) = P(\{\text{Sample space}\}) + P(\emptyset)
$$

2. For any event $E$$$
P(E^C) = 1-P(E)
$$
proof. sample space = $E\cup E^C$$$
\therefore 1 = P(E) + P(E^C)
$$
3. $P(E\cup F) = P(E) = P(F) - P(E\cap F)$
proof. divide by three parts by excluding the intersection. use axiom 3
