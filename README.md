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
     
