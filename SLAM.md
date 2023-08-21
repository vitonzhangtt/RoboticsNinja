# SLAM: Simultaneous Localization and Mapping


## What's SLAM

### Problem
`If we leave a robot in an unknown location in an unknown environment, can the robot make
a satisfactory map while simultaneously being able to find its pose in that map?` <sup>12</sup>

### Definition
`SLAM is the process by which a robot builds a map of the environment and, at the same 
time, uses this map to compute its location` <sup>[12]</sup>

**Localization**: inferring location given a map <br>
**Mapping**: inferring a map given a location <br>
**SLAM**: learning a map and locating the robot simultaneously <br>

### Chicken-or-egg Problem
SLAM is a chicken-or-egg problem: <sup>[12]</sup> <br>
→ A map is needed for localizing a robot <br>
→ A pose estimate is needed to build a map 

## The Architecture of SLAM
`Two parts of Visual SLAM`<sup>[25]</sup> <br>

Generally a SLAM system consists of a frontend and a backend. <sup>[32]</sup>

Frontend takes in raw sensor data from sensors such as LiDAR, camera, IMU, etc. <br>
and transforms it into an **intermediate representation** such as constraints of an <br>
optimization problem.

Backend takes this intermediate representation from the frontend and does <br>
the task of solving the optimization problem or state estimation problem i.e. <br>
estimating parameters which describe the position of objects/landmarks in the <br>
environment or where the robot is in it. 

### Frontend


### Backend

## Diversification of SLAM

### Feature-based Method 

Table-1: Features list


| Feature Name | Description |
| --- | --- |
| SIFT: Scale-invariant Feature Transform | |
| SURF: Speeded Up Robust Features |  |
| ORB: Oriented FAST and Rotated BRIEF | |

These features are designed to be robust to translation, rotation, <br>
variations in scale, view-point, lighting, etc.



### Direct Method

#### LSD-SLAM

#### Direct Sparse Odometry


## Camera poses

### RANSAC

### Iterative Closest Point (ICP)

## Correcting the map

### Filter Methods

#### Extended Kalman Filters (EKF)

#### Particle Filters
Rao-Blackwellized particle filter (FastSLAM)

### Bundle Adjustment



Real-time Bundle Adjustment:
* Pose Graph Optimisation

### Filter Methods vs. Bundle Adjustment

### Graph-Based SLAM


## Place Recognition

### image-to-image
For image-to-image comparison, Bag of Words (BoW) is an effective way to quickly narrow down candidates for corresponding frames.

### image-to-map

### map-to-map

## Visual SLAM

### Camera

#### Stereo cameras

#### Depth cameras
There is one disadvantage though — unlike stereo cameras, depth cameras <br>
only work for short distances (e.g. indoors). <sup>[11]</sup>

### Implementation (make hands dirty) <sup>[36]</sup>

## Triangulation



## Visual Odometry, Visual SLAM and Structure-from-Motion <sup>[9], [10], [11]</sup>

### Visual Odometry <sup>[19]</sup>

