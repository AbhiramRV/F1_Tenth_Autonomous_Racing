# F1_Tenth_Autonomous_Racing

https://www.youtube.com/watch?v=LETPf6eoyYg


https://www.youtube.com/watch?v=v6w_zVHL8WQ&list=PL7rtKJAz_mPdFDJtufKmqfWRNu55s_LMc


ROS2

Perception:
  Detection and Segmentation
    3D Deep Learning
  Localization
      Localization of an f1 Tenth car is ususally done by inertial and odometry for inital guess and scan matching algorithm to fine tune it as map in know to us beforehand.
    EKF, UKF
    Scan Matching(NDT algorithm)
    Scan Matching (ICP)
    https://www.youtube.com/watch?v=LETPf6eoyYg&list=PL868twsx7OjdnroeAUFVBGlKGnFGi9txc&index=14
      In the ICP algorithm, if correspondences are known, resulting Rotation and Translation are computed uisng SVD method.
  
There are several techniques used for robot localization, depending on the available sensors, environment characteristics, and computational resources. Here are some commonly used techniques:

Odometry: Odometry is a technique that estimates the robot's pose by integrating measurements from proprioceptive sensors, such as wheel encoders or inertial measurement units (IMUs). By measuring the relative motion of the robot's wheels or its inertial forces, odometry provides an estimation of the robot's displacement and orientation. However, odometry suffers from cumulative errors over time, and its accuracy degrades in the presence of wheel slippage or sensor noise.

Kalman Filters and Extended Kalman Filters (EKF): Kalman filters and their extended versions are recursive estimation techniques that fuse sensor measurements with motion models to estimate the robot's pose. They maintain a probabilistic belief distribution of the robot's state and iteratively update the belief based on new sensor measurements. Kalman filters are suitable for linear systems, while extended Kalman filters handle non-linear systems by linearizing the motion and measurement models. They are widely used for localization with sensors like GPS, inertial sensors, or range finders.

Particle Filters (Monte Carlo Localization): Particle filters, also known as Monte Carlo Localization (MCL), are probabilistic methods that estimate the robot's pose by representing it with a set of particles. These particles are sampled from the belief distribution and updated based on sensor measurements. Particle filters are flexible and can handle non-linear motion and measurement models, making them suitable for localization in complex environments. They are commonly used with sensors like laser scanners or cameras.

Grid-based Methods: Grid-based localization methods represent the environment as a grid map and estimate the robot's pose by matching the sensor measurements with the map. Occupancy Grid Mapping is a technique that models the environment as a grid of cells, where each cell represents the probability of occupancy. Localization is performed by comparing the observed sensor data with the expected measurements from the map. Grid-based methods are commonly used with range sensors like laser scanners or sonar sensors.

Feature-based Methods: Feature-based localization relies on extracting and matching distinctive features in the environment to estimate the robot's pose. These features can be lines, corners, or landmarks. Techniques like Scan Matching, which aligns consecutive sensor scans, or Iterative Closest Point (ICP), which aligns 3D point clouds, fall under feature-based methods. Feature-based methods can be used with various sensors, including laser scanners, cameras, or depth cameras.

Simultaneous Localization and Mapping (SLAM): SLAM is a technique that addresses the problem of simultaneous mapping of the environment and localization of the robot within that map. It involves estimating the robot's pose while simultaneously building a map of the environment using sensor measurements. SLAM can utilize a combination of sensor types, such as laser scanners, cameras, or range finders, and various algorithms, including graph-based SLAM or filter-based SLAM.

These are just a few examples of the techniques used for robot localization. Each technique has its strengths and limitations, and the choice of technique depends on the specific requirements of the robot and the available sensor suite.

Particle filters and scan matching algorithms are both commonly used techniques for robot localization, but they differ in their approaches and underlying principles. Here's a brief explanation of each:

Particle Filters (Monte Carlo Localization):
Particle filters, also known as Monte Carlo Localization (MCL), are probabilistic methods used for estimating the robot's pose (position and orientation) based on sensor measurements. They rely on a set of particles, where each particle represents a potential pose hypothesis of the robot. These particles are randomly sampled from the robot's belief distribution and updated as new sensor measurements are received.
The basic idea of particle filters is to propagate particles through a prediction step using motion models and weight them based on the likelihood of the sensor measurements given the particle's pose. The weights are computed by comparing the expected sensor measurements with the actual measurements obtained from the sensors. After updating the weights, particles are resampled based on their weights to give more weight to particles that better match the measurements. This process helps to concentrate the particles around the true pose of the robot, improving the accuracy of localization.

Particle filters are flexible and can handle both global and local localization problems. They can handle non-linear motion and measurement models, as well as handle uncertainties effectively. However, the main drawback is their computational complexity, as the number of particles required for accurate localization increases with the complexity of the environment.

Scan Matching Algorithms:
Scan matching algorithms, also known as scan alignment or scan registration algorithms, aim to estimate the robot's pose by aligning consecutive 2D or 3D sensor scans obtained from range sensors, such as laser scanners or depth cameras. The algorithm compares the current scan with a reference scan (usually from a map or a previous scan) and finds the transformation (translation and rotation) that best aligns the two scans.
The alignment is typically performed by optimizing an objective function that measures the similarity between the two scans. This optimization process minimizes the difference between corresponding points or features in the scans, adjusting the robot's pose until the best alignment is achieved. Iterative Closest Point (ICP) is a commonly used algorithm for scan matching, but there are other variants and techniques available.

Scan matching algorithms are computationally efficient and can provide real-time localization results. They are especially effective in situations where the environment is well-structured and the robot's motion is relatively small between consecutive scans. However, they are sensitive to errors and uncertainties in the sensor measurements, and they may struggle in situations with limited distinctive features or in dynamic environments.

In summary, particle filters (MCL) and scan matching algorithms are both techniques for robot localization, but they employ different approaches. Particle filters use probabilistic sampling and weighting of pose hypotheses to estimate the robot's pose, while scan matching algorithms align consecutive scans to find the best pose estimate. Particle filters are more flexible but computationally demanding, while scan matching algorithms are computationally efficient but sensitive to sensor errors and require distinctive features for accurate localization.

        
    SLAM (Graph SLAM, EKF SLAM, Fast SLAM, Topological SLAM, Visual SLAM, Lidar SLAM)
    Dead Reckoning
    inertial Visual Odometry
    AMCL
    
    Camera
    Lidar
  Tracking
  Sensor Fusion
  
Planning:
  Behavior Planning:
    Finite State Machines
    Markov Decision Process
  Path Planning
    Local
      Graphs: A*, Dijkrtas, etc
      Sampling: RRT. RRT*
      Curve interpolation
      Numerical Optimization
    Global
  Tragectory generation
Control:
  MPC
  Pure Pursuit Control
  PID


SLAM:
  SLAM techniques are used in robotics to generate a map of an unknown environment. With the generated map, robot can localize itself during autonomous run.
  1. LIDAR SLAM
  2. Visual SLAM:
     Visual SLAM algorithm contains following steps

     Sensor Data Acquisition(Data from Camera)
     Visual Odometry
     Loop Closing
     Reconstruction
Good article to read on VSlam is
https://medium.com/@dcasadoherraez/introduction-to-visual-slam-chapter-1-introduction-to-slam-a0211654bf0e
     
