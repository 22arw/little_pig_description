# Little Pig Description - ROS Package

This repository is meant for all the desciption based code **only**. Example's of such:
- Adding some simulated properties to Basic Pig such as RPLIDAR, IntelRealSense, etc....
  
Ackermann Config is the description of the simulated pig. It turns out that lowering the wheelbase produces a more accurate version of odom in the simulation  
  
Upload robot launch is a generic launch file that takes a urdf file and loads it to the parameter server  
  
Gazebo file is for all of the plugins and eventually will hold the laser and the imu

urdf.xacro files hold the description of the vehicle. The only description is basic_laser_pig
