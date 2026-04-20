# Screw Theory (螺旋运动)

A **screw** can be used to denote the **linear and angular velocity** of a rigid body. <sup>[2]</sup>

## What is Screw Theory

Screw theory is a mathematical framework used in robotics and mechanics to describe rigid body motion and <br>
forces by combining translation and rotation about a single axis. Developed by **Sir Robert Ball** in the late <br>
19th century, it simplifies **kinematics and dynamics** into **6D vectors**, known as **twists** (velocity) and <br>
**wrenches** (force).

## Screw Theory and Lie Theory

Screw theory and Lie theory are deeply intertwined in robotics and kinematics, where screw theory provides <br>
the geometric, **intuitive description** of rigid-body motion (twists/wrenches). **Lie theory** provides the <br>
rigorous **analytic foundation**, identifying screws as elements of the Lie algebra $`so(3)`$ corresponding to <br>
the Lie group $`SO(3)`$ of finite rigid-body transformations.

## Chasles-Mozzi theorem

The **Chasles-Mozzi theorem** states that any rigid body displacement in 3D space is equivalent to a **screw** <br> 
**displacement**—a rotation about a specific axis combined with a translation along that same axis. This <br>
kinematic principle shows that all 3D motions, no matter how complex, can be decomposed into a rotation ($`\theta`$) <br>
and a linear shift ($`d`$) along a "screw axis".

* **Screw Axis** (Helical Axis): The unique line about which the combined rotation and translation occur.
* Decomposition: A general motion can be separated into a rotation ($`\phi`$) around an axis and a <br>
  translation ($`t`$) parallel to that axis.
* Application: Essential in kinematics and robotics for simplifying motion analysis, avoiding singularities <br>
  inherent in Euler angles.
* Origins: Named after **Michel Chasles** and **Ottaviano-Fabrizio-Mossoti**, it extends Euler’s rotation theorem, <br>
  which states that a rotation with a fixed point is simply a rotation about an axis.

## Screw Coordinates (or Screw Parameters) 

Screw coordinates (or screw parameters) define a rigid body's spatial motion—a combination of rotation about <br>
an axis and translation along it—using a **6-parameter vector** or a **4x4 matrix**. They represent **twists** <br>
(velocities) or **wrenches** (forces) in robotics and kinematics. Key components include the **screw axis**, <br>
**direction**, **pitch** (ratio of linear to angular motion), and **amplitude**. 

* Representation: A **screw** is defined by a 6-vector, which can be broken down into a **3D unit angular velocity** <br>
  ($`\omega`$) and **3D linear velocity** ($`v`$) of the frame's origin.
* Pitch ($`h`$): **The ratio of the linear speed to angular speed along the axis**. A pitch of zero represents <br>
  **pure rotation**, while infinite pitch represents **pure translation**.
* Exponential Coordinates: Used in robotics to express a displacement from an initial configuration to a target <br>
  configuration, usually defined by a screw axis ($`S`$) and total rotation ($`\theta`$).
* **Plücker Coordinates**: When the **pitch is zero**, screw coordinates are identical to Plücker line coordinates, <br>
  representing 3D lines.
* Applications: Essential for kinematics, statics, path planning, and analyzing spatial mechanisms, often <br>
  simplifying problems compared to traditional DH parameters.

## Plücker Coordinates

Screw coordinates are built on top of **Plücker coordinates**, which are a way of representing lines. <sup>[6]</sup>

Plücker coordinates are a way to represent lines in 3D space using a six-dimensional homogeneous vector. <br>
While **a 3D line only has four degrees of freedom**, these coordinates provide a compact, linear representation <br> 
that simplifies complex geometric operations like finding intersections between lines and planes. 

### Geometric Definition

A line in space is represented by two vectors, often denoted as ($`l, m`$): 

* Direction Vector ($`l`$): The displacement vector between any two distinct points $`P_1`$ and $`P_2`$ on the line ($`l = P_1 - P_2`$).
* Moment Vector ($`m`$): The cross product of a point on the line and the direction vector ($`m = P_1 \times l`$). <br>
  This vector is **perpendicular** to the plane containing the line and the origin, and its **magnitude** represents <br>
  twice the area of the triangle formed by the origin and the two points.

<img width="570" height="210" alt="Figure 1 from [7]" src="https://github.com/user-attachments/assets/6bd6bd6d-bade-4816-8b34-dca83ec8bd58" />

### Key Mathematical Properties

