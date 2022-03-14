# Introduction2LA_L3

<!--more-->

# 1. Mind Map

![](https://raw.githubusercontent.com/loss4wang/wx_imagehost/main/LA_Lecture_3.png)

# 2. Reading Notes (2.4-2.5)

## 2.4 Rules for Matrix Operations

### 4 ways to find AB. (matrix multiplication)

- Take the dot product of each row of A with each column of B.
- Each column of AB is a combination of the columns of A. (Matrix A times every column of B)
- Every row of AB is a combination of the rows of B. (Every row of A times matrix B)
- Multiply columns 1 to n of A times rows 1 ton of B. Add those matrices.

### The Laws for Matrix Operations

- Addition Law
  - commutative law
  - distributive law
  - associative law
- Multiplication Law
  - associative law for ABC
  - distributive law from the left
  - distributive law from the right
- Law of exponents
  - $A^{P} = AAA\cdots A\text{(p factors)}$
  - $(A^p)(A^q)=A^{p+q}$
  - $(A^p)^q=A^{pq}$

### Block Matrices and Block Multiplication

- $\begin{bmatrix}
  I & 0 \cr
  -CA^{-1} & I
  \end{bmatrix}
  \begin{bmatrix}
  A & B \cr
  C & D
  \end{bmatrix}
  = \begin{bmatrix}
  A & B \cr
  0 & D-CA^{-1}B
  \end{bmatrix}$
- Block elimination produces the **Schur complement** $D-CA^{-1}B$.

## 2.5 Inverse Matrices

- Two sided inverse $A^{-1}A = AA^{-1}=I$
- **IMPORTANT: If A is invertible, then Ax = 0 can only have the zero solution $x = A^{-1}0 = 0$.**
- OR: If Ax = 0 for a nonzero vector x, then A has no inverse.

### The Inverses of a Product AB

If A and B are invertible then so is AB. Then inverse of a product AB is

$(AB)^{-1}=B^{-1}A^{-1}$

- **Inverse of AB**
- $(AB)B^{-1}A^{-1} = AIA^{-1} = AA^{-1}=I$
- $(ABC)^{-1}= C^{-1}B^{-1}A^{-1}$

**Inverse of an elimination matrix**

$E=\begin{bmatrix}1&0&0
\cr -5 & 1 & 0
\cr 0 & 0 & 1
 \end{bmatrix}
\quad and \quad
E^{-1} =\begin{bmatrix}1&0&0
\cr 5 & 1 & 0
\cr 0 & 0 & 1
 \end{bmatrix}$

For square matrices, an inverse on one side is automatically an inverse on the other side.

$F=\begin{bmatrix}1&0&0
\cr -0 & 1 & 0
\cr 0 & -4 & 1
 \end{bmatrix}
\quad and \quad
F^{-1} =\begin{bmatrix}1&0&0
\cr 0 & 1 & 0
\cr 0 & 4 & 1
 \end{bmatrix}$

- **In elimination order F follows E. In reverse order $E^{-1}$ follows  $F^{-1}$.**
- $FE=\begin{bmatrix}1&0&0
  \cr -5 & 1 & 0
  \cr 20 & -4 & 1
   \end{bmatrix}
  \quad \text{is inverted by }
  E^{-1}F^{-1} =\begin{bmatrix}1&0&0
  \cr 5 & 1 & 0
  \cr 0 & 4 & 1
   \end{bmatrix}$
- $E^{-1}F^{-1}$ is quick. **The multipliers 5, 4 fall into place below the diagonal of 1 's.**

### Calculating $A^{-1}$ by Gauss-Jordan Elimination

Each of the columns $x_1,x_2,x_3$ of $A^{-1}$ is multiplied by $A$ to produce a column of $I$:

- $AA^{-1} = A\begin{bmatrix} x_1&x_2&x_3\end{bmatrix} =
  \begin{bmatrix} e_1&e_2&e_3\end{bmatrix} = I$
- $Ax_1=e_1=(1,0,0);Ax_2=e_2;\cdots$

**The Gauss-Jordan method computes $A^{-1}$ by solving all n equations together.**

- $\begin{bmatrix}
  K & e_1 & e_2 & e_3
  \end{bmatrix}
  =\begin{bmatrix}
  K & I
  \end{bmatrix}
  \Rightarrow 
  \begin{bmatrix}
  I & x_1 & x_2 & x_3
  \end{bmatrix}
  =\begin{bmatrix}
  I & K^{-1}
  \end{bmatrix}$

### Singular verus Invertible

- $A^{-1} \text{ exists exactly when A has a full set of n pivots.(Row exchange allowed)}$
- **A triangular matrix is invertible if and only if no diagonal entries are zero.**

### Recognizing an Invertible Matrix

**Diagonally dominant matrices are invertible.（Unnecessary and sufficient condition）**

- Diagonally dominant matrices are invertible.
- $|a_{ii}| >  \sum_{j\neq i}|a_{ij}|$
- $\text{Example: } 
  \begin{bmatrix}
  3 & 1 & 1 \cr
  1 & 3 & 1 \cr
  1 & 1 & 3
  \end{bmatrix}$


