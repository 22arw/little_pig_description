# Little Pig Description - ROS Package
The little-pig-description repository contains all the code describing little pig. This includes the urdf files which describe all the joints and links. <br>

The basic_laser_pig urdf (and gazebo file) is a generic version of little pig that has been replaced by little_pig_base. These urdf files are set up as xacro files which are parsed into a full xml description on startup. The urdf files also contains gazebo plugins that will load in the simulation. <br>

The relevant files for the little_pig_base urdf are found in subfolders: the meshes subfolder is used by gazebo to represent the body and wheels. The xacro folder contains "macros" which are individual components loaded by the base urdf. Any new joints or simulated components should be placed here and called by the base file. The "params" folder contains measurements and other descriptions that are used as xacro variables in the other files. <br>

The config folder currently contains the parameters used by the simulated ackermann controller. The launch folder is a simple launched file called from little_pig_ctrl that finds the robot description, calls xacro to parse the urdf, and loads into robot_description for the other ros nodes to use. <br>


## Content Descriptions
<This repository is meant for all the desciption based code **only**. Example's of such:>
<- Adding some simulated properties to Basic Pig such as RPLIDAR, IntelRealSense, etc....>
  
Ackermann Config is the description of the simulated pig. It turns out that lowering the wheelbase produces a more accurate version of odom in the simulation  
  
Upload robot launch is a generic launch file that takes a urdf file and loads it to the parameter server  
  
Gazebo file is for all of the plugins and eventually will hold the laser and the imu

urdf.xacro files hold the description of the vehicle. The only description is basic_laser_pig
