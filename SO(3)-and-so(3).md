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
The Lie algebra $`\mathfrak{so(n, R)}`$ consisting of **real skew symmetric $`n \times n`$ matrices** is <br>
the corresponding set of **infinitesimal** rotations.

$`\mathfrak{so(3)}`$ is a special instance of $`\mathfrak{so(n}, \mathbb{R})`$ for $`n=3`.

## How are $`SO(3)`$ and $`\mathfrak{so(3)}`$ related? <sup>Ref[4]</sup>


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
