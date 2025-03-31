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

Consider a set S of n distinct items. Fix attention on one particular item, call it x.

Now, let's count how many different subsets of size r can be formed from the set S:

- Subsets containing the item x:
    
    To form a subset of size r containing the fixed item x, we must select the remaining r−1 items from the other n - 1 available items. The number of ways to do this is:
    

$$
\binom{n-1}{r-1}
$$

- Subsets NOT containing the item x:
    
    To form a subset of size r without the fixed item x, we must choose all r items from the remaining n - 1 available items. The number of ways to do this is:
    

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

Each die is a six-sided die, and thus each has 6 outcomes. Hence, total outcomes = $6 \times 6 \times 6 = 216$

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
P(W^c|D) = \frac{(0.8)(0.1)}{0.215} = \frac{0.08}{0.215} = \frac{16}{43}
$$

Thus, the probability your neighbor forgot to water the plant given it is dead is $\frac{16}{43}$
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

$$

$$

## (b)

- We already have:
$$
P(E) = \frac{1}{6}
$$
- Probability the second die lands on 3: $$
P(G) = \frac{6}{36} = \frac{1}{6}
$$
- Compute the conditional probability $P(E|G)$:

The outcomes when second die lands on 3 : $(1,3),(2,3),(3,3),(4,3),(5,3),(6,3)$
Only one outcome $(4,3)$ sums to 7, thus:

$$
P(E|G) = \frac{1}{6} = P(E)
$$
Thus, event $E$ and event $G$ are also independent.

# 39
## (a)

Two possible cases:

- HHH _ _
- TTT _ _

Both has $2^2$ possibilities. Thus total outcomes satisfying condition:

$$
4+4 = 8
$$
Hence, probability is:

$$
P = \frac{8}{32} = \frac{1}{4}
$$

## (b)

Define events:

- $A$: first three flips are the same.
- $B$: last three flips are the same.

We already have from (a):
- $P(A) = \frac{1}{4}$

Similarly, event $B$ also has probability:
- Last three flips same:
    - _ _ HHH: 4 ways
    - _ _ TTT: 4 ways  
        Total: 8 ways, hence:
$$
P(B) = \frac{8}{32} = \frac{1}{4}
$$
- Next, calculate intersection $P(A\cap B)$ to subtract double counting:

There are only two : HHHHH and TTTTT

Thus:
$$
P(A\cap B) = \frac{2}{32} = \frac{1}{16}
$$
$$
P(A\cup B) = \frac{1}{4} + \frac{1}{4} - \frac{1}{16} = \frac{7}{16}
$$

## (c)

Label the five coin flips as $A,B,C,D,E$. The two conditions are:

- **Condition C:** Among flips $A,B,C$ there are at least 2 heads.
    
- **Condition D:** Among flips $C,D,E$ there are at least 2 tails.
    

Notice that flip C appears in both groups. We'll consider two cases based on the outcome of flip C.

#### **Case 1:** C = H

- **For Condition C:** With C = H, we need at least one more head from flips A and B. The possible outcomes for (A,B) that have at least one head are: HT, TH, or HH. That gives 3 possibilities.

- **For Condition D:** With C = H, to have at least 2 tails in (C, D, E), both D and E must be tails. There is 1 possibility.

Thus, total outcomes in Case 1: $3 \times 1 = 3$.

#### **Case 2:** C = T

- **For Condition C:** With C = T, we need both A and B to be heads to achieve at least 2 heads. There is 1 possibility (HH).

- **For Condition D:** With C = T, we already have one tail. Now we need at least one tail from flips D and E. The outcomes for (D,E) with at least one tail are: HT, TH, or TT. That gives 3 possibilities.

Thus, total outcomes in Case 2: $1 \times 3 = 3$.

Adding both cases:

$$
\text{Favorable outcomes} = 3+3 = 6
$$

Since there are $2^5$ total outcomes for five coin flips, the probability is:

$$
\text{Probability} = \frac{6}{32} = \frac{3}{16}
$$
# 40
Let

- A be the event that outcome 1 never occurs in n trials, and
- B be the event that outcome 2 never occurs in n trials.

**Step 1. Calculate the probability of A:**  
If outcome 1 never occurs, each trial results in either 0 or 2. The probability of either 0 or 2 is:

$$
P(0 \text{ or } 2) = 0.3 + 0.2 = 0.5
$$

Since the trials are independent, the probability that outcome 1 never appears in all nnn trials is:

$$
P(A) = (0.5)^n
$$

