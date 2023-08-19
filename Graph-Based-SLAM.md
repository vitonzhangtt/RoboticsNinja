# Graph-Based SLAM


## Least Squares 
The least squares is called "最小二乘法" in chinese.

### Problem
Suppose that $`A\vec{x}=\vec{b}`$ does not have a solution. What is the best approximate solution? <br>
For our purposes, the best approximate solution is called the **least-squares solution**. <sup>14</sup>

### 

3:10 in Ref[2]




## Pose and Constraints
Pose refers to XY or XYZ location plus the heading information. <sup>[2]</sup> The pose is as the node of the graph. <br>
The constraints are between poses, they are as the edges of the graph.  

Constraints connect the poses of the robot while it is moving. 


## $`g^2O`$ framework







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

