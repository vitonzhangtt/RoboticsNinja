# Motion Planning

## Workspace

## Configuration Space (C-Space)

### Configuration
The key problem is to make sure no point on the robot hits an obstacle, so we need <br>
a way to represent the location of all the points on the robot. **This representation** <br>
is the **configuration** of the robot, and the **configuration space** is the space of all <br>
configurations the robot can achieve. <sup>[12]</sup>

The **configuration** of a robot system is a **complete specification** of the position of <br>
every point of that system. The **configuration space**, or **C-space**, of the robot <br>
system is the space of all possible configurations of the system. <br>
Thus a configuration is simply a point in this abstract configuration space. <sup>[12]</sup>

The number of **degrees of freedom** of a robot system is the dimension of the configuration <br>
space, or the minimum number of parameters needed to specify the configuration. <sup>[12]</sup>

## Forward Kinematics


## Inverse Kinematics
As opposed to **forward kinematics**, which computes the workspace coordinates of the robot <br>
given a **configuration** as input, **inverse kinematics (IK)** is essentially the <br>
reverse operation: computing configuration(s) to reach a desired workspace coordinate. <sup>[11]</sup>


## Books

### Principles of Robot Motion - Theory Algorithms and Implementations (2005)


## Reference
1. [Robot Motion Planning @ CMU](https://www.cs.cmu.edu/afs/cs/academic/class/15381-s07/www/slides/020807motion.pdf)
2. [Motion Planning in Robotics](https://cs.stanford.edu/people/eroberts/courses/soco/projects/1998-99/robotics/basicmotion.html)
3. [Robotic Path Planning](https://fab.cba.mit.edu/classes/865.21/topics/path_planning/robotic.html)
4. [Introduction to Motion Planning Algorithms | Motion Planning with the RRT Algorithm, Part 1](https://www.youtube.com/watch?v=-fePRPyeKnc)
5. [Path Planning - A* (A-Star)](https://www.youtube.com/watch?v=icZj67PTFhc)
6. [Path Planning #2 Wave Propagation, Potential Fields & Modern(ish) C++](https://www.youtube.com/watch?v=0ihciMKlcP8)
7. [A review of motion planning algorithms for intelligent robots](https://link.springer.com/article/10.1007/s10845-021-01867-z) (To Read)
8. [Robot Motion Planning](http://ais.informatik.uni-freiburg.de/teaching/ss11/robotics/slides/18-robot-motion-planning.pdf) (To Read)
9. [Robot Motion Planning](https://resources.mpi-inf.mpg.de/departments/d1/teaching/ss10/Seminar_CGGC/Slides/06_Bazhenova_RMP.pdf)
10. [video: RSS 2023: Convex Geometric Motion Planning on Lie Groups via Moment Relaxation](https://www.youtube.com/watch?v=othZX-T-r5A)
11. Book: [Robotic Systems by Kris Hauser](https://motion.cs.illinois.edu/RoboticSystems/) (AAAA+)
12. Book: Principles of Robot Motion - Theory Algorithms and Implementations (2005)

