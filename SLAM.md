# SLAM: Simultaneous Localization and Mapping


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
Extended Kalman Filters (EKF)
Particle Filters

### Bundle Adjustment

Real-time Bundle Adjustment:
* Pose Graph Optimisation

### Filter Methods vs. Bundle Adjustment

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
only work for short distances (e.g. indoors).<sup>11</sup>

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
