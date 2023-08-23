# Graph-Based SLAM


## Least Squares 
The least squares is called "最小二乘法" in chinese.
3:10 in Ref[2]

### Problem
Suppose that $`A\vec{x}=\vec{b}`$ does not have a solution. What is the **best approximate solution**? <br>
For our purposes, the best approximate solution is called the **least-squares solution**. <sup>14</sup>

### Least-Squares Solutions


### Gauss–Newton algorithm






## Pose and Constraints
Pose refers to XY or XYZ location plus the heading information. <sup>[2]</sup> The pose is as the node of the graph. <br>
The constraints are between poses, they are as the edges of the graph.  

Constraints connect the poses of the robot while it is moving. 


## $`g^2O`$ framework


## RTAB-Map 
RTAB-Map (**Real-Time Appearance-Based Mapping**) is a RGB-D, Stereo and Lidar  <br>
Graph-Based SLAM approach based on an incremental appearance-based  <br>
loop closure detector. <sup>[23]</sup>





## Reference
1. [A brief introduction to GraphSLAM](https://shivachandrachary.medium.com/a-brief-introduction-to-graphslam-4204b4fce2f0) (AAAA)
2. [Graph-based SLAM using Pose Graphs (Cyrill Stachniss)](https://www.youtube.com/watch?v=uHbRKvD8TWg&t=6s) (AAAA+)
3. [GRAPH SLAM: A Beginner’s Guide to this Groundbreaking Mapping Technology](https://pub.towardsai.net/everything-you-need-to-know-about-graph-slam-7f6f567f1a31) (AAA)
4. [Applying Graph-based SLAM Algorithm in a Simulated Environment](https://iopscience.iop.org/article/10.1088/1757-899X/769/1/012035)
5. [ICP-based pose-graph SLAM](https://hal.science/hal-01522248/document)
6. [graphslam: Graph SLAM solver in Python](https://python-graphslam.readthedocs.io/en/stable/)
7. [Dynamic Pose Graph SLAM: Long-term Mapping in Low Dynamic Environments](https://www.cs.cmu.edu/~kaess/pub/WalcottBryant12iros.pdf)
8. [ProSLAM: Graph SLAM from a Programmer's Perspective](https://arxiv.org/abs/1709.04377)
9. [g2o: A General Framework for Graph Optimization](https://github.com/RainerKuemmerle/g2o)
10. [g2o: A General Framework for Graph Optimization](http://ais.informatik.uni-freiburg.de/publications/papers/kuemmerle11icra.pdf)
11. [g2o: A General Framework for Graph Optimization (Slide)](https://cse.sc.edu/~yiannisr/774/2015/g2o.pdf)
12. [Analysis for Graph-Based SLAM Algorithms under $`g^2o`$ Framework](https://www.cs.cmu.edu/~tianxian/files/Analysis_for_Graph_Based_SLAM_Algorithms_under_g2o_Framework.pdf)
13. [A Tutorial on Graph-Based SLAM](http://www2.informatik.uni-freiburg.de/~stachnis/pdf/grisetti10titsmag.pdf)
14. [6.5 The Method of Least Squares](https://textbooks.math.gatech.edu/ila/least-squares.html)
15. [Gauss–Newton algorithm](https://en.wikipedia.org/wiki/Gauss%E2%80%93Newton_algorithm)
16. [Stochastic Gauss-Newton Algorithms for Nonconvex Compositional Optimization](http://proceedings.mlr.press/v119/tran-dinh20a/tran-dinh20a-supp.pdf)
17. [Solving a nonlinear least squares problem with the Gauss-Newton method and lsqnonlin](https://www.math.umd.edu/~petersd/460/html/nonlinls.html)
18. [Least Square Method](https://www.cuemath.com/data/least-squares/)
19. [Least Squares Method: What It Means, How to Use It, With Examples](https://www.investopedia.com/terms/l/least-squares-method.asp)
20. [wiki: Least squares](https://en.wikipedia.org/wiki/Least_squares)
21. [Graph SLAM](https://courses.cs.washington.edu/courses/cse571/23sp/slides/L09/Lecture09_Modern%20SLAM.pdf) (To Read)
22. [A LiDAR/Visual SLAM Backend with Loop Closure Detection and Graph Optimization](https://www.mdpi.com/2072-4292/13/14/2720/htm)
23. [RTAB-Map: Real-Time Appearance-Based Mapping](http://introlab.github.io/rtabmap/)
24. [video list: Autonomous Navigation](https://www.youtube.com/playlist?list=PLn8PRpmsu08rLRGrnF-S6TyGrmcA2X7kg) | [Understanding SLAM Using Pose Graph Optimization | Autonomous Navigation, Part 3](https://www.youtube.com/watch?v=saVZtgPyyJQ&list=PLn8PRpmsu08rLRGrnF-S6TyGrmcA2X7kg&index=3)