**Step 2. Calculate the probability of B:**  
If outcome 2 never occurs, each trial results in either 0 or 1. The probability of either 0 or 1 is:

$$
P(0 \text{ or } 1) = 0.3 + 0.5 = 0.8
$$

Thus, the probability that outcome 2 never appears in all n trials is:

$$
P(B) = (0.8)^n
$$
**Step 3. Calculate the probability of A∩BA \cap BA∩B:**  
This is the event that neither outcome 1 nor outcome 2 occurs, meaning every trial results in 0. The probability for each trial is:

$$
P(0) = 0.3
$$

So, for n trials:

$$
P(A \cap B) = (0.3)^n
$$

**Step 4. Use the complement (via inclusion-exclusion):**  
We want the probability that both outcome 1 and outcome 2 occur at least once, which is the complement of the event that either outcome 1 or outcome 2 does not occur. Thus, by the principle of inclusion-exclusion:

$$
P(\text{both 1 and 2 occur}) = 1 - \left[P(A) + P(B) - P(A \cap B)\right]
$$

Substitute the probabilities:

$$
P(\text{both 1 and 2 occur}) = 1 - \left[(0.5)^n + (0.8)^n - (0.3)^n\right]
$$

**Final Answer:**

$$
1 - (0.5)^n - (0.8)^n + (0.3)^n
$$
# 45
## (a)

One way to look at a series is to focus on the deciding  part when both teams are equally positioned. Suppose that after several games the remaining wins needed for each team is 3. Then:

- One team’s chance of winning the next 3 games (and thus the series) is $p^3$.
- The other team’s chance is $(1-p)^3$.

Since one of these outcomes must occur, the probability that the team with win–probability p wins the series is the ratio of its chance to win all its remaining games over the total chance for either team:

$$
p_A = \frac{p^3}{p^3 + (1-p)^3}
$$
This fraction gives the desired probability under the assumption that the final “race” is a matter of winning 3 games.

## (b)
Here the idea is to break the overall probability into two cases based on which team is ahead:

1. **If Team A is ahead:**  
    The chance they win the series is increased. In a simplified model, if they need to win fewer games, one way to express this is by calculating the probability that they do _not_ lose all the remaining opportunities. For example, if they need to win at least one out of 4 remaining games, the probability they do not lose all four is
    $$
1 - (1-p)^4
$$
2. **If Team A is behind:**  
    Then they must overcome the deficit. In a symmetric fashion (with roles reversed), the probability they overcome it can be written as
    $$
1-p^4
$$

If we denote by $p_{A}$​ the probability that team A is ahead, then by the law of total probability the overall chance that team A wins the series is

$$
p_A \Bigl(1 - (1-p)^4\Bigr) + (1-p_A)\Bigl(1 - p^4\Bigr)
$$

This expression averages the chances over the two scenarios, weighted by the probability of being ahead or behind.

## (c)

Assume the following situation:

- Two teams are playing a series (for example, best-of-7) and the first game has been won by one team.
- To decide the series, imagine that even after a team reaches 4 wins the teams keep playing a total of 7 games.
- Because the team that wins the first game already has one win, it needs at least 3 wins in the remaining 6 games to secure a total of 4 wins.
    

Under the assumption that each game is independent and each team has a 50–50 chance (i.e. probability 12\frac{1}{2}21​ for each game), the probability that the team wins at least 3 of the next 6 games is calculated by summing the probabilities for winning exactly 3, 4, 5, or all 6 games:

$$
P(W) = \sum_{i=3}^{6} \binom{6}{i} \left(\frac{1}{2}\right)^6
$$

Let’s break down the sum:


- For $i = 3:\binom{6}{3} = 20$
- For $i = 4: \binom{6}{4} = 15$
- For $i = 5 : \binom{6}{5} = 6$
- For $i = 6 : \binom{6}{6} = 1$

Thus,

$$
P(W) = \frac{20 + 15 + 6 + 1}{64} = \frac{42}{64} = \frac{21}{32}
$$

This means that if a team wins the first game, it wins the series with probability $\frac{21}{32}$

# 51

Let's denote the three distinct values by $x_1 < x_2 < x_3$​. The cards A, B, and C receive these values uniformly at random. Notice that the event "the smaller of the values on A and B is smaller than the value on C" is equivalent to saying that card C does not hold the smallest value overall.

Since each card is equally likely to receive any of the three values, the probability that card C gets the smallest value $x_1$ is $\frac{1}{3}$​. Therefore, the probability that card C does not have the smallest value is:

$$
1-\frac{1}{3 } = \frac{2}{3}
$$
The answer is $\frac{2}{3}$