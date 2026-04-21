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

## Screw Coordinates (or Screw Parameters, Screw) 

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

### Types of Screw Coordinates

Depending on the application, screw coordinates take two main forms:

* **Twists** (Kinematics): Represent the **motion** of a body.
  * $`\mathcal{V} = (\omega, v)`$, where $`\omega`$ is the **angular velocity** and $`v`$ is the linear velocity of a point <br>
    in the body currently at the origin. 
* **Wrenches** (Statics/Dynamics): Represent the **forces** and **torques** acting on a body.
  * $`\mathcal{F} = (f, m)`$, where $`f`$ is the resultant force and $`m`$ is the total moment about the origin.

### Twists

In kinematics, a twist (represented by the symbol $`\mathcal{V}`$ or $`\xi`$) is a 6-vector that defines the <br>
**instantaneous velocity of a rigid body**. It describes both how fast a body is rotating and how fast a specific <br>
point on it is moving at that exact moment.

#### Vector Structure

A twist is composed of two 3-dimensional vectors: 

<img width="147" height="61" alt="" src="https://github.com/user-attachments/assets/a231bca4-923e-4895-9a75-91a44356a12c" />

* $`\omega`$ (Angular Velocity): A vector representing the axis of rotation and the speed of rotation (magnitude $`|\omega`$ in rad/s).
* $`v`$ (Linear Velocity): The instantaneous linear velocity of a point in the rigid body that is currently at the <br>
  origin of the reference frame. 

#### Mathematical Description <sup>[8]</sup>

<img width="464" height="202" alt="page 4 from [8]" src="https://github.com/user-attachments/assets/c504c29c-bf8a-4962-bdcd-029fd9bce48f" /> <br>

NOTE: $`\hat{a}`$ is the skew-symmetric matrix representation of vector $`a`$.

##### The Bottom Component: $`\omega`$
  * What it is: The angular velocity vector.
  * Role: It defines the axis the body is rotating around and how fast it is spinning (in rad/s).

##### The Top Component: $`- \omega \times q + h\omega`$

This represents the **linear velocity** $`v`$ of the body at the origin(NOTE: The origin is in the <br>
**Stationary Frame** that is also called the **Space Frame**, **World Frame**, or **Fixed Frame**.). <br>
It is made of two distinct physical effects:

* Part A: $`- \omega \times q`$ (The "Swing" Velocity)
  * $`q`$ is a vector pointing from the origin to any point on the **screw axis**.
  * This term accounts for the **velocity created by rotation** when the axis is not passing through the origin.
  * If you are spinning a wheel whose center is 5 meters away ($`q`$), the origin (where you are) feels a "wind" <br>
    or velocity because of that distance.
* Part B: $`+h\omega`$ (The "Slide" Velocity)
  * $`h`$ is the pitch of the screw.
  * In a **true screw motion** (like a bolt in a nut), the object doesn't just rotate; it also **slides** along the axis.
  * Since $`\omega`$ points along the axis, $`h\omega`$ represents the **linear translation speed** occurring <br>
    simultaneously with the rotation.

##### Symbols

|Symbol |	Meaning |
| -| -|
|$`\xi`$ | The Twist: the complete description of the rigid body's motion. |
|$`\omega`$|Angular Velocity: direction and speed of rotation.|
|$`q`$|**Position Vector**: a point on the rotation axis relative to the origin.|
|$`h`$|Pitch: the linear distance moved per radian of rotation.|
|$`- \omega \times q`$|Velocity at the origin due to rotation at a distance.|
|$`h \omega`$|Velocity at the origin due to translation along the axis.|

#### Geometrical Description

<img width="266" height="238" alt="" src="https://github.com/user-attachments/assets/2fdddf15-1093-4d5a-b41e-85f919eb0170" />

In screw theory, a twist provides the **geometrical description** of a rigid body's **instantaneous velocity**. <br>
It treats the entire body's motion as a combined **rotation** about and **translation** along a single line in space, <br> 
known as the **Instantaneous Screw Axis** (ISA).

##### Screw Axis ($`l`$): 

A **directed line** in space that serves as both the axis of rotation and the direction of translation. It is often
represented using [**Plücker coordinates**]() to define its position and direction.

To compute the Screw Axis from twist ($`\xi`$), we need to find two things: the direction of the axis and a point 
$`q`$ on that axis.

###### Find the Direction

The direction of the axis is simply **the unit vector of the angular velocity** $`\omega`$.

The unit vector: $`\hat{s} = \frac{\omega}{\lVert \omega \rVert}`$

