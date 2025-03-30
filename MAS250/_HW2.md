# 11

## **Base case (n = 2)

$$
P(A \cup B) = P(A)  + P(B)  - P(A \cap B )
$$
Since $P(A\cap B) \geq 0$, we get

$$
P(A\cup B) \geq P(A)+P(B) 
$$
Boole's inequality holds

## **Inductive Step (Finite case)

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

## **Extension to countably infinite case**

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

We have proven Boole's inequality holds generally.
# 13

## (a)
Notice that the event $E$ can be partitioned into two disjoint events: $EF$ and $EF^c$. Specifically:

$$
E = (EF) \cup (EF^c), \quad (EF) \cap (EF^c) = \emptyset
$$

Since these events are disjoint, we have:

$$
P(E) = P(EF) + P(EF^c)
$$

Rearranging this equation gives the desired result:

$$
P(EF^c) = P(E) - P(EF)
$$
## (b)

Using De Morgan's Law:

$$
P(E^cF^c) = P((E \cup F)^c) = 1 - P(E \cup F)
$$

Next, use the formula for the probability of a union:

$$
P(E \cup F) = P(E) + P(F) - P(EF)
$$
Thus, we have:

$$
P(E^cF^c) = 1 - [P(E) + P(F) - P(EF)]
$$

Simplify the expression:

$$
P(E^cF^c) = 1 - P(E) - P(F) + P(EF)
$$
This completes the proof.
# 17

## **Algebraic Proof**:
Recall the definition of binomial coefficients:

$$
\binom{n}{r} = \frac{n!}{r!(n - r)!}
$$

Now, algebraically expanding the right-hand side, we have:

$$
\binom{n-1}{r-1} + \binom{n-1}{r} = \frac{(n-1)!}{(r-1)!((n-1)-(r-1))!} + \frac{(n-1)!}{r!(n-1 - r)!}
$$

Simplify the denominators:

$$
= \frac{(n-1)!}{(r-1)!(n - r)!} + \frac{(n-1)!}{r!(n - 1 - r)!}
$$

Factor out common terms carefully by finding a common denominator:

$$
= \frac{(n-1)! \cdot r}{r!(n - r)!} + \frac{(n-1)! (n - r)}{r!(n - r)!}
$$

Combine the fractions:

$$
= \frac{(n-1)! [r + (n - r)]}{r!(n - r)!} = \frac{(n-1)! \cdot n}{r!(n - r)!}
$$

But notice that:

$$
=(nr)\frac{(n-1)! \cdot n}{r!(n - r)!} = \frac{n!}{r!(n - r)!} = \binom{n}{r}
$$

This completes the algebraic proof.

### **Combinatorial Argument (Intuitive Proof):**

Consider a set S of nnn distinct items. Fix attention on one particular item, call it x.

Now, let's count how many different subsets of size r can be formed from the set S:

- Subsets containing the item x:
    
    To form a subset of size rrr containing the fixed item xxx, we must select the remaining r−1 items from the other n - 1 available items. The number of ways to do this is:
    

$$
\binom{n-1}{r-1}
$$

- Subsets NOT containing the item x:
    
    To form a subset of size rrr without the fixed item x, we must choose all rrr items from the remaining n - 1 available items. The number of ways to do this is:
    

$$
\binom{n-1}{r}
$$

Since every subset of size r either contains x or does not, and these two cases are mutually exclusive, the total number of subsets of size r is the sum of the two cases above:

$$
\binom{n}{r}= \binom{n-1}{r-1} + \binom{n-1}{r}
$$

This combinatorial argument directly demonstrates the identity.
# 28

## (a)

Each die is a six-sided die, and thus each has 6 outcomes. Hence, total outcomes = $6 \times 6 \times 6 = 2166$

- Number of outcomes with **no two dice equal**:  
    The first die (say Blue) can show **any of 6 numbers**.  
    The second die (say Yellow) must differ from Blue, thus has **5 choices left**.  
    The third die (Red) must differ from both Blue and Yellow, thus has **4 choices left**.
    

Thus, total outcomes where all three dice differ = $6 \times 5 \times 4 = 120$

Hence, the required probability is:

$$
P(\text{all dice differ}) = \frac{120}{216} = \frac{5}{9}
$$
## (b)

