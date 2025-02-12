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