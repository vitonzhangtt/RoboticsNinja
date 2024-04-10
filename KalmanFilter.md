# Kalman Filter



## Guass-Kalman Process
**Gauss–Markov stochastic processes** (named after Carl Friedrich Gauss and Andrey Markov) are stochastic <br>
processes that satisfy the requirements for both **Gaussian processes** and **Markov processes**. <sup>[15]</sup>

## Linear Kalman Filter (LKF)

They(Kalman Filter) are separated into **predict** (using the model) and **correct** (using the <br>
measurements), hence the two-step process for estimating state. The **predict step** is <br>
responsible for propagating the state vector into the future using the linear model, <br>
and the **correct(or, update) step** blends the current prediction with a current measurement to get the <br> 
corrected estimated state. <sup>[18]</sup>

The LKF assumes that the **system dynamics** are linear. <sup>[21]</sup>

### Recap <sup>[18]</sup>
* A Kalman filter combines a **noisy measurement** with a **flawed prediction** to create an optimal state estimate. 

* We can use covariance as a measure of how much uncertainty there is in the noisy measurement, the flawed model, and the final estimation. 

* Since covariance is multi-dimensional, it’s mathematically easier to maintain it in matrix form.

* A Kalman filter uses three different covariance matrices (measurement,  model, final estimation) in order to maintain an estimate of the system state. 

### Gaussian Distribution

But luckily - and importantly! - a Gaussian probability distribution maintains 
its **Gaussian shape** when subjected to linear operations. <sup>[18]</sup>

Therefore, if the initial distribution is Gaussian and the process model is linear 
(or has been linearized prior to running it) then the final prediction uncertainty 
is still Gaussian in nature. It can be wider or narrower, but it’s just a Gaussian shape. <sup>[18]</sup>

### Formula

#### Symbole

| Symbole | Description |
| -- | -- |
| P | prediction error covariance | 
| Q | process noise covariance |
| R | measurement noise covariance |



### System Model
As we’ve seen, a Kalman filter requires a mathematical model in order to predict the future state. <sup>[18]</sup>

## Kalman Filter Equations

### 1. State Extrapolation Equation (Transition Equation / Prediction Equation / Dynamic Model / State Space Model)

This system of equations **extrapolates** the current state to the next state (prediction).
The **State Extrapolation Equations** depend on the **system dynamics** and differ from example to example.

Using the **state extrapolation equation**, we can **predict** the next system state based on <br>
the knowledge of the current state. It extrapolates the state vector from the present (time step $`n`$) <br>
to the future (time step $`n + 1`$). <sup>[21]</sup>

The state extrapolation equation describes **the model of the dynamic system**.  <sup>[21]</sup>

#### Definition
$`\hat{x}_{n+1,n} = F\hat{x}_{n,n} + Gu_{n} + w_{n} `$  Where:

<img width="800" alt="Screen Shot 2024-04-10 at 13 35 44" src="https://github.com/vitonzhangtt/RoboticsNinja/assets/28706904/923d0e3d-b216-450e-9715-b25e7fa680a5">


### 2. State Update Equation


### 3. Covariance Extrapolation Equation

The **State Extrapolation Equation** and the **Covariance Extrapolation Equation** depend on the system dynamics.

### 4. Kalman Gain Equation

#### Kalman Gain
This multiplier, k, is the optimal Kalman gain. The value is a scale between 0 and 1 and <br>
it reflects the relative uncertainty in the prediction versus the measurement. <sup>[18]</sup>

As you can see, the **Kalman Gain** ($`K_{n}`$) is the **measurement weight**, and the $`(1 − K_{n})`$ <br>
term is the weight of the current state estimate. <sup>[21]</sup>

### 5. Covariance Update Equation

## Process Noise

In the real world, there are uncertainties in the system dynamic model. <sup>[21]</sup>

The uncertainty of the dynamic model is called the **Process Noise**. In the literature, <br>
it is also called **plant noise, driving noise, dynamics noise, model noise, and system noise**. <br>
The process noise produces estimation errors. <sup>[21]</sup>

The **Process Noise Variance** is denoted by the letter $`q`$.

## Lag Error

## Covariance Matrix 

The Kalman Filter output is a **multivariate random variable**. A **covariance matrix** <br>
describes the squared uncertainty of the multivariate random variable. <sup>[21]</sup>

The uncertainty variables of the multivariate Kalman Filter: <sup>[21]</sup> 

| Notation | Notes |
| -- | -- |
| $`P_{n,n}`$ | is a covariance matrix that describes the squared uncertainty of an estimate |
| $`P_{n+1,n}`$| is a covariance matrix that describes the squared uncertainty of a prediction |
| $`R_{n}`$ | is a covariance matrix that describes the squared measurement uncertainty|
| $`Q`$ | is a covariance matrix that describes the process noise |



## Extended Kalman Filter

