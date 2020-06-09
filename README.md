# Little Pig Description - ROS Package

This repository is meant for all the desciption based code **only**. Example's of such:
- Adding some simulated properties to Basic Pig such as RPLIDAR, IntelRealSense, etc....

### Installation instructions

Heres a simple guide to get you started with Little Pig Description. Before continuing, be sure to have ROS Melodic installed.

- **Step 1.**
  - ```cd catkin_ws/src```
- **Step 2.**
  - ```git clone https://github.com/22arw/little_pig_description.git```
  - If you don't have the other three packages you can run these lines also:
    - ```git clone https://github.com/22arw/little_pig_ctrl.git```
    - ```git clone https://github.com/22arw/little_pig_rviz.git```
    - ```git clone https://github.com/22arw/little_pig_gazebo.git```

Your resulting directory should have this layout:

- catkin_ws/
  - src/
    - little_pig_ctrl/
    - little_pig_description/
    - little_pig_gazebo/
    - little_pig_rviz/

### Usage Instructions

Once you have this repo downloaded, run the following commands in the terminal:

- ```cd ..```
- ```catkin_make```

This should completed without failing. If it does fail, call Coach. There are not any files that launch in this repo. It's more of a dependency.

### Using Laser Simulation with RVIZ/Gazebo

Before launching Gazebo, you will need to open another terminal tab and run the following command:

- ```rosrun tf static_transform_publisher 0 0 0 0 0 1 map basic_laser_pig/laser_link 100```

This is a publisher which tells rviz how to transform the laser link into the map frame.

Now, you can launch Gazebo and RVIZ. Inside of RVIZ, add the laser component to the displays with the LaserScan topic set to /basic_laser_pig/laser_link. Also check the Global Options to ensure the fixed frame is set o map. 