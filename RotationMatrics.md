# Rotation Matrics

## Definition


## [SO(3) Group](https://github.com/vitonzhangtt/RoboticsNotes/blob/main/SO(3).md)
The set of $`3 × 3`$ **rotation matrices** forms the **special orthogonal group SO(3)**.

## Properties
Let $`R`$ be a rotation matrix, then the following properties hold:

### Inverse
$`R^{-1}=R^T \in SO(3)`$ <br>
$`RR^{-1}=R^{-1}R=I \text{ and } R^{-1} \in SO(3)`$

### Closure
$`R_{1}R_{2} \in SO(3)`$

### Associative
$`(R_{1}R_{2})R_{3}=R_{1}(R_{2}R_{3})`$

### Not commutative
$`R_{1}R_{2} \neq R_{2}R_{1}`$

### Vector length preservation
Rotating a vector does not change its length. <br>
$`x \in \mathbb{R}^3, \|Rx\|=\|x\|`$

## Use cases

### Frame
Frame(contains fixed frame and body frame) is denoted by $`\{a\}`$. <br>
Let $`\{a\}`$, $`\{b\}`$ and $`\{c\}`$ are three different **body frames**.

### Represent an orientation <sup>Ref[3]</sup>
$`R_{sc}`$: we are representing the frame $`\{c\}`$ of the second subscript <br>
relative to the frame $`\{s\}`$ of the first subscript. <br> 
The subscript is the frame.

$`R_{bc}`$ is the orientation of $`\{c\}`$ relative to $`\{b\}`$.

$`R_{c}`$ is implicitly referring to the orientation of frame $`\{c\}`$ <br>
relative to the **fixed frame** $`\{s\}`$.

$`R_{bc}R_{cb}=I \implies R_{bc}={R_{cb}}^{-1}={R_{cb}}^T`$ 

### Change reference frame <sup>Ref[3]</sup>
The rotation matrix $`R_{ab}`$ represents the orientation of $`\{b\}`$ in $`\{a\}`$, <br>
and $`R_{bc}`$ represents the orientation of $`\{c\}`$ in $`\{b\}`$. <br>
  $`R_{ac} = R_{ab}R_{bc}`$

#### The Subscript Cancellation rule
When multiplying two **rotation matrices**, if the second subscript of the first matrix <br>
matches the first subscript of the second matrix, the two subscripts **“cancel”** and <br>
a change of reference frame is achieved: <br>
$`R_{ab}R_{bc} = R_{a\cancel{b}}R_{\cancel{b}c} = R_{ac}`$

A **rotation matrix** is just a collection of three unit vectors, so the **reference frame** <br>
of a vector can also be changed by a rotation matrix: <br>
$`R_{ab}p_{b} = R_{a\cancel{b}}p_{\cancel{b}} = p_{a}`$

$`p_{b}`$ represent the vector in reference frame $`\{b\}`$, <br>
$`p_{a}`$ represent the vector in reference frame $`\{a\}`$.

### Rotate a vector or frame















## Reference
1. [Modern Robotics, Chapter 3.2.1: Rotation Matrices (Part 1 of 2)](https://www.youtube.com/watch?v=OZucG1DY_sY)
2. [Modern Robotics, Chapter 3.2.1: Rotation Matrices (Part 2 of 2)](https://www.youtube.com/watch?v=6KIPusOv5fA&list=PLggLP4f-rq01NLHOh2vVPPJZ0rxkbVFNc&index=3)
3. [Section 3.2.1.2 Uses of Rotation Matrices from <<Modern Robotics: Mechanics, Planning, and Control>>](https://www.amazon.com/Modern-Robotics-Mechanics-Planning-Control/dp/1107156300)
