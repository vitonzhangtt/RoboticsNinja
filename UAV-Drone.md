# UAV: Unmanned Aerial Vehicles (or Drone)

## Items

| English | Chinese |
| -- | -- |
| multirotor | 多旋翼 |
| quadcopter | 四轴飞行器 |

## What's UAV
Unmanned aerial vehicles (UAV) are a class of aircrafts that can fly without the onboard presence of pilots. <br>
Unmanned Air Vehicle (UAV)

## Multirotor UAV(多旋翼无人机)

### QuadRotor (四旋翼)

## Simulator

### RotorPy

### Gazebo
[24]

## Flight Controller
TODO: [37]

This is the role of the `flight controller` — a vital component of a `quadcopter drone` that <br>
acts as its “brain”. The flight controller is responsible for **controlling** and **stabilizing** <br> 
the flight of the quadcopter while it is airborne. More specifically, it is **responsible for** <br>
ensuring that the quadcopter manages stable flight at all times and complies with the attitude(姿态) <br>
“requests” of it’s pilot. <sup>[37]</sup>


### List
1. [Complete List of Flight Controller Firmware Projects](https://blog.unmanned.tech/flight-controller-firmware/)
2. [A Review of Open-Source Flight Control Systems](https://reefwing.medium.com/a-review-of-open-source-flight-control-systems-2fe37239c9b6)


## Dronecode
[3]

## PX4
[1]
`PX4` is an open source **flight control software** for drones and other unmanned vehicles.

### SITL
PX4 supports both *Software In the Loop* (`SITL`) simulation, where the flight stack <br>
runs on computer (either the same computer or another computer on the same network) <br>
and *Hardware In the Loop* (`HITL`) simulation using a simulation firmware on a real <br>
**flight controller board**. <sup>[22]</sup>

### PX4 vs. Ardupilot
* [PX4 vs ArduPilot: What is Difference](https://www.hows.tech/2024/02/px4-vs-ardupilot-what-is-difference.html)
* [PX4 vs ArduPilot: Choosing the right open source flight stack](https://www.thedroningcompany.com/blog/px4-vs-ardupilot-choosing-the-right-open-source-flight-stack)
* [ArduPilot vs PX4](https://dojofordrones.com/ardupilot-vs-px4/)


## Aerodynamics (空气动力学)

## Companies

### DroneDeploy
[7]

## MAVLink
*MAVLink* is a very lightweight **messaging protocol** for communicating with drones (and between <br>
onboard drone components). <sup>[30]</sup>

### Pymavlink
[31], 

## Links for Drone

Table: Links
| Name | Link | Description |
| -- | -- | -- |
| Ardupilot | [Ardupilot](Ardupilot.org) | |
| ecalc | [ecalc](ecalc.ch) | |

## Books

* Build a Drone: A Step-by-Step Guide to Designing, Constructing, and Flying Your Very Own Drone (2016)
* Mastering Drone Design and Programming: A Comprehensive Guide to Learn Drone Design and Programming (2023)
* Fundamentals of Capturing and Processing Drone Imagery and Data (2023)
* Make your Arduino Quadcopter Drone from Scratch: Choice of components, Construction of the frame, Electrical and electronic wiring, Programming in Arduino language of the flight controller (2021)
* Drone Technology in Architecture, Engineering, and Construction: A Strategic Guide to Unmanned Aerial Vehicle Operation and Implementation (2021)
* OpenDroneMap: The Missing Guide: A Practical Guide To Drone Mapping Using Free and Open Source Software, Second Edition (2023)
* Make: Drones: Teach an Arduino to Fly (2016)
* How to build and maintain a drone from scratch: The simplified method of constructing, handling, and maintaining a drone from scratch even as a as a novice or professionals (2023)
* Advanced Robotic Vehicles Programming: An Ardupilot and Pixhawk Approach (2020)
* Artificial Intelligence Applications for Drone Cyber Security: Second Edition (2022)

## Reference
1. [PX4: Open Source Autopilot For Drone Developers](https://px4.io/) | [Getting Started with PX4 Autopilot
](https://docs.px4.io/main/en/getting_started/)
2. [Make a drone from beginning](https://medium.com/@abdullahorzan/make-a-drone-from-beginning-part-1-60cfe5d36c5a)
3. Dronecode: [We are setting the standards in the drone industry with open-source.](https://dronecode.org/)
4. [Top Drone Flight Simulators](https://uavcoach.com/drone-flight-simulator/#guide-6)
5. RotorPy: [A multirotor simulator with aerodynamics for education and research.](https://github.com/spencerfolk/rotorpy)
6. AirSim : [Open source simulator for autonomous vehicles built on Unreal Engine / Unity, from Microsoft AI & Research](https://github.com/microsoft/AirSim) |
7. [dronedeploy: Transforming the way businesses collect, manage and interpret reality capture data from drones, 360 cameras and mobile ground robots.](https://dronedeploy.com/) | [Forum](https://forum.dronedeploy.com/)
8. [Controlling a Drone After Sudden Rotor Failure #ICRA2022 with Sihao Sun](https://robohub.org/controlling-a-drone-after-sudden-rotor-failure-icra2022/)
9. [drone simulation environment setup (PX4, ROS2, gazebo)](https://medium.com/@kazuyahirotsu/drone-simulation-environment-setup-px4-ros-89314a3fba42) [To Read]
10. [How to start developing drone with PX4 and raspberry pi](https://medium.com/@kazuyahirotsu/how-to-start-developing-drone-with-px4-and-raspberry-pi-7b3db3575e1c) [To Read]
11. [Implementing a Search and Rescue Algorithm for Autonomous Drones](https://medium.com/@oscar.personal/implementing-a-search-and-rescue-algorithm-for-autonomous-drones-68559638378b)
12. [How Drones are Changing the Business Landscape](https://pcsite.medium.com/how-drones-are-changing-the-business-landscape-224e93f3e742)
13. [Resolving ESC Desynchronization in FPV Drones: Tips & Techniques](https://medium.com/@basharnipa45678/resolving-esc-desynchronization-in-fpv-drones-tips-techniques-a5b9eed3f33f)
14. [Aerospace(航天) Series](https://www.amazon.com/-/zh/dp/B09NMGXZBJ?binding=hardcover&searchxofy=true&ref_=dbs_s_bs_series_rwt_thcv&qid=1715829072&sr=1-4)
15. [现代飞机的飞行控制系统（一）](https://zhuanlan.zhihu.com/p/60196490)
16. Book: **Flight Simulation Software - Design Development and Testing** (2023)
17. [Hackflight is a C++ software toolkit for building multirotor flight controllers.](https://github.com/simondlevy/Hackflight)
18. [ArduPilot is the most advanced, full-featured, and reliable open source autopilot software available. ](https://github.com/ArduPilot/ardupilot)
19. [**dRehmFlight** is the flight controller for hobbyists, hackers, and non-coders interested in stabilizing their wacky and unique flying creations.](https://github.com/nickrehm/dRehmFlight)
20. [PX4 SITL of QuadRotor with Gazebo and QGround Control](https://www.youtube.com/watch?v=yR1fhNV970E)
21. [Gazebo Simulation](https://docs.px4.io/main/en/sim_gazebo_gz/)
22. [Simulation](https://docs.px4.io/main/en/simulation/)
23. [Ignition Gazebo for PX4 Software-In-The-Loop Simulations - Jaeyoung Lim, ETH Zurich](https://www.youtube.com/watch?v=KIcFbCiK0QU)
24. [Gazebo Simulator Tutorials](https://www.youtube.com/playlist?list=PLNw2RD-1J5YYvFGiMafRD_axHrBUGvuIg) [To Read]
25. [Connecting PX4 SITL Gazebo to Local Area Connection](https://www.youtube.com/watch?v=SU_hf1Sdamw)
26. Youtube Channel: [PX4 Autopilot - Open Source Flight Control.](https://www.youtube.com/@PX4Autopilot/playlists)
27. Video List: [2023 PX4 Developer Summit](https://www.youtube.com/playlist?list=PLYy2pGCdhu7xHIN7F5X1ytQ84hdYnIonr)
28. Youtube Channel: [Ascend Engineering: A team of engineers empowering the future of drones, unmanned aerial vehicles, and fixed-wing software engineering solutions no matter size, scope, or complexity.](https://www.youtube.com/@ascendengineering640)
29. [How To Start a Mission Using Pymavlink](https://www.youtube.com/watch?v=pAAN055XCxA)
30. [MAVLink Developer Guide](https://mavlink.io/en/)
31. [Using Pymavlink Libraries (mavgen)](https://mavlink.io/en/mavgen_python/)
32. [Pymavlink Tutorials](https://www.youtube.com/playlist?list=PLy9nLDKxDN68cwdt5EznyAul6R8mUSNou)
33. [Survey of Simulators for Aerial Robots](https://arxiv.org/pdf/2311.02296)
34. [Autonomous Ardupilot Tiny Whoop](https://www.youtube.com/watch?v=NHWOztdg5mM) [To Read]
35. [Simulated Workflows using Software-In-The-Loop Simulations — PX4 Developer Summit Virtual 2020](https://www.youtube.com/watch?v=60SX8pwYLUc)
36. [PX4 X-Plane SITL Ultimate Setup Guide: Fly Custom eVTOL & Drones in Real Worlds - Version 1.0.0](https://www.youtube.com/watch?v=aRJxsnf24k4) | [PX4 X-Plane Plugin](https://github.com/alireza787b/px4xplane)
37. [My Greatest Engineering Accomplishment: The Scout Flight Controller](https://timhanewich.medium.com/my-greatest-engineering-accomplishment-the-scout-flight-controller-d8937fb45b24) [To Read] (AAAA+)
38. [Types of Drones and UAVs (2025)](https://www.tytorobotics.com/blogs/articles/types-of-drones) [To Read]
