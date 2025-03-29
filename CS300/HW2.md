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

- **Find the peak element**:
    
    - Traverse the array from left to right.
        
    - Compare each element to its successor until the first element greater than its successor is found. The first decreasing point indicates the peak. (This step requires O(n) time in the worst-case scenario.)
        
- **Split the array into two subarrays**:
    
    - First subarray (left side of peak) is strictly increasing.
        
    - Second subarray (right side of peak) is strictly decreasing.
        
- **Reverse the second subarray**:
    
    - Reverse the second subarray to transform it from decreasing to increasing. (This operation requires O(n) time.)
        
- **Merge both increasing subarrays**:
    
    - Both subarrays are now sorted in increasing order. Merge them into one fully sorted array.
        
    - Merging two sorted arrays can be done in O(n) time by using a standard merge procedure from merge sort.

**Overall Complexity**:

- Finding peak: O(n)
- Reversing second subarray: O(n)
- Merging two sorted subarrays: O(n)

**Total Complexity:** O(n)

# 3
## (a)

### Step 1: Breaking Down the Algorithm

- Divide the $n$ elements into groups of **9** elements.
    
- There are $\lceil n/9 \rceil$ such groups.
    
- Find the median of each group (5th smallest element out of 9) using brute-force, which is $O(1)$ for each group since the group size is constant (9).
    
- Thus, finding medians of all groups takes $O(n)$.
    

### Step 2: Finding the Median-of-Medians

- Recursively apply MY-SELECT to find the median of these medians.
    
- The recursion operates on $m = \left\lceil  \frac{n}{9}  \right\rceil$ elements.
    

### Step 3: Partitioning Based on the Median-of-Medians

- Partition the original array using the median-of-medians (MOM).
    
- This partitioning takes $O(n)$ time.
    

### Step 4: Estimating Recursion Size

When we pick MOM from groups of size 9, how many elements can we guarantee to eliminate?

- At least half of the medians ($\frac{1}{2} \times m$) are smaller or equal to MOM.
    
- Each median corresponds to a group of 9 elements.
    
- Thus, at least half of these groups have 5 elements ≤ MOM (including the median itself).
    
- Thus, number of elements guaranteed to be ≤ MOM is at least:
    

$$
5 \times \frac{1}{2}\left\lceil\frac{n}{9}\right\rceil \approx \frac{5n}{18}
$$
### Step 5: Recurrence Analysis

Thus, we can guarantee at least $\frac{5n}{18}$​ elements are smaller or equal (and similarly, at least $\frac{5n}{18}$​ larger or equal), which ensures recursion on at most:

$$
n - \frac{5n}{18} = \frac{13n}{18}​
$$
The recurrence becomes:

$$
T(n) \le T\left(\frac{n}{9}\right) + T\left(\frac{13n}{18}\right) + O(n)
$$

Let's intuitively verify this is still linear ($O(n)$):

- The total cost is bounded by two subproblems of fractions summing significantly less than nnn.
    
- Using the Master theorem or recursion tree methods, the recurrence leads to $O(n)$.
    

Thus, **MY-SELECT with groups of size 9 remains O(n)**.

## (b)
When duplicates are allowed, the partition step can fail to reduce the problem size significantly:

- The key to the linear complexity is the guaranteed elimination of a fraction of elements at each step.
	
- With duplicates, MY-PARTITION could return an extremely unbalanced partition:
    
    - If the chosen pivot (MOM) equals many duplicates, partitioning might place nearly all elements on one side.
        
    - For example, if nearly all elements equal MOM, MY-PARTITION could return a very skewed partition, with almost no reduction in array size for subsequent recursive calls.
        
- This could lead to recursive calls that shrink only slightly at each iteration, resulting in a recurrence resembling:
$$T(n) \approx T(n-c) + O(n)$$
    where $c$ could be small or constant, thus resulting in worst-case $O(n^2)$ complexity.

Thus, duplicates break the guaranteed fraction reduction required for linear complexity.

## (c)

he main idea is **3-way partitioning** to handle duplicates efficiently:

### Modified MY-PARTITION (3-way partition):

Instead of partitioning into two segments, partition into 3 segments based on pivot $x$:

Elements less than pivot $x$ , Elements equal to pivot $x$, Elements greater than pivot $x$

**Algorithm**
```
MY-3WAY-PARTITION(A[1..n], x):
  lt = 1, i = 1, gt = n
  while i ≤ gt do:
    if A[i] < x:
      swap A[lt] ↔ A[i]
      lt = lt + 1, i = i + 1
    else if A[i] > x:
      swap A[i] ↔ A[gt]
      gt = gt - 1
    else:
      i = i + 1
  return lt, gt

```

This is clearly O(n)

## Modified MY-SELECT algorithm

Change partitioning step to use MY-3WAY-PARTITION and then recurse accordingly

```
MY-SELECT(A[1..n], k):
  if n ≤ 81:
    solve using brute force
  else:
    m = ⌈n/9⌉
    for i = 1 to m do:
      B[i] = MY-SELECT(A[9i−8..9i], 5)
    mom = MY-SELECT(B[1..m], ⌊m/2⌋)
    
    lt, gt = MY-3WAY-PARTITION(A[1..n], mom)
    
    if k < lt:
      return MY-SELECT(A[1..lt−1], k)
    else if k ≤ gt:
      return mom  # Since k-th element is equal to pivot
    else:
      return MY-SELECT(A[gt+1..n], k−gt)

```

## Complexity analysis

- MY-3WAY-PARTITION ensures efficient partitioning even with duplicates.
    
- Each recursive call eliminates a guaranteed fraction of elements, maintaining linear complexity:
    
    - With 3-way partition, duplicates clustered at the pivot are separated efficiently.
        
    - Thus, subsequent recursive calls are guaranteed to operate on reduced array sizes significantly.