If no two dice land the same, the three numbers are distinct. Now, there are exactly 3!=63! = 63!=6 equally-likely orderings of the three distinct numbers:

$$
B<Y<R,\quad B<R<Y,\quad Y<B<R,\quad Y<R<B,\quad R<B<Y,\quad R<Y<B
$$

Since each ordering is equally likely, the probability that specifically $B<Y<R$ occurs is exactly 1 out of these 6 cases:

Thus, conditional probability:

$$
P(B<Y<R \mid \text{no two dice equal}) = \frac{1}{6}
$$

## (c)
We use conditional probability:

$$
P(B<Y<R) = P(B<Y<R \mid \text{no two dice equal}) \times P(\text{no two dice equal})
$$
From parts (a) and (b):

$$
P(\text{no two dice equal})  =\frac{5}{9}
$$
$$
P(B<Y<R \mid \text{no two dice equal}) = \frac{1}{6}
$$
Thus,
$$
P(B<Y<R) = \frac{1}{6} \times \frac{5}{9} = \frac{5}{54}
$$
## (d)

Since each die has 6 outcomes and they are distinguishable (B, R, Y), the total number of outcomes is:
$$
6×6×6=216
$$
## (e)

We must choose three distinct numbers from the set \{1,2,3,4,5,6\}, and order them uniquely as $B < Y < R$:

- Number of ways to select three distinct numbers from six: $\binom{6}{3}$
- For each choice of three distinct numbers, there is exactly **one ordering** out of the $3! = 6$ that satisfies the strict order $B < Y < R$.

Thus, total outcomes satisfying $B < Y < R$ is:

$$
\binom{6}{3} = \frac{6 \times 5 \times 4}{3 \times 2 \times 1} = 20
$$
## (f)

Using results from (d) and (e):
- Number of outcomes with $B < Y < R : 20$
- Total outcomes: 216

Thus,

$$
P(B < Y < R ) = \frac{20}{216} = \frac{5}{54}
$$

which matches exactly our answer to (c).
# 29

- Let $W$ be the event that your neighbor **waters** the plant.
    
- Let $W^c$ be the event that your neighbor **forgets** to water the plant.
    
- Let $D$ be the event that the plant **dies**.
    
- Let $D^c$ be the event that the plant remains **alive**.

## (a)

We use total probability here:

$$
P(D^c) = P(D^c|W)P(W) + P(D^c|W^c)P(W^c)
$$

Plugging in values, we get:

$$
P(D^c) = (0.85)(0.9) + (0.2)(0.1) = 0.765 + 0.02 = 0.785
$$

Thus, the probability the plant is alive when you return is **0.785**

## (b)

We use **Bayes' theorem** here. The probability we want is $P(W^c|D)$:

$$
P(W^c|D) = \frac{P(D|W^c)P(W^c)}{P(D)}
$$

First, calculate the total probability the plant dies $P(D)$:
$$
P(W^c) = (0.15)(0.9) + (0.8)(0.1) = 0.135 + 0.08 = 0.215
$$
Now, applying Bayes’ theorem:

$$
P(W^c|D) = \frac{(0.8)(0.1)}{0.215} = \frac{0.08}{0.215} \approx 0.3721
$$

Thus, the probability your neighbor forgot to water the plant given it is dead is approximately: **0.3721**
# 36

## (a)

- First, we find probabilities individually:

$$
P(E) = \frac{\text{number of outcomes where sum = 7}}{\text{total outcomes}}
$$

There are 6 ways to roll a sum of 7:

$$
(1,6),(2,5),(3,4),(4,3),(5,2),(6,1)
$$
Thus:

$$
P(E) = \frac{6}{36} = \frac{1}{6}
$$

- The probability the first die lands on 4 is clearly:

$$
P(F) = \frac{6}{36} = \frac{1}{6}
$$

- Now, we compute conditional probability $P(E|F)$:


If the first die lands on 4, outcomes are: $(4,1),(4,2),(4,3),(4,4),(4,5),(4,6)$. 
Only one outcome $(4,3)$ sums to 7, thus:

$$
P(E|F) = \frac{1}{6}
$$

- To check independence, we must verify:

$$
P(E|F) = P(E)
$$

Indeed, we have:

$$
P(E|F) = \frac{1}{6} = P(E)
$$

Thus, event $E$ and event $F$ are independent.

# 39

# 40

# 45
# 47

# 51