* Homogeneity: The vectors $`(l, m)`$ and $`(\lambda l, \lambda m)`$ represent the same line for any non-zero scalar $`\lambda`$.
* Plücker Constraint: Because the moment vector $`m`$ is defined as a cross product involving the direction $`l`$, <br>
  they must always be orthogonal. This is expressed by the dot product $`l \cdot m = 0`$.
* Distance to Origin: The shortest distance from the coordinate origin to the line is given by the ratio of the <br>
  magnitudes of the two vectors: $`\frac{\lVert m \rVert}{\lVert l \rVert} `$. 

### How to calculate the distance to origin?

Before we calculate the shortest distance from origin to the line, we should find the $`p_{\perp}`$ which is the <br>
unique point on the line such that the vector from the origin to the point is **perpendicular** to the line's direction.

Therefore, $`p_{\perp}`$ must satisfy two conditions:

* It is on the line: $`p_{\perp} \times l = m`$
* It is perpendicular to the direction: $`p_{\perp} \cdot l = 0`$

First let's give the conclude: $`p_{\perp} = \frac{l \times m}{{\lVert l \rVert}^2}`$, and then prove that.

#### The Algebraic Proof of The Conclude

We start with the [**Vector Triple Product Identity**](https://byjus.com/jee/vector-triple-product/) (the **BAC-CAB** rule):

$`a \times (b \times c) = b(a \cdot a) - c(a \cdot b)`$

Let $`a = l`$, $`b = p_{\perp}`$, and $`c = l`$. Substituting these into the identity: 

$`l \times (p_{\perp} \times l ) = p_{\perp}(l \cdot l) - l(l \cdot p_{\perp})`$

* Substitute $`p_{\perp} \times l`$ with $`m`$.
* Substitute $`l \cdot l`$ with $`{\lVert l \rVert}^2`$.
* Substitute $`l \cdot p_{\perp}`$ with $`0`$ (because they are perpendicular).

The equation simplifies to: $`l \times m = p_{\perp} {\lVert l \rVert}^2 - 0`$

Then solving for $`p_{\perp}`$: $`p_{\perp} = \frac{l \times m }{{\lVert l \rVert}^2}`$

Finally, The distance from the origin to the line is the magnitude of this vector $`\lVert p_{\perp} \rVert`$:

$`Distance = \lVert \frac{l \times m}{{\lVert l \rVert}^2} \rVert = \frac{\lVert l \times m \rVert}{{\lVert l \rVert}^2}`$

Since $`l`$ and $`m`$ are always perpendicular in Plücker coordinates ($`90^{\circ}`$ angle), the magnitude 
of their cross product is $`\lVert l \rVert \lVert m \rVert sin(90^{\circ}) = \lVert l \rVert \lVert m \rVert`$:

$`Distance = \frac{\lVert l \times m \rVert}{{\lVert l \rVert}^2} = \frac{\lVert l \rVert \lVert m \rVert}{{\lVert l \rVert}^2} = \frac{\lVert m \rVert}{\lVert l \rVert}`$

If $`m = 0`$, the distance is $`0`$, meaning the line passes directly through the origin.

### Why does a 3D line have four degrees of freedom?

## Books

* Robots and Screw Theory: Applications of Kinematics and Statics to Robotics (Davidson & Hunt) [2004]






# Reference
1. [Lecture 7: Screw Theory, Exponential Coordinates, and Forward Kinematics](https://publish.illinois.edu/ece470-intro-robotics/files/2023/02/07-lecture-slides.pdf) from [`ECE470/AE482/ME445 || Introduction to Robotics`](https://publish.illinois.edu/ece470-intro-robotics/)
2. [](https://opentextbooks.clemson.edu/me8930/chapter/introduction-to-lie-theory-and-its-application-to-robotics)
3. Lecture 6:[Chpater 6](https://publish.illinois.edu/ece470-intro-robotics/files/2025/09/06-lecture-raw.pdf)
4. Lecture 7:[Screw Theory, Exponential Coordinates, and Forward Kinematics](https://publish.illinois.edu/ece470-intro-robotics/files/2023/02/07-lecture-slides.pdf)
5. [Geometry and Screw Theory for Robotics](http://alvarestech.com/temp/RoboAseaIRB6S2-Fiat/geometry_and_screw_theory_for_robotics.pdf)
6. [Lecture 9 Representing displacements](https://www.cs.cmu.edu/afs/cs/academic/class/16741-s07/www/lectures/Lecture9.pdf) from `Mechanics of Manipulation`
7. [Plücker Coordinates for Lines in the Space](https://faculty.sites.iastate.edu/jia/files/inline-files/plucker-coordinates.pdf)
