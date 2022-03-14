# MIT 18.06(Linear Algebra) L2 Note


# 1. Mind Map
![](https://raw.githubusercontent.com/loss4wang/wx_imagehost/main/LA_Lecture_2.png)

# 2. Reading Notes(2.2-2.3)

## 2.2 The Idea of Elimination

A systematic way to solve linear equations: elimination

- GOAL: produce an **upper triangular system**
- The system **solved from the bottom upwards: back substitution**
- **Pivot** : first nonzero in the row that does the elimination
- Multiplier : (entry to eliminate) divided by (pivot)

### Breakdown of Elimination

**Failure**: The method might ask us to divide by zero.

- Permanent failure with no solution.
- Failure with infinitely many solutions.

---

- Elimination leads to an equation  $0 \neq 0$ (no solution) or 0 = 0 (many solutions)

Success comes with n pivots. But we may have to **exchange** the n equations.

### Three Equations in Three Unknowns

Goal: Forward elimination is complete from A to U.

### Elimination from A to U

- Column 1. Use the first equation to create zeros below the first pivot.
- Column2. Use the new equation2 to create zeros below the second pivot.
- Columns 3 to n. Keep going to find all n pivots and the upper triangular U.

## 2.3 Elimination Using Matrices

### Matrices times Vectors and Ax = b

- $Ax=b$
  - Ax **is a combination of columns of A**
  - **Components of Ax are dot products with rows of A.**

### The Matrix Form of One Elimination Step

$Ax=b:
\begin{bmatrix}2&4&-2
\cr 4&9&-3
\cr -2&-3&7
 \end{bmatrix}
\begin{bmatrix} -1
\cr 2
\cr 2
 \end{bmatrix}
=\begin{bmatrix}2
\cr 8
\cr 10
 \end{bmatrix}$

- First step: Subtract 2*Row1 from Row2
  - Elimination matrix is $E = \begin{bmatrix}1&0&0
    \cr -2&1&0
    \cr 0&0&1
     \end{bmatrix}$
  - $b_{new} = Eb$
  - $\begin{bmatrix}1&0&0
    \cr -2&1&0
    \cr 0&0&1
     \end{bmatrix}
    \begin{bmatrix} 2
    \cr 8
    \cr 10
     \end{bmatrix}
    =\begin{bmatrix}2
    \cr 4
    \cr 10
     \end{bmatrix}$
  - $\begin{bmatrix}1&0&0
    \cr -2&1&0
    \cr 0&0&1
     \end{bmatrix}
    \begin{bmatrix}b_1
    \cr b_2
    \cr b_3
     \end{bmatrix}
    = \begin{bmatrix}b_1
    \cr -2b_1+b_2
    \cr b_3
     \end{bmatrix}$
- **I: identity matrix $\begin{bmatrix}1&0&0
  \cr 0&1&0
  \cr 0&0&1
   \end{bmatrix}$**
- **E :elementary matrix or elimination matrix**
  - $E_{ij}$  has extra nonzero entry $-l$ in the i,j position. Then $E_{ij}$  subtracts a multiple $l$ of row j from row i.
  - $E_{31} = \begin{bmatrix}1&0&0
    \cr 0&1&0
    \cr -l&0&1
     \end{bmatrix}$
  - **The purpose of** $E_{31}$ **is to produce a zero in the ( 3, 1) position of the matrix.**
  - **Products and inverses** are especially clear for E's. It is those two ideas that the book will use.

### Matrix Multiplication

Q: **How do we multiply two matrices?**

- $E(Ax) =Eb \quad{also}\quad (EA)x = Eb$
- Associative law is true
- Commutative law is false
- E on the **rights** acts on the **columns** of A
- E on the **left** acts on the **rows** of A

**Matrix multiplication:**

$AB = A [b_1,b_2,b_3]=[Ab_1,Ab_2,Ab_3]$

### The Matrix $P_{ij}$ for a Row Exchange

**Permutation Matrix**

- A row exchange is needed when zero is in the pivot position.

$$
\begin{bmatrix}1&0&0
\cr 0&0&1
\cr 0&1&0
 \end{bmatrix}
\begin{bmatrix}2&4&1
\cr 0&0&3
\cr 0&6&5
 \end{bmatrix}
= \begin{bmatrix}2&4&1
\cr 0&6&5
\cr 0&0&3
 \end{bmatrix}
$$

- Row Exchange Matrix $P_{ij}$ is the identity matrix with rows i and j reversed.

### The Augmented Matrix

$$
\text{Augmented matrix} [A\quad b] = \begin{bmatrix} 2&4&-1&2
\cr 4&9&-3&4
\cr -2 &-3&7&10
\end{bmatrix}
$$