###### Find a Point $`q`$ on the Axis

The point $`q`$ is the location of the axis relative to your origin. Since an axis is an **infinite line**, <br>
we usually calculate the point $`q`$ that is closest to the origin.

$`q = \frac{\omega \times v}{{\lVert \omega \rVert}^2}`$

* Why this works: The cross product $`\omega \times v`$ finds the vector perpendicular to both the rotation <br>
  and the velocity at the origin, pointing directly toward the axis. Dividing by $`{\lVert \omega \rVert}^2`$ scales <br>
  it to the correct physical distance.

###### Screw Motion (The General Case)

<img width="143" height="51" alt="" src="https://github.com/user-attachments/assets/18fe4ae4-02c8-4c1e-bc08-ff558b1329b6" />

This is the most important formula for the **Chasles-Mozzi Theorem**. It calculates the axis location directly <br>
from the Twist ($`\omega, v`$). 

* The First Term ($`\frac{\omega \times v}{{\lVert \omega \rVert}^2}`$): This identifies **the point on the axis** <br>
  **closest to the origin**.
* The Second Term ($`\lambda \omega`$): This "stretches" that point into an infinite line pointing in the
  direction of the rotation $`\omega`$. 

###### Pure Rotation

<img width="102" height="26" alt="" src="https://github.com/user-attachments/assets/d32a3b43-057d-41ba-bd0c-3bbdb6529c3b" />

* What it represents: A body spinning around a fixed axis with no sliding.
* $`q`$: A specific point on the axis.
* $`\omega`$: The direction of the axis.

**Explanation**: The line starts at point $`q`$ and extends infinitely in the direction of the rotation vector $`\omega`$.

###### Pure Translation

<img width="70" height="25" alt="" src="https://github.com/user-attachments/assets/45a0ff36-fca6-414b-b98f-e180fab15fa4" />

* What it represents: The body is moving in a straight line with zero rotation ($`\omega = 0`$).
* Explanation: In this case, there is no "rotation axis." Instead, the "axis" of motion is simply a line passing
  through the origin in the direction of the velocity vector $`v`$.
* **Note**: Because there is no rotation, the point $`q`$ from the previous formulas becomes irrelevant or undefined.

##### Pitch $`h`$

To compute the pitch ($`h`$) using the vectors of a twist $`\xi = [\omega, v] ^{T}`$, you use the following formula:

$`h = \frac{\omega \cdot v}{{\lVert \omega \rVert}^2}`$

* Calculate the Dot Product <br>
  <img width="367" height="31" alt="" src="https://github.com/user-attachments/assets/bfc8d951-0afc-4cde-8d55-aa2a6e7df89b" />
* Calculate the Squared Magnitude <br>
  <img width="333" height="30" alt="" src="https://github.com/user-attachments/assets/d5c1ea09-f997-4c1c-a980-e9b8911907e6" />

###### Final Formula

<img width="226" height="59" alt="" src="https://github.com/user-attachments/assets/14ddd45c-b228-441d-b0f5-8d288927e915" />

The result tells you exactly **how many units of distance** the body translates along its axis for every <br>
**one radian it rotates**.

###### Understanding the Result

* $`h = 0`$: The rotation and linear velocity are perpendicular ($`\omega \cdot v = 0`$). This occurs in <br>
  **pure rotation** where there is no sliding along the axis.
* $`h \neq 0`$: The body is performing a **screw motion**, sliding along the axis as it turns.
* $`h \rightarrow \infty`$: If $`\omega = 0`$ but $`v \neq 0`$, the motion is a **pure translation**. <br>
  Mathematically, the pitch is undefined or infinite because there is no rotation to relate the translation to.

##### Magnitude ($`M`$)

The **magnitude of a displacement** (often called the **twist magnitude**) depends on whether the motion involves <br>
rotation or is a pure translation. It is the scalar value that describes "how much" the body has moved.

###### 1. If there is Rotation ($`\omega \neq 0`$)

The magnitude is defined as the **angle of rotation** $`\theta`$. 

* Formula: $`M = \lVert \omega \rVert`$
* Units: Typically in **radians**.
* Interpretation: The total amount the body turned around the screw axis. 

###### 2. If it is Pure Translation ($`\omega = 0`$)

The magnitude is defined as the linear distance $`d`$. 

* Formula: $`M = \lVert v \rVert`$
* Units: Typically in **meters** or **units of length**.
Interpretation: The straight-line distance the body moved.

###### Relationship Between Components

