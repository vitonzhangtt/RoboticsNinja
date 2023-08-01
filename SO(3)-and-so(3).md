# $`SO(3)`$ and $`\mathfrak{so(3)}`$

The set of skew-symmetric matrices $`\mathfrak{so(3)}`$ is called the Lie algebra of the Lie group **SO(3)**.

## Lie group $`SO(3)`$

### SO(3) Definition

The following definition is from '1:23:10' in Ref[1]. <br>
$`SO(3)=\{R \in GL_{n}(\mathbb{R}): RR^T = I \text{ and } det(R)=1\}`$

The **special orthogonal group SO(3)**, also known as the group of <br>
**rotation matrices**, is the set of all $`3 × 3`$ real matrices <br>
$`R`$ that satisfy (i) $`R^TR=I`$ and (ii) $`det(R)=1`$. <sup>Ref[2]</sup>

### Property A: $`\text{If }R \in SO(3)\text{, then }R^{-1} = R^T`$

$`RR^{-1}=I \text{ and } RR^T = I \implies R^{-1} = R^T`$

### Property B: $`\text{If }R \in SO(3)\text{, then }R^{-1} \in SO(3)`$

## Lie algebra $`\mathfrak{so(3)}`$

### $`\mathfrak{so(3)}`$ Definition <sup>Ref[5]</sup>

The Lie algebra $`\mathfrak{so}(n, \mathbb{R})`$ consisting of **real skew symmetric $`n \times n`$ matrices** is <br>
the corresponding set of **infinitesimal** rotations.

$`\mathfrak{so(3)}`$ is a special instance of $`\mathfrak{so}(n, \mathbb{R})`$ for $`n=3`.

#### Skew symmetric matrics

For skew symmetric matrics, refer to [skew-symmetric-matrix](https://github.com/vitonzhangtt/LinearAlgebraNinja/blob/main/Concepts.md#skew-symmetric-matrix).

If $`A`$ is a $`n \times n`$ matrix, and $`A = -A^T`$, then $`A`$ is a skew symmetric matrix.

## How are $`SO(3)`$ and $`\mathfrak{so(3)}`$ related? <sup>Ref[4]</sup>

### **Theorem**： If $`A \in \mathfrak{so(3)}`$, then $`e^A \in SO(3)`$.

#### Proof: Orthogonal matrix
Step 1: <br>

If $`A \in \mathfrak{so(3)}`$, then $`A`$ is a skew symmetric matrix. <br>
As a skew symmetric matrix, then $`-A = A^T`$ is hold. <br>
Because A is real matrix, $`A^T = A^H`$($`A^H`$ is [Conjugate transpose](https://github.com/vitonzhangtt/LinearAlgebraNinja/blob/main/Concepts.md#conjugate-transpose-matrix)). <br>
So the following is hold: $`-A = A^T = A^H`$

Step 2: <br>

| Derivation steps | Explanation |
| --- | --- |
| $`e^A{(e^A)}^T=e^A(e^{A^T})`$ |  According to [Theorem 2](https://github.com/vitonzhangtt/LinearAlgebraNinja/blob/main/MatrixExponentials.md#theorem-2ref1-eateat-text-for-any--n-times-n-text-matrix--a), $`(e^A)^T = e^{A^T}`$ |
| $`e^A(e^{A^T})=e^Ae^{-A}`$  | From step 1, $`-A = A^T`$ |
| $`e^Ae^{-A}=e^{A+(-A)}=e^{0_{n \times n}}=I_{n \times n}`$ | According to [Theorem 1](https://github.com/vitonzhangtt/LinearAlgebraNinja/blob/main/MatrixExponentials.md#theorem-1-ref1), and $`A(-A)=(-A)A`$. |

So $`e^A{(e^A)}^T=e^A(e^{A^T})=e^A(e^{A^T})=e^Ae^{-A}`$, then $`e^A`$ is an orthogonal matrix.

#### Proof: $`det(e^A)`$ = 1
For [If $`A`$ is Skew-symmetric, then $`tr(A) = 0`$. ](https://github.com/vitonzhangtt/LinearAlgebraNinja/blob/main/Concepts.md#property-b-if-a-is-skew-symmetric-then-tra--0), then $`det(e^A)=e^{tr(A)}=e^0=1`$ [According to this](https://github.com/vitonzhangtt/LinearAlgebraNinja/blob/main/MatrixExponentials.md#the-determinant-of-the-matrix-exponential-ref5).

#### Proof: $`e^A`$ is real matrix


## Lie group and Lie algebra in Latex <sup>Ref[3]</sup>
By convention a Lie group is denoted by an ordinary Latin letter and its <br>
associated Lie algebra is denoted by the same letter in **Fraktur font**.

## Reference
1. [Lecture 05-Symmetry & Rigid Body Motion](https://www.youtube.com/watch?v=0emGmE3cnjw&list=PLdMorpQLjeXmbFaVku4JdjmQByHHqTd1F&index=6)
2. [Section 3.2.1 Rotation Matrices from <<Modern Robotics: Mechanics, Planning, and Control>>](https://www.amazon.com/Modern-Robotics-Mechanics-Planning-Control/dp/1107156300)
3. [Lie Group and Lie Algebra in Latex](https://www.johndcook.com/blog/2018/07/21/fraktur-math/)
4. [Rotations, SO(3) and so(3)](https://www.youtube.com/watch?v=uILYfubYxd0)
5. [Basics of Classical Lie Groups: The
Exponential Map, Lie Groups, and
Lie Algebras (AAAA)](https://www.cis.upenn.edu/~cis6100/cis61008lie1.pdf)
