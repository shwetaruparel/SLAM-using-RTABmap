# SLAM-using-RTABmap

## ABSTRACT
Abstract—What if a robot has to uncover the information of an unknown place like a differentplanet, or a home environment where the setting of the furniture changes and the prior map givento the robot is no more valid.Since the navigation of the robot in an environment involves knowing its own location and those ofits goals,this problem is more commonly known asSimultaneous Localization and Mapping(SLAM), a problem solved by computing the robot pose and a map of its environment of operationat the same time.This paper presents the techniques and comparison of different slam algorithms used in creating2D occupancy grid and 3D octomaps from the provided simulated environment and newly createdsimulation environment.

### To read more check the Slam_mapnyworld pdf 

https://github.com/shwetaruparel/SLAM-using-RTABmap/blob/master/SLAM_mapmyworld.pdf

## Steps to create the package slam_project and executing the SLAM for kitechen-dining and Gas-Station Test Environments.

Build your catkin workspace and initialise

$ mkdir -p ~/home/workspace/catkin_ws/src

$ cd /home/workspace/catkin_ws/src

$ catkin_init_workspace

$ cd ..

$ catkin_make

Perform a System Update/Upgrade

$ apt-get update

$ apt-get upgrade -y

Download the Project Repository https://github.com/shwetaruparel/SLAM-using-RTABmap and copy slam_project in src

Build the packages

$ catkin_make

$ source devel/setup.bash

Deploy the slam bot in Gas Station Test enviroment.

Open 4 -5 terminal windows and perform the following on each

$ cd /home/workspace/catkin_ws

$ source devel/setup.bash

Launch three different packages on separate terminals.

$ roslaunch slam_project slam_world.launch

On a different Terminal launch the teleop node for controlling through a keyboard.

$ roslaunch slam_project teleop.launch

On another terminal launch mapping node to start mapping the environment.

$ roslaunch slam_project mapping.launch


You will see the following packages running.

1) Gazebo with gas station environment and slam  bot at initial position.

2) Rviz that helps to visualise the robot model, tf links, map, octomap, 

3) RtabMap to viw statistics, for loop closure, to visualise odometry and 3d maps.

If you want to change the environment for kitchen-dining , go to slam_project/launch/slam_world.launch

Change     <arg name="world_name" value="$(find slam_project)/worlds/gasstation.world"/>

to 
    
    <arg name="world_name" value="$(find slam_project)/worlds/kitchen_dining.world"/>
    
After minium 3 loop closures , check the following on a different termninal.

$ rtabmap-databaseViewer ~/.ros/rtabmap.db

Once open, add some windows to get a better view of the relevant information, so:

Say yes to using the database parameters
View -> Constraint View
View -> Graph View

Enjoy mapping the environment and experiment with mapping parameters 