## Reference
1. [The future of spatial intelligence is here](https://www.slamcore.com/)
2. [Spatial AI: Augmenting SLAM technology with deep learning](https://blog.slamcore.com/spatial-ai-slam-deep-learning)
3. [A Review of Common Techniques for Visual Simultaneous Localization and Mapping](https://www.hindawi.com/journals/jr/2023/8872822/)
4. Book: [Large-Scale Simultaneous Localization and Mapping](https://link.springer.com/book/10.1007/978-981-19-1972-5) (2022)
5. [46. Simultaneous Localization and Mapping](https://www.cs.columbia.edu/~allen/F19/NOTES/slam_paper.pdf) (AAAA+)
6. [Simultaneous Localisation and Mapping (SLAM):Part I The Essential Algorithms](https://people.eecs.berkeley.edu/~pabbeel/cs287-fa09/readings/Durrant-Whyte_Bailey_SLAM-tutorial-I.pdf)
7. [Simultaneous Localization and Mapping (SLAM):Part II](https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=1678144)
8. Book: [Introduction to Visual SLAM: From Theory to Practice](https://www.amazon.com/Introduction-Visual-SLAM-Theory-Practice/dp/9811649383)
9. [Visual Odometry vs. Visual SLAM vs. Structure-from-Motion](https://guvencetinkaya.medium.com/visual-odometry-vs-visual-slam-cdda75df592)
10. [Tutorial on Visual Odometry](http://mrsl.grasp.upenn.edu/loiannog/tutorial_ICRA2016/VO_Tutorial.pdf) 
11. [How Robots Make Maps— an Intro to SLAM (Simultaneous Localisation and Mapping)](https://medium.com/swlh/how-robots-make-maps-an-intro-to-slam-simultaneous-localisation-and-mapping-37370c3e7dfe) (AAAA+) [Read Again]
12. [SLAM Tutorial](https://www.cs.columbia.edu/~allen/F19/NOTES/slam_pka.pdf) (To Read) [Notes](https://www.cs.columbia.edu/~allen/F19/notes.html)
13. [Types of SLAM and Its Application Examples](https://www.maxstblog.com/post/types-of-slam-and-application-ex)
14. [The Types of SLAM Algorithms](https://medium.com/@nahmed3536/the-types-of-slam-algorithms-356196937e3d)
15. [Lidar SLAM: The Ultimate Guide to Simultaneous Localization and Mapping](https://www.wevolver.com/article/lidar-slam-the-ultimate-guide-to-simultaneous-localization-and-mapping) (To Read)
16. [LiDAR SLAM : spotlight on Kitware’s open source library](https://www.kitware.com/lidar-slam-spotlight-on-kitwares-open-source-library/)
17. [A Comparative Analysis of LiDAR SLAM-based Indoor Navigation for Autonomous Vehicles](http://mvr.whu.edu.cn/pubs/IEEE_SLAM-v11.pdf)
18. [Robotic LiDARs for fast 3D construction](https://innowings.engg.hku.hk/slam-lidar/)
19. [Direct Visual Odometry in Low Light using Binary Descriptors](https://www.ri.cmu.edu/app/uploads/2017/04/Alismail17ral.pdf)
20. [wiki: List of SLAM methods](https://en.wikipedia.org/wiki/List_of_SLAM_methods)
21. [OpenSLAM](https://openslam-org.github.io/)
22. [Past, Present, and Future of Simultaneous Localization and Mapping: Toward the Robust-Perception Age](https://rpg.ifi.uzh.ch/docs/TRO16_cadena.pdf) (To Read)
23. [Perceptual Aliasing++: Adversarial Attack for Visual SLAM Front-End and Back-End](https://romi.seecs.nust.edu.pk/wp-content/uploads/2023/02/Perceptual_Aliasing_Adversarial_Attack_for_Visual_SLAM_Front-End_and_Back-End.pdf)
24. [Real-time 6-DOF Multi-session Visual SLAM over Large Scale Environments](https://www.cs.cmu.edu/~kaess/pub/McDonald13ras.pdf)
25. [Learning Deep Visual SLAM Frontends: SuperPoint++](https://tom.ai/presentations/visual_slam_workshop_malisiewicz_iccv2019.pdf)
26. [Visual SLAM: What Are the Current Trends and What to Expect?](https://www.mdpi.com/1424-8220/22/23/9297) (To Read)
27. [Learning Deep Convolutional Frontends for Visual SLAM](https://www.youtube.com/watch?v=kjaRRGLw4RA)
28. [Visual-SLAM Classical Framework and Key Techniques: A Review](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC9227238/) (2022) (To Read)
29. [ULL-SLAM: underwater low-light enhancement for the front-end of visual SLAM](https://www.frontiersin.org/articles/10.3389/fmars.2023.1133881/full)
30. [SLAM Course - 20 - SLAM Frontends (2013/14; Cyrill Stachniss)](https://www.youtube.com/watch?v=Ejw1HBj3Apg)
31. [3 Lectures on SLAM: E02 - SLAM Frontend & Backend - From feature matching to pose graph optimization](https://www.youtube.com/watch?v=eoXRziLhU-I) (To Read)
32. [Introduction to SLAM](https://medium.com/@rutwikshinde2000/basic-introduction-to-slam-26688f7994a8)
33. [Introduction to SLAM (Cyrill Stachniss)](https://www.youtube.com/watch?v=0I30M6yTklo) (To Read)
34. [Lecture 23: Simultaneous Localization and Mapping I](https://vnav.mit.edu/material/23-SLAM1-formulationsAndSparsity-notes.pdf) (MIT 16.485: Visual Navigation for Autonomous Vehicles (VNAV)) (To Read)
35. [SLAM Front-Ends](http://ais.informatik.uni-freiburg.de/teaching/ws11/robotics2/pdfs/rob2-13-frontends.pdf)
36. [How to implement visual SLAM?](https://dvic.devinci.fr/how-implement-visual-slam)
