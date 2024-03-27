# Bayes Filter

## [Markov Property](https://github.com/vitonzhangtt/ProbabilityTheoryNinja/blob/main/MCMC_Markov-Chain-Monte-Carlo.md#markov-property)

## Recursive Bayes Filter
42:07@[1]

<img width="447" alt="Screen Shot 2024-03-26 at 17 53 15" src="https://github.com/vitonzhangtt/RoboticsNinja/assets/28706904/6b01ef90-7ef4-4c96-ac7a-6a3201022d32">



## Steps 

44:13@[1]

<img width="429" alt="Screen Shot 2024-03-26 at 18 00 08" src="https://github.com/vitonzhangtt/RoboticsNinja/assets/28706904/60c0ad13-570c-43ba-b33e-cb8b8d1d312f">


### Predict step

In the **predict step**, we will make an estimate about the current value of our state, given only the **prior measurements**. <sup>[10]</sup>

### Update/Correction step
In what we call the **update step**, we use the current measurement to estimate the current state. <sup>[10]</sup>

## Models
45:15@[1]

<img width="518" alt="Screen Shot 2024-03-26 at 18 18 31" src="https://github.com/vitonzhangtt/RoboticsNinja/assets/28706904/02fdfcee-470f-45dc-a1dc-22fc4f3917b0">

### Sensor/Measurement/Observation Model


### Action/Motion/Transition Model

## Filters
49:05@[1]

<img width="540" alt="Screen Shot 2024-03-26 at 18 34 37" src="https://github.com/vitonzhangtt/RoboticsNinja/assets/28706904/e24cf78d-14bd-4291-b91d-ae656e1c3267">


## Related Topic
Kalman Filter, 

## TODO
1. google "dynamic bayesian network for control, state, sensations"






## Reference
1. [Lecture 02-Bayes Filters-Kalman Filtering](https://www.youtube.com/watch?v=2__ktwJrMf8&list=PLdMorpQLjeXmbFaVku4JdjmQByHHqTd1F&index=2)
2. wiki: [Recursive Bayesian estimation](https://en.wikipedia.org/wiki/Recursive_Bayesian_estimation)
3. [Bayes Filters](https://people.eecs.berkeley.edu/~pabbeel/cs287-fa13/slides/bayes-filters.pdf) [To Read]
4. [Bayes Filter (Cyrill Stachniss)](https://www.youtube.com/watch?v=0lKHFJpaZvE) | [A Short Introduction to the
Bayes Filter and Related Models](http://ais.informatik.uni-freiburg.de/teaching/ws13/mapping/pdf/slam03-bayes-filter-short.pdf)
5. [**Statistical Techniques in Robotics** (16-831, F10) Lecture #02 Bayes Filter @CMU](https://www.cs.cmu.edu/~16831-f14/notes/F14/16831_lecture02_prayana_tdecker_humphreh.pdf)
6. [Bayesian Filtering for Location Estimation](https://rse-lab.cs.washington.edu/postscripts/bayes-filter-pervasive-03.pdf)
7. [Introduction to recursive Bayesian filtering](https://people.csail.mit.edu/mrub/talks/filtering.pdf) [To Read]
8. [Kalman and Bayesian Filters in Python](https://github.com/rlabbe/Kalman-and-Bayesian-Filters-in-Python)
9. [The Bayes Filter: A Tool Every Roboticist Should Know](https://www.youtube.com/watch?v=nVU1DQ-_R5E)
10. [The Bayes Filter](https://medium.com/@vikramsetty169/the-bayes-filter-71f8b61afc1c) about Bayes Filter and SLAM. (AAAA+)
11. [A Discriminative Approach to Bayesian Filtering with Applications to Human Neural Decoding](https://burkh4rt.github.io/pubs/Burkhart-2019.pdf) [To Read]
12. [Lecture 3: Bayesian Filtering Equations and Kalman Filter](https://users.aalto.fi/~ssarkka/course_k2016/handout3.pdf)
13. [The Bayes Filter and Intro to State Estimation](https://johnwlambert.github.io/bayes-filter/) (AAAAA)
