## 행렬의 연산

[[Matrix]]를 수학적 대상으로 다루기 위해 필요한 기본적인 기본연산들을 다룬다.

### Addition and Subtraction
Let,
$$
A = \begin{bmatrix}
a_{ij}
\end{bmatrix}, B = \begin{bmatrix}
b_{ij}
\end{bmatrix} \in M_{m, n}
$$ 
1. Addition
$$
A + B = \begin{bmatrix}
a_{ij}
\end{bmatrix} + \begin{bmatrix}
b_{ij}
\end{bmatrix} := \begin{bmatrix}
a_{ij} + b_{ij}
\end{bmatrix}
$$
2. Subtraction
$$
A - B = \begin{bmatrix}
a_{ij}
\end{bmatrix} - \begin{bmatrix}
b_{ij}
\end{bmatrix} := \begin{bmatrix}
a_{ij} - b_{ij}
\end{bmatrix}
$$
3. Basic Properties
![[Pasted image 20250213033208.png]]

#### Note
교환법칙 : Commutative Property
결합법칙 : Associative Property
항등원 : Identity Element
역원 : Inverse Element

### Scalar Multiplication
#### Definition
$$
A = \begin{bmatrix}
a_{ij}
\end{bmatrix} \in M_{m, n}, k \in \mathbb{R}
$$
일 때, 다음과 같이 정의한다.

$$
kA = k \left[ a_{ij} \right] := \left[ ka_{ij} \right] = \left[ \begin{array}{cccc}
ka_{11} & ka_{12} & \cdots & ka_{1n} \\
ka_{21} & ka_{22} & \cdots & ka_{2n} \\
\vdots & \vdots & \ddots & \vdots \\
ka_{m1} & ka_{m2} & \cdots & ka_{mn}
\end{array} \right]

$$
#### Basic Properties
![[Pasted image 20250214225931.png]]

### Multiplication of Matrices
$$
AB := \begin{bmatrix}
c_{ij}
\end{bmatrix} \in M_{m, n}, c_{ij} := a_{i1}b_{1j} + a_{i2}b_{2j} + \cdot + a_{ip}b_{pj} = \sum_{k = 1}^{p} a_{ik}b_{kj}
$$
**Note  : Commutative Property does not hold**$$
AB \neq BA
$$
#### Expression with Row Vector and Column Vector
$$
A = \begin{bmatrix}
a_{ik}
\end{bmatrix} \in M_{m, p}, B = \begin{bmatrix}
b_{kj}
\end{bmatrix} \in M_{p,n}
$$
일 때, 다음이 성립한다; 
$$A_{(i)}B^{(j)} = \begin{bmatrix}
a_{i1} & a_{i2} & \cdots & a_{ip}
\end{bmatrix}
\begin{bmatrix}
b_{1j} \\ b_{2j} \\ \vdots \\ b_{pj}
\end{bmatrix} = \sum_{k = 1}^p a_{ik}b_{kj}
$$
$$
(AB)_{(ij)} = A_{(i)} B^{(j)}
$$
$$
AB = \begin{bmatrix}
A_{(1)}B^{(1)} & A_{(1)}B^{(2)} & \cdots  & A_{(1)}B^{(n)} \\
A_{(2)}B^{(1)} & A_{(2)}B^{(2)} & \cdots & A_{(2)}B^{(n)} \\
\vdots & \vdots &   & \vdots \\
A_{(m)} B^{(1)} & A_{(m)}B^{(2)} & \cdots & A_{(m)}B^{(n)} \\
\end{bmatrix}
$$
$$
(AB)_{(i)} = A_{(i)}B, (AB)^{(j)} = AB^{(j)}
$$
### Exponentiation of Matrices
$$
A = \begin{bmatrix}
a_{ij} 
\end{bmatrix}
$$