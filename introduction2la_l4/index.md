# MIT 18.06(Linear Algebra) L4 Note


<!--more-->

# 1. Mind Map

![](https://raw.githubusercontent.com/loss4wang/wx_imagehost/main/LA_Lecture_4.png)

# 2. Reading Notes (2.6)

## 2.6 Elimination = Factorization : A = LU

$(E_{32}E_{31}E_{21})A = U \quad\text{becomes }  A = (E_{21}^{-1}E_{31}^{-1}E_{32}^{-1})U \text{which is } A = LU.$

### Explanation and Examples

**Special Pattern**

$A = \begin{bmatrix}
1 & 1 & 0 & 0 \cr
1 & 2 & 1 & 0 \cr
0 & 1 & 2 & 1 \cr
0 & 0 & 1 & 2
\end{bmatrix} = LU
\begin{bmatrix}
1 &  &  &  \cr
1 & 1 &  &  \cr
0 & 1 & 1 &  \cr
0 & 0 & 1 & 1
\end{bmatrix}
\begin{bmatrix}
1 & 1 & 0 & 0 \cr
 & 1 & 1 & 0 \cr
 &  & 1 & 1 \cr
 &  &  & 1
\end{bmatrix}$

Assume no row exchanges, we can predict ***zeros*** in ***L*** and ***U:***

- When a **row** of A starts with zeros, so does that row of **L**.
- When a **column** of A starts with zeros, so does that column of **U**.

**Key reason why A equals LU**

(Row 3 of A)= $l_{31}$(Row 1 of U) + $l_{32}$(Row 2 of U) + 1(Row 3 of U).

This is exactly row 3 of A = LU. That row of L holds  $l_{31}$,  $l_{32}$ , 1. All rows look like this, whatever the size of A. With no row exchanges, we have A= LU.

<aside>
💡 Why explain this?


</aside>

**Better balance from LDU**

A = LU is “unsymmetric”, because U has the pivots on its diagonal where L has 1’s. **Divide U by a diagonal matrix D that contains the pivots.** That leaves a new triangular matrix with l's on the diagonal.

$$
LU =\begin{bmatrix}
1 & 0 \cr
3 & 1
\end{bmatrix}
\begin{bmatrix}
2 & 8 \cr
0 & 5
\end{bmatrix} \text{splits further into }
LDU=
\begin{bmatrix}
1 & 0 \cr
3 & 1
\end{bmatrix}
\begin{bmatrix}
2 & 0 \cr
0 & 5
\end{bmatrix}
\begin{bmatrix}
1 & 4 \cr
0 & 1
\end{bmatrix}
$$

### One Square System = Two Triangular Systems

Matrix L contains memory of Gaussian elimination. 

How do we use it in solving $Ax = b$?

- **Forward (elimination) and backward (substitution)**
  - System $Ax=b$  is factored into **two triangular systems**
  - Solve $Lc = b$
  - and then solve $Ux=c$

Example: 

$$
Ax = b \quad
\begin{cases}u + 2v  &= 5  \cr
4v + 9v &=21  \end{cases}
$$

Forward elimination

$$
Ux = c \quad
\begin{cases}u + 2v  &= 5 \cr
v &=1
\end{cases}
$$



$Lc =b$  The lower triangular system  $\begin{bmatrix}
1 & 0 \cr
4 & 1
\end{bmatrix}
\begin{bmatrix}
c_1 \cr
c_2
\end{bmatrix}
=\begin{bmatrix}
5 \cr
21
\end{bmatrix}$ gave $c =\begin{bmatrix}
5 \cr
1
\end{bmatrix}$

     

$Ux=c$ The upper triangular system  $\begin{bmatrix}
1 & 2 \cr
0 & 1
\end{bmatrix}
\begin{bmatrix}
x_1 \cr
x_2
\end{bmatrix}
=\begin{bmatrix}
5 \cr
1
\end{bmatrix}$ gives $x = \begin{bmatrix}
3 \cr
1
\end{bmatrix}$


