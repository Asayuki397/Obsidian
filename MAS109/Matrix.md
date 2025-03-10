## 행렬
pl) Matrices

m by n matrix[^1]


![[Pasted image 20250210005719.png]]

- 가로줄을 row, 세로줄을 column 이라고 한다.
- a<sub>ij</sub> = 행렬 ***A***의 element(원소), entry(성분)
- A<sub>(i)</sub> := ![[Pasted image 20250210233732.png]]행렬 ***A***의 i번째 1 by n [[row vector]]

- A<sup>(j)</sup> := ![[Pasted image 20250210233209.png]]행렬 ***A***의 j번째 m by 1 [[column vector]]

![[Pasted image 20250210234806.png]]

- 행렬 ***A***의 행벡터 표현과 열벡터 표현

### Square Matrix
정방행렬, 정사각행렬

_m = n_ => 행렬 ***A*** = \[a<sub>ij</sub>]<sub>n x n</sub>를 n차 Square Matrix 라고 한다.
또한 a<sub>11</sub>, a<sub>22</sub>, ... , a<sub>nn</sub> 을 ***A***의 main diagonal elements 라고 한다.

### Set of Matrices
![[Pasted image 20250212195638.png]]

### Matrices' Equal
***A*** = \[a<sub>ij</sub>], ***B*** = \[b<sub>ij</sub>] ∈ ***M***<sub>m, n</sub> 일 때, ***A***와 ***B***의 원소가 같을 때 두 행렬은 equal이라고 하고 아래와 같이 정의한다.
![[Pasted image 20250212221458.png]]

### Zero Matrix
$$
O = [o_{ij}] \in M_{m, n} : \text{zero matrix}\
\Leftrightarrow o_{ij} = 0, \forall i,j
$$

### Special Matrices
#### Diagonal Matrix
$$
A = \begin{bmatrix}
a_{ij}
\end{bmatrix}
\in M_{n}
\Leftrightarrow
a_{ij} = 0, \forall i \neq j
$$
#### Identity Matrix
$$
I_{n} := \begin{bmatrix}
\delta _{ij} 
\end{bmatrix}
\in M_{n}
\Leftrightarrow
\delta_{ij} := \begin{cases}
1, (i = j) \\
0, (i \neq j)
\end{cases}
$$
**Note : $\delta_{ij}$ : Kronecker Symbol, 크로네커기호**

#### Upper Triangular Matrix
$$
U = \begin{bmatrix}
u_{ij}
\end{bmatrix} \in M_{n}
\Leftrightarrow
u_{ij} = 0, \forall i > j
$$
#### Lower Triangular Matrix
$$
L = \begin{bmatrix}
l_{ij}
\end{bmatrix} \in M_{n}
\Leftrightarrow
l_{ij} = 0, \forall i < j
$$
**Note : $l_{ab} = 1, \forall a = b$ 인 경우 Unit lower triangular matrix라고 한다. 

#### Symmetric Matrix
$$
A = \begin{bmatrix}
a_{ij}
\end{bmatrix} \in M_{n}
\Leftrightarrow
A^t = A
$$
**Note 주대각원소를 중심으로 원소들이 대칭인 배열을 한다.**

#### Skew Symmetric Matrix
TODO
### Operations
- [[Matrices Operations]]
- [[Linear Transformation]]

#### Footnote
[^1]:세로x가로임에 주의하자