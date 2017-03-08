# robot #

## Setup of standard ROS VM ##
**Download and install VirtualBox and VirtualBox Extension Pack**
https://www.virtualbox.org/wiki/Downloads

**Download ros indigo64bit VM**
https://drive.google.com/file/d/0B_ULD8CBaw26TEpqUG1McGs5aVU/view?usp=sharing

(http://nootrix.com/downloads/)

**Configure and start VM**
You may need to change some things in the configuration e.g. ubuntu32 ->ubuntu64

## Run Demo ##
In individual terminals start the following nodes:

**as always start roscore**
- $ roscore

**start simulated robot node**
- $ rosrun turtlesim turtlesim_node

**start keyboard input driver node**
- $ rosrun turtlesim turtle

## Setup of ROS industrial ##
**Add sources for ros packages**
- $ sudo sh -c 'echo "deb http://packages.ros.org/ros/ubuntu trusty main" > /etc/apt/sources.list.d/ros-latest.list'
- $ wget https://raw.githubusercontent.com/ros/rosdistro/master/ros.key -O - | sudo apt-key add -
- $ sudo apt-get update

**Install UR ros driver**
http://wiki.ros.org/universal_robot

**Getting started with ROS industrial and UR**
http://wiki.ros.org/universal_robot/Tutorials/Getting%20Started%20with%20a%20Universal%20Robot%20and%20ROS-Industrial

**Install MoveIt!**
http://moveit.ros.org/install/