## Books
1. [Kalman Filter Make Easy](https://thekalmanfilter.com/kalman-filter-made-easy-ebook/)
2. Kalman and Bayesian Filters in Python | [Github](https://github.com/rlabbe/Kalman-and-Bayesian-Filters-in-Python)
3. Bayesian Inference of State Space Models: Kalman Filtering and Beyond (2021)
4. Introduction to Random Signals, Estimation Theory, and Kalman Filtering (2024)
5. SMOOTHING, FILTERING AND PREDICTION: Second Edition (2019)
6. Flight Dynamics: Second Edition (2022)
7. Nonlinear Kalman Filter for Multi-Sensor Navigation of Unmanned Aerial Vehicles: Application to Guidance and Navigation of Unmanned Aerial Vehicles Flying in a Complex Environment (2018)
8. KALMAN FILTER DESIGN FOR BALLISTIC MISSILE DEFENSE APPLICATION: KALMAN FILTER DESIGN (2023)
9. Control System Design: An Introduction to State-Space Methods (2005)
10. Kalman Filtering: with Real-Time Applications (2017)
11. Digital and Kalman Filtering: An Introduction to Discrete-Time Filtering and Optimum Linear Estimation, Second Edition (2018)

## Reference
1. [Orientation Estimation using Kalman Filter, Quaternions, and an IMU as sensor | long video
](https://www.youtube.com/watch?v=6oH4Stb2Ifs)
2. [Kalman Filter - Part 1](https://www.youtube.com/watch?v=LioOvUZ1MiM)
3. [Kalman Filter for Beginners, Part 1 - Recursive Filters & MATLAB Examples
](https://www.youtube.com/watch?v=HCd-leV8OkU)
4. ["Kalman Filtering with Applications in Finance" by Shengjie Xiu, course tutorial 2021
](https://www.youtube.com/watch?v=R63dU5w_djQ)
5. [Sensor Fusion Algorithms For Autonomous Driving: Part 1 — The Kalman filter and Extended Kalman Filter](https://medium.com/@wilburdes/sensor-fusion-algorithms-for-autonomous-driving-part-1-the-kalman-filter-and-extended-kalman-a4eab8a833dd)
6. [Kalman Filter For Self Driving Cars, Part 2](https://medium.com/@nikhilbadam56/kalman-filter-for-self-driving-cars-part-2-c069d815553e)
7. [Kalman Filtering for Attitude Estimation with Quaternions and Concepts from Manifold Theory](https://www.ncbi.nlm.nih.gov/pmc/articles/PMC6339217/pdf/sensors-19-00149.pdf)
8. [Kalman Filters: A step by step implementation guide in python](https://medium.com/analytics-vidhya/kalman-filters-a-step-by-step-implementation-guide-in-python-91e7e123b968) (To Read)
9. [Kalman Filter Part 1 — Introduction](https://medium.com/@mathiasmantelli/kalman-filter-series-introduction-6d2e2b28d4cf) [To Read] (AAAA+)
10. [Kalman Filter Part 2 — Bayes Filter](https://medium.com/@mathiasmantelli/kalman-filter-part-2-bayes-filter-f2fa9c0b5c95) [To Read]
11. [Kalman Filter Part 3 — A Formal Discussion](https://medium.com/@mathiasmantelli/kalman-filter-part-3-a-formal-discussion-e1a61b359fef)
12. [4.2 Bayesian derivation of the Kalman filter](https://www.youtube.com/watch?v=u_xRUxwlaFY) | Video List: [Sensor fusion and nonlinear filtering](https://www.youtube.com/playlist?list=PLTD_k0sZVYFqjFDkJV8GE2EwfxNK59fJY) [To Read]
13. [The math behind Extended Kalman Filtering](https://medium.com/@sasha_przybylski/the-math-behind-extended-kalman-filtering-0df981a87453) [To Read]
14. [LiDAR and Radar Sensor Fusion using Unscented Kalman Filter](https://medium.com/@nikhilnair8490/lidar-and-radar-sensor-fusion-using-unscented-kalman-filter-5b20de0ab1d1)
15. wiki: [Gauss–Markov process](https://en.wikipedia.org/wiki/Gauss%E2%80%93Markov_process)
16. [为什么使用卡尔曼滤波器？](https://www.youtube.com/watch?v=mwn8xhgNpFY) | [Understanding Kalman Filters](https://www.youtube.com/playlist?list=PLn8PRpmsu08pzi6EMiYnR-076Mh-q3tWr)
17. [Covariance Matrix Explained With Pictures](https://thekalmanfilter.com/covariance-matrix-explained/)
18. [#2: The Kalman Filter](https://engineeringmedia.com/controlblog/the-kalman-filter) (AAAAA)
19. [Gaussian, Markov and stationary processes](https://www.seas.upenn.edu/~ese3030/block_4_stationary_processes/slides/400_markov_gaussian_stationary_processes.pdf)
20. [Understanding Kalman Filter for Computer Vision](https://www.analyticsvidhya.com/blog/2021/10/an-intuition-about-kalman-filter/)
21. Book: Kalman Filter - from the Ground Up (2023)
