# Angular Velocity and Rotation

## Angular Velocity <sup>Ref[2]</sup>

### Physics for Angular Velocity <sup>Ref[7]</sup>
Angular Velocity is denoted by $`\omega`$. 

#### Period and Frequency

**Period** is time that it takes to make one complete cycle, and is denoted by $`T`$. <br>
The unit for period is seconds.

**Frequency** is the number of cycles that occurs per second, and is denoted yb $`f`$. <br> 
The unit for frequency is Hertz ($`Hz`$).

The relation of Period and Frequency is $`T=\frac{1}{f}`$.

$`\omega = 2{\pi}f = \frac{2\pi}{T}`$

### Centripetal Acceleration
Centripetal acceleration (denoted by $`A_{c}`$) points towards the center of cicle.

$`A_{c} = \frac{V^2}{R}`$ <br>
$`V = {\omega}R`$ <br>
$`A_{c} = \frac{V^2}{R}=\frac{({\omega}R)^2}{R}={\omega}^2{R}`$

If an object is moving with constant speed around a circle, the only  <br>
acceleration it has is the **centripetal acceleration** also known as the <br>
**radial acceleration**.

### Tangential Acceleration

$`A_{tan} = {\alpha}R`$  $`{\alpha}`$ is Angular Acceleration.
Tangential acceleration and Centripetal acceleration are 
prependicular to each other.

### Math for Angular Velocity 
The following snapshot at **9:22** in Ref[2]. <br>
There are three axises: $`x, y`$ and $`z`$, $`z`$ axis points to the screen. <br>
$`\vec{a}`$ is the axis of rotation in 3D and $`\vec{a}`$ is unit vector. <br>
$`\vec{x}`$ is the vector which rotates about rotation axis $`\vec{a}`$. <br>
$`\dot{\theta}`$ is the change in angle. <br>

$`\vec{v}`$ is a **velocity vector** and a vector which is $`3 \times 1`$. 
<br> Let $`\vec{v}=\alpha\vec{d}`$, $`\alpha`$ is the magnitude and $`\vec{d}`$ is the direction. 

<img width="800" alt="Definition of Angular Velocity" src="https://github.com/vitonzhangtt/RoboticsNotes/assets/28706904/df8bd09d-50c8-4e52-9552-fda189f0a9f4">

#### Direction of Velocity vector
$`{\Huge {\vec{d} = \frac{\vec{a} \times \vec{x}}{\left| \vec{x} \right|}}}`$

#### Magnitude
With a tiny change $`\Delta{t}`$ in time $`t`$, the new position of $`x`$ denoted by $`x_{1}`$. <br>
The $`\vec{x_{1}}`$ represent the position $`x_{1}`$ in the coordinate system, then <br>

##### Step 1: Find the vector for new position $`x_{1}`$
$`
\vec{x_{1}} = \vec{x} + \Delta{t}\vec{v} = \vec{x} + \alpha\Delta{t}\vec{d} `$

##### Step 2: Calculate the distance using trigonometric
$`
\alpha\Delta{t} = {\left| \vec{x} \right|} \tan{(\dot{\theta}\Delta{t})} = {\left| \vec{x} \right|} \frac{\sin{(\dot{\theta}\Delta{t})}}{\cos{(\dot{\theta}\Delta{t})}} = {\left| \vec{x} \right|} {\dot{\theta}\Delta{t}} (\frac{\sin{(\dot{\theta}\Delta{t})}}{{\dot{\theta}\Delta{t}}})(\frac{1}{\cos{(\dot{\theta}\Delta{t})}})
`$

##### Step 3: Apply the limit when $`\Delta{t}`$ approaches 0
According the [limits](#limits), the result be when $`\Delta{t}`$ approaches $`0`$. (because $`\Delta{t}`$ is **very very tiny**). <br>

$`
\alpha\Delta{t} \approx {\left| \vec{x} \right|} \dot{\theta} \Delta{t} \implies \alpha \approx {\left| \vec{x} \right|} \dot{\theta}
`$

<img width="800" alt="Magnitude of Angular Velocity" src="https://github.com/vitonzhangtt/RoboticsNotes/assets/28706904/e76bab4f-5cee-4959-8106-2d608ed6f6d5">

#### Expression of Angular Velocity

$`
\Huge \vec{v} = {\left| \vec{x} \right|} \dot{\theta} \frac{\vec{a} \times \vec{x}}{\left| \vec{x} \right|} = (\dot{\theta}\vec{a}) \times \vec{x}  \text{                \color{red} Cross Product }
`$

We call $`\dot{\theta}\vec{a}`$ as **Angular Velocity** and denoted by $`\vec{\omega}`$. So we have <br>

$`
\Huge \vec{v} = \vec{\omega} \times \vec{x}
`$

### Limits
#### Limit of $`\sin{(x)}/x`$ when x approaches 0 <sup>Ref[4], Ref[5]<sup>
According the Ref[4] and Ref[5], we got the following: <br>

$`
\lim\limits_{x \to 0} \frac{\sin{(x)}}{x} = 1
`$

#### Limit of $`1/\cos(x)`$ when x approaches 0
$`\lim\limits_{x \to 0} \frac{1}{\cos{(x)}} = 1`$

## Euler angles 


## Examples in Real Life <sup>Ref[6]</sup>





## Reference
1. [Rotational motion](http://www.thphys.nuim.ie/Notes/MP350/notes-16/5-Rotation.pdf)
2. [Rotation Matrix Time Derivative (AAAA+)](https://www.youtube.com/watch?v=1RF7j-Yc21c)
3. [wiki: Angular velocity](https://en.wikipedia.org/wiki/Angular_velocity)
4. [A Beautiful Proof: Why the Limit of sin(x)/x as x Approaches 0 is 1?](https://medium.com/however-mathematics/a-beautiful-proof-why-the-limit-of-sin-x-x-as-x-approaches-0-is-1-c9709e72fda)
5. [Limit of sin(x)/x as x approaches 0](https://www.khanacademy.org/math/ap-calculus-ab/ab-limits-new/ab-1-8/v/sinx-over-x-as-x-approaches-0)
6. [Angular velocity](https://byjus.com/physics/angular-velocity/)
7. [Rotational Motion Physics, Basic Introduction, Angular Velocity & Tangential Acceleration](https://www.youtube.com/watch?v=WQ9AH2S8B6Y)
8. [Centripetal and Centrifugal Force](https://byjus.com/physics/centripetal-and-centrifugal-force/)
