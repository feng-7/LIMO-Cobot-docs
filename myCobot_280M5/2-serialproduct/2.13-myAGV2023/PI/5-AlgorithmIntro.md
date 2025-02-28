# Realize Mapping

 ![建图文件成功打开](../../../resourse/13-AdvancedKit/myAGV/小车建图/1.jpg)

At present, the use of robots needs to carry out SLAM mapping, because the mobile robot wants to achieve autonomous walking, the core lies in the realization of autonomous positioning and navigation, in the autonomous positioning and navigation technology will involve positioning, mapping, path planning and other issues, and the quality of map construction will directly affect the robot's walking path. If a robot wants to reach a certain destination, it needs to draw a map like a human, and the process of describing the environment and understanding the environment mainly relies on the map.

**Introduction to Gmapping Algorithm**

**Gmapping**: is a particle filter-based laser SLAM algorithm, which has been integrated with ROS and is the most used SLAM algorithm in mobile robots.

Particle filter-based algorithms represent the posterior probability of a path with several weighted particles, each given an important factor.

But they usually require a large number of particles to obtain good results, thereby increasing the computational complexity of the algorithm. In addition, the particle degradation exhaustion problem associated with the PF resampling process also reduces the accuracy of the algorithm.

**Introduction to Cartographer Algorithm**

**Cartographer**: It is a real-time indoor SLAM project developed by Google, a set of SLAM algorithms based on graph optimization.

Cartographer adopts the method of nonlinear optimization based on ceres developed by Google. The highlight of Cartographer lies in code specification and engineering, which is very suitable for commercial applications and redevelopment.

Moreover, the idea of Cartographer constructing a global map based on submap submaps can effectively avoid the interference of moving objects in the environment during the mapping process. And Cartographer supports multi-sensor data (odometry, IMU, LaserScan, etc.) for mapping, Support 2D_SLAM and 3D_SLAM mapping. It can output the covariance matrix naturally, the input item of back-end optimization.

**Comparison of Gmapping and Cartorgrapher**

Gmapping can build indoor maps in real time, and requires less computation and higher accuracy in building small scene maps. Compared with Cartographer when building a small scene map, Gmapping does not require too many particles and there is no loopback detection, so the calculation amount is less than Cartographer and the accuracy is not much worse.

Gmapping effectively uses wheel odometer information, which is why Gmapping has low requirements for lidar frequency: odometer can provide the robot's pose prior.

The original intention of Cartographer is not to solve the positioning and mapping of planar mobile robots, but Cartographer is used for hand-held lidar to complete the SLAM process, so there is no odometer to use.

