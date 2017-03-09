# robot #

## Setup of standard ROS VM ##
**Download and install VirtualBox and VirtualBox Extension Pack**
https://www.virtualbox.org/wiki/Downloads

Note: I experienced that, sometimes, the network adapter for VirtualBox messes with the network access on the work PC, if that is the case, simply disable it while not using the VM.

**Download ros indigo64bit VM**
https://drive.google.com/file/d/0B_ULD8CBaw26TEpqUG1McGs5aVU/view?usp=sharing

(http://nootrix.com/downloads/)

**Configure and start VM**
You may need to change some things in the configuration e.g. ubuntu32 ->ubuntu64

user password: viki

**update system**
- $ sudo apt-get upgrade
If asked where to install grup, select with "space bar" and press enter

## Run Demo ##
In individual terminals start the following nodes:

**as always start roscore**
- $ roscore

**start simulated robot node**
- $ rosrun turtlesim turtlesim_node

**start keyboard input driver node**
- $ rosrun turtlesim turtle

## Installation of ROS industrial ##
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

## Issues ##
There is problems with 3D hardware acceleration in the guest OS. This means that any 3D visualization results in errors like this "libGL error: failed to load driver: vboxvideo"

This command will reveal the problem if it exists
- $ sudo /usr/lib/nux/unity_support_test -p

This should not happen if the system is updated:
- $ sudo apt-get upgrade

Possible fix:
Install Guest Additions(https://help.ubuntu.com/community/VirtualBox/GuestAdditions)
- $ sudo apt-get install virtualbox-guest-additions-iso

Possible workaround(slow):
- $ export LIBGL_ALWAYS_SOFTWARE=1
or disable 3D acceleration in Virtual box
