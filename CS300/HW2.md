20240625 장민혁

# 1
## (a)

| j   | A[j] | A[j] ≤ 4? | Changes (i, swap)                  | A                                                 |
| --- | ---- | --------- | ---------------------------------- | ------------------------------------------------- |
| 0   | 8    | X         | No changes                         | $\begin{bmatrix}8,2,5,7,1,9,4\end{bmatrix}$       |
| 1   | 2    | O         | $i = 0, A[0] \leftrightarrow A[1]$ | $\begin{bmatrix}2, 8, 5, 7, 1, 9, 4\end{bmatrix}$ |
| 2   | 5    | X         | No changes                         | $\begin{bmatrix}2, 8, 5, 7, 1, 9, 4\end{bmatrix}$ |
| 3   | 7    | X         | No changes                         | $\begin{bmatrix}2, 8, 5, 7, 1, 9, 4\end{bmatrix}$ |
| 4   | 1    | O         | $i = 1, A[1] \leftrightarrow A[4]$ | $\begin{bmatrix}2,1,5,7,8,9,4\end{bmatrix}$       |
| 5   | 9    | X         | No changes                         | $[2,1,5,7,8,9,4]$                                 |
Final result after `PARTITION` : 
$[2,1,4,7,8,9,5]$
Final index of `pivot` = 2
## (b)

Worst case occurs when each `RANDOMIZED-PARTITION` consistently selects the largest or smallest element as pivot. It causes highly unbalanced partitions.

- Initially: Select pivot = 9, partitions into `[8, 2, 5, 7, 1, 4]` and `[]`
- Next step: Select pivot = 8, partitions into `[2, 5, 7, 1, 4]` and `[]`
- Next: pivot = 7, partitions `[2, 5, 1, 4]` and `[]`
- Next: pivot = 5, partitions `[2, 1, 4]` and `[]`
- Next: pivot = 4, partitions `[2, 1]` and `[]`
- Next: pivot = 2, partitions `[1]` and `[]`

Recursion depth `n-1`
Complexity of sorting $\Theta(n^2)$ 

## (c)

- **Best-case scenario:**  
    In the best case, the pivot always splits the array evenly (balanced partition), resulting in the height of the recursion tree being `Θ(log n)`.  
    At each recursion level, a total of exactly `n` elements are partitioned. The total number of calls to RANDOM matches the number of calls to RANDOMIZED-PARTITION, which occurs once per partitioning. Thus, each element is chosen exactly once as pivot, resulting in exactly `n` RANDOM calls in total.  
    **Best-case complexity of RANDOM calls:**  
    **Θ(n)**
    
- **Worst-case scenario:**  
    In the worst case, the partitions are extremely unbalanced. One side always has size `0`, and the other side size `n-1`. This means the algorithm recursively selects pivots `n` times (once per recursion), each pivot choice invoking RANDOM exactly once. Again, this totals exactly `n` RANDOM calls.  
    **Worst-case complexity of RANDOM calls:**  
    **Θ(n)**

# 2

## (a)
**No**, such a permutation does not exist. Every permutation π has the possibility to sort at least one particular bitonic array. Here's why:

- Consider a bitonic array as an increasing sequence up to a single peak and then decreasing.
- Each permutation π corresponds to some ordering of elements. It is always possible to construct a bitonic array specifically matching this permutation's sorted order, by carefully choosing elements in increasing order up to a maximum, and then decreasing afterward.
- Therefore, there does not exist a single permutation π that would fail for every bitonic array. Every permutation can correctly sort at least one specially crafted bitonic array.

## (b)

- The lower bound Ω(n log n) for comparison-based sorting algorithms applies generally because sorting n elements requires distinguishing among all possible permutations (n! permutations), and this inherently requires at least log(n!) = Ω(n log n) comparisons.
- However, for a bitonic array, the number of possible permutations is significantly restricted.
- Specifically, a bitonic array with distinct elements has exactly one peak and therefore only a linear number of possible ways to position this peak. Once the peak position is fixed, the array before and after the peak are monotonically increasing and decreasing, respectively, greatly restricting the structure of possible permutations.
- The key observation is that a bitonic array of length n can be uniquely identified by determining the peak position. Identifying this peak involves at most **n comparisons** (by comparing consecutive elements to detect a decrease).
- Thus, the decision tree depth (number of comparisons) necessary to determine the ordering for any bitonic array is at least proportional to the **linear task** of identifying the peak position, hence Ω(n).

Thus, the lower bound for sorting a bitonic array, using comparison-based sorting, is **Ω(n)**.

## (c)

**Overall Complexity**:

- Finding peak: O(n)
- Reversing second subarray: O(n)
- Merging two sorted subarrays: O(n)

**Total Complexity:** O(n)