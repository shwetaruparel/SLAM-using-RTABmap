# SLAM-using-RTABmap

## ABSTRACT
Abstract—What if a robot has to uncover the information of an unknown place like a differentplanet, or a home environment where the setting of the furniture changes and the prior map givento the robot is no more valid.Since the navigation of the robot in an environment involves knowing its own location and those ofits goals,this problem is more commonly known asSimultaneous Localization and Mapping(SLAM), a problem solved by computing the robot pose and a map of its environment of operationat the same time.This paper presents the techniques and comparison of different slam algorithms used in creating2D occupancy grid and 3D octomaps from the provided simulated environment and newly createdsimulation environment.

### To read more check the Slam_mapnyworld pdf 

https://github.com/shwetaruparel/SLAM-using-RTABmap/blob/master/SLAM_mapmyworld.pdf

## Steps to create the package slam_project and executing the SLAM for kitechen-dining and Gas-Station Test Environments.

1. Build your catkin workspace and initialise

$ mkdir -p ~/home/workspace/catkin_ws/src

$ cd /home/workspace/catkin_ws/src

$ catkin_init_workspace

$ cd ..

$ catkin_make

Perform a System Update/Upgrade

$ apt-get update

$ apt-get upgrade -y

Download the Project and copy slam_project in src

Build the packages

$ catkin_make

$ source devel/setup.bash
