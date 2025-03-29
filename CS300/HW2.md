20240625 장민혁

# (a)

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
# (b)

Worst case occurs when each `RANDOMIZED-PARTITION` consistently selects the largest or smallest element as pivot. It causes highly unbalanced partitions.

- Initially: Select pivot = 9, partitions into `[8, 2, 5, 7, 1, 4]` and `[]`
- Next step: Select pivot = 8, partitions into `[2, 5, 7, 1, 4]` and `[]`
- Next: pivot = 7, partitions `[2, 5, 1, 4]` and `[]`
- Next: pivot = 5, partitions `[2, 1, 4]` and `[]`
- Next: pivot = 4, partitions `[2, 1]` and `[]`
- Next: pivot = 2, partitions `[1]` and `[]`

Recursion depth `n-1`
Complexity of sorting $\Theta(n^2)$ 

# (c)

Best case scenario : The pivot always splits the array evenly.
- Height of the recursion tree : $\Theta(\log n)$
The total number of calls 