Once you have the magnitude ($`M`$), you can relate the translation and rotation through the pitch($`h`$):

* Translation distance ($`d`$): $`d = h \times \theta`$ (only if $`\theta`$ is the magnitude).
* Total Twist: $`V = S\dot{\theta}`$, where $`S`$ is the unit screw axis and $`\dot{\theta}`$ is **the magnitude** <br>
  **of the velocity** (rate of displacement).

### A Numerical Example of Twist

#### 1. Define the Twist
Assume a rigid body has the following angular velocity $`\vec{\omega}`$ and linear velocity $`\vec{v_o}`$ **at the origin**: 

* Angular Velocity: $`\vec{\omega} = (0, 0, 2)`$ **rad/s**.
* Linear Velocity **at Origin**: $`\vec{v_o} = (4, -2, 1)`$ **m/s**.

#### 2. Calculate the Pitch
The pitch $`h`$ represents the ratio of translational speed along the axis to the rotational speed. 
It is found by projecting $`\vce{v_o}`$ onto $`\vec{\omega}`$:

<img width="476" height="59" alt="" src="https://github.com/user-attachments/assets/fd0b0898-1a3f-4dba-aaba-70367a689aa2" />

Geometric Meaning ($`h = 0.5`$): For every $`1`$ radian of rotation, the body slides $`0.5`$ meters along the axis.

#### 3. Locate a Point on the Axis

The screw axis is shifted away from the origin by a vector $`\vec(q)`$. This point $`\vec(q)`$ is where the <br>
"tangential" component of the origin's velocity (the part caused by being off-center) exactly cancels the <br>
perpendicular component of $`\vec{v_o}`$:

<img width="727" height="106" alt="" src="https://github.com/user-attachments/assets/594b53de-0fcb-4c09-9679-a5344d2cb602" />

Geometric Meaning: The center of rotation (the axis) is located $`1`$ unit away on the $`x`$-axis and 2 units 
away on the $`y`$-axis.

#### 4. Interpret the Result

The screw axis is a line passing through the point $`(1, 2, 0)`$ and pointing in the direction of $`(0, 0, 1)`$.

* Any point on this axis has a velocity of $`v_{axis}`$: $`v_{axis} = h \times (0, 0, 2) = (0, 0, 1)`$ **m/s**.
* The motion looks like a bolt being screwed into a hole: it rotates at $`2`$ **rad/s** while sliding forward <br>
  at $`1`$ **m/s** along the $`z`$-direction.

<img width="442" height="422" alt="" src="https://github.com/user-attachments/assets/f2ceb6c6-be6a-44ae-80fa-3f4a7948df12" />

#### Linear Velocity at Origin

In screw theory, **the linear velocity at the origin** ($`\vec{v_o}`$) is the velocity a point on the rigid body <br>
would have if it were located at $`(0,0,0)`$ at that exact moment.

Think of it as a "reference snapshot" rather than the movement of the entire object. 

##### 1. It’s a "Point-Specific" Velocity

A rigid body in screw motion doesn't have just one linear velocity. Because the body is rotating, every point <br>
on the body has a different velocity vector. **We pick the origin as a standard reference point** to define the "Twist."

##### 2. It is composed of two parts

The vector $`\vec{v_o}`$ (in our example: $`4i - 2j + 1k`$) is the sum of:
* The Translation: The movement of the actual screw axis itself.
  * The $`1k`$(z-component) is the "true" sliding motion (the pitch).
* The Tangential Velocity: The speed caused by the origin's distance from the screw axis (the "spinning" effect).
  * The $`(4, -2)`$ ($`x`$ and $`y`$ components) is purely "phantom" velocity caused by the fact that the origin <br>
    is sitting at a distance from the rotation axis. 

##### 3. The "Remote Hand" Analogy

Imagine you are holding a long, rigid pole. If you rotate the pole while walking forward, the tip of the pole 
(the origin) moves in a wide, fast arc, while your hand (the axis) moves in a straight line. $`\vec{v_o}`$ is the
velocity of that tip.








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
8. [Screw Theory](https://ethz.ch/content/dam/ethz/special-interest/mavt/robotics-n-intelligent-systems/multiscaleroboticlab-dam/documents/trm/HS2019/Slides/03_2019-10-14_ScrewTheory.pdf)
9. Book: `A Mathematical Introduction to Robotic Manipulation` (1994)
10. [Relationship Between Plücker, Screw, and Twist Coordinates](https://medium.com/@tahsincankose/relationship-between-pl%C3%BCcker-screw-and-twist-coordinates-4f32835129d1)
