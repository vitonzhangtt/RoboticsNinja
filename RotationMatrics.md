# Rotation Matrics

## Definition


## SO(3) Group <sup>Ref[4]</sup>
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

### Change reference frame

### Rotate a vector or frame















## Reference
1. [Modern Robotics, Chapter 3.2.1: Rotation Matrices (Part 1 of 2)](https://www.youtube.com/watch?v=OZucG1DY_sY)
2. [Modern Robotics, Chapter 3.2.1: Rotation Matrices (Part 2 of 2)](https://www.youtube.com/watch?v=6KIPusOv5fA&list=PLggLP4f-rq01NLHOh2vVPPJZ0rxkbVFNc&index=3)
3. [Section 3.2.1.2 Uses of Rotation Matrices from <<Modern Robotics: Mechanics, Planning, and Control>>](https://www.amazon.com/Modern-Robotics-Mechanics-Planning-Control/dp/1107156300)
4. [SO(3)](https://github.com/vitonzhangtt/RoboticsNotes/blob/main/SO(3).